usefull links:

install pgadmin 4 venv:

https://linuxhint.com/install-pgadmin4-ubuntu/


https://www.e2enetworks.com/help/knowledge-base/install-pgadmin-4-on-ubuntu-16-04/


STEPS:
1-download wheell and follow the artcile execpt install venv with python 3, since the default is 2:
 virtualenv -p python3 pgAdmin4
 cd pgAdmin4/
 source bin/activate

2- install with pip 3 the wheel: 
 pip3 install pgadmin4-4.2-py2.py3-none-any.whl 

3 - run pgadmin from command:
python3  lib/python3.6/site-packages/pgadmin4/pgAdmin4.py 

4 - the shell script that run pgadmin should be copied:
cp  /home/salim/Programs/pgadmin4/pgadmin4Bck/pgadmin4 /home/salim/Programs/pgadmin4/pgadmin4/pgAdmin4/

5- make sure the service point to the shell script:
nano /etc/systemd/system/pgadmin4.service 


Appendix:
The script:

:~/Programs/pgadmin4$ more pgadmin4/pgAdmin4/pgadmin4
#!/bin/bash
cd ~/Programs/pgadmin4/pgadmin4/pgAdmin4
source bin/activate
python3 lib/python3.6/site-packages/pgadmin4/pgAdmin4.py

