# fah
wget https://download.foldingathome.org/releases/public/release/fahclient/centos-6.7-64bit/v7.5/fahclient-7.5.1-1.x86_64.rpm
wget https://download.foldingathome.org/releases/public/release/fahcontrol/centos-6.7-64bit/v7.5/fahcontrol-7.5.1-1.noarch.rpm
sudo rpm -i --nodeps fah*
cd /usr/lib
sudo ln -s /usr/lib/python2.7 /usr/lib/python2.6
sudo cp -R /usr/lib/python2.6/site-packages/fah /usr/lib/python2.7/site-packages/fah
sudo wget https://raw.githubusercontent.com/rehmert/fah/master/config.xml
sudo mv -f config.xml /etc/fahclient/config.xml
sudo shutdown -r -t 30
