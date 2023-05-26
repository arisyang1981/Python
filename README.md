# Python


# Solved case 
Tags: pip and SSL  
Problem: pip is configured with locations that require TLS/SSL, however the ssl module in Python is not available. 
Description: Above error when issue 'pip install module' with pip and openssl. 
Solution: Rebuild Python from source. 
Steps: 
cd /usr/src 
sudo wget https://www.python.org/ftp/python/3.9.16/Python-3.9.16.tgz 
sudo tar -xvzf Python-3.9.16.tgz 
cd Python-3.9.16 
sudo ./configure --prefix=/usr/local/python3 --with-openssl=/usr/local/openssl 
sudo make 
sudo make altinstall 
sudo ln -s /usr/local/python3/bin/python3 /usr/bin/python3 
