wget http://springdale.math.ias.edu/data/puias/computational/6/x86_64/git-1.8.3.1-1.sdl6.x86_64.rpm
wget http://springdale.math.ias.edu/data/puias/computational/6/x86_64/perl-Git-1.8.3.1-1.sdl6.noarch.rpm
yum remove git -y
yum localinstall git-*.rpm perl-Git-*.noarch.rpm -y
git config --global http.sslVerify false
git config http.sslVerify false
yum update -y nss curl libcurl # 이것만 작동됨
