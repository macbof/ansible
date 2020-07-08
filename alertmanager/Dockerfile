FROM centos:centos8

RUN mkdir /alertmanager /etc/alertmanager \
    && chown -R nobody: /alertmanager /etc/alertmanager

USER nobody

COPY alertmanager.yml /etc/alertmanager
COPY alertmanager /bin/alertmanager
COPY amtool /bin/amtool

EXPOSE 9093
WORKDIR /etc/alertmanager
ENTRYPOINT [ "/bin/alertmanager" ]
CMD [ "--storage.path=/alertmanager" ]
