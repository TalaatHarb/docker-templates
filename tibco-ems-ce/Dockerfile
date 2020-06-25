FROM centos:latest
RUN yum install perl-IO-Compress unzip -y
COPY TIB_ems-ce_8.5.1_linux_x86_64.zip TIB_ems-ce_8.5.1.zip
RUN unzip TIB_ems-ce_8.5.1.zip
RUN rm TIB_ems-ce_8.5.1.zip
RUN rpm -i /TIB_ems-ce_8.5.1/rpm/TIB_ems-ce_8.5.1_linux_x86_64-server.rpm
RUN rpm -i /TIB_ems-ce_8.5.1/rpm/TIB_ems-ce_8.5.1_linux_x86_64-samples_src.rpm
RUN rpm -i /TIB_ems-ce_8.5.1/rpm/TIB_ems-ce_8.5.1_linux_x86_64-thirdparty.rpm
RUN mkdir /opt/tibco/ems/8.5/samples/config/datastore
RUN chmod 755 /opt/tibco/ems/8.5/samples/config/ -R
RUN chmod 777 /opt/tibco/ems/8.5/samples/config/datastore
WORKDIR /opt/tibco/ems/8.5/samples/config
CMD ["/opt/tibco/ems/8.5/bin/tibemsd", "-config", "tibemsd.conf"]
