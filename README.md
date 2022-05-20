# gh-actions-ansible
Ansible in Docker for Github Actions

```
.
├── .github
│   └── workflows
│       └── master.yml
├── .ssh
│   └── id_rsa-encrypted
└── ansible
    ├── Dockerfile
    ├── action.yml
    ├── entrypoint.sh
    ├── hosts
    └── playbook.yml
```

# Instructions

## Step 1

- Place your ssh key as ```id_rsa``` in ```~/.ssh``` locally
- Run this command to encrpyt your ssh key with passphase
```
echo "your-secret-password" > ansible_vault_password.txt &&\
ansible-vault \
encrypt \
--vault-password-file=ansible_vault_password.txt \
~/.ssh/id_rsa \
--output=id_rsa-encrypted &&\
rm ansible_vault_password.txt
```

## Step 2

Create Actions Secret ```VAULT_PASS``` for ```your-secret-password``` passphase 

## Step 3

Edit ```hosts``` in ```./ansible/hosts```

## Step 4

Edit ```playbook.yml``` in ```./ansible/playbook.yml```




