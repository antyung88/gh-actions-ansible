FROM alpine
RUN apk add --update ansible
ENV ANSIBLE_HOST_KEY_CHECKING=False
COPY entrypoint.sh /entrypoint.sh
RUN ["chmod", "+x", "/entrypoint.sh"]
ENTRYPOINT ["/entrypoint.sh"]
