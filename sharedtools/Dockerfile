FROM centos:7
#hashicorp/terraform:1.0.7
RUN yum update -y && \
    yum install telnet -y && \
    yum install wget -y && \
    yum install unzip -y && \
    yum install elinks -y && \
    wget https://releases.hashicorp.com/terraform/1.0.7/terraform_1.0.7_linux_amd64.zip && \
    unzip terraform_1.0.7_linux_amd64.zip && \
    mv terraform  /usr/bin && \
    rm -rf terraform_1.0.7_linux_amd64.zip && \
    rm -rf /usr/sbin/packer && \
    wget https://releases.hashicorp.com/packer/1.6.1/packer_1.6.1_linux_amd64.zip && \
    unzip packer_1.6.1_linux_amd64.zip && \
    rm -rf packer_1.6.1_linux_amd64.zip

CMD ["/usr/sbin/httpd","-D","FOREGROUND"] 