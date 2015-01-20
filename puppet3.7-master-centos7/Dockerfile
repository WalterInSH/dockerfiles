FROM walterinsh/puppet3.7-centos7:latest

RUN yes | yum install puppetserver \
    && yum clean all

ADD puppet.conf /etc/puppet/puppet.conf

VOLUME ["/opt/puppet"]

EXPOSE 8140

CMD ["/bin/mkdir", "/opt/puppet"]

ADD puppet.conf /etc/puppet/puppet.conf

CMD [ "/usr/bin/puppet", "master", "--verbose"]

