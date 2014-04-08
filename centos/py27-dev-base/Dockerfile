FROM minadyn/centos-epel
MAINTAINER minadyn@gmail.com
RUN yum -y groupinstall development 
RUN yum install -y zlib-dev openssl-devel sqlite-devel bzip2-devel
# install python 2.7
RUN wget http://www.python.org/ftp/python/2.7.6/Python-2.7.6.tar.xz && xz -d Python-2.7.6.tar.xz && tar xvf Python-2.7.6.tar && cd Python-2.7.6 && ./configure --prefix=/usr/local && make && make altinstall
# install pip
RUN wget --no-check-certificate https://pypi.python.org/packages/source/s/setuptools/setuptools-1.4.2.tar.gz && tar -xvf setuptools-1.4.2.tar.gz && cd setuptools-1.4.2 && python2.7 setup.py install
RUN curl https://raw.github.com/pypa/pip/master/contrib/get-pip.py | python2.7 -
