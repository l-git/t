


http://allpcworld.com/download-rhel-red-hat-linux-6-6-free/


<a>http://www.linuxidc.com/Linux/2011-09/43704.htm</a>

redhat enterprise linux 6.0 download url

rhel




http://www.linuxidc.com/Linux/2011-09/43704.htm



red hat enterprise linux  6 install


url:http://www.linuxidc.com/Linux/2011-09/43704.htm


only support thunder download:

https://content-web.rhn.redhat.com/rhn/isos/rhel-6.0/md5sum/f7141396c6a19399d63e8c195354317d/rhel-server-6.0-x86_64-dvd.iso?__gda__=1289476047_dab4280abd4dcbb41b1b165a0e2c82f8&ext=.iso







system is not registered with rhn (red hat network)

Here’s an example of how to set it up for OL6:
# cd /etc/yum.repos.d
# wget http://public-yum.oracle.com/public-yum-ol6.repo

change gpa-check=1 to gpa-check=0 in public-yum-ol6.repo 


then yum can used

yum (yellowdog updater modifier)


update gcc
yum update gcc


install g++


yum install gcc-c++



install gdb
yum install gdb



gcc -v

4.4.7




install jdk

downlad jdk tar

extra

vi .bash_profile 


# .bash_profile

# Get the aliases and functions
if [ -f ~/.bashrc ]; then
        . ~/.bashrc
fi

# User specific environment and startup programs



JAVA_HOME=$HOME/jdk1.7.0_80

PATH=$JAVA_HOME/bin:$PATH:$HOME/bin

export JAVA_HOME

export PATH


.bash_path variable must be ordered, so JAVA_HOME must be before it used (path=$java_home)


install tomcat

download tomcat


extra tomcat

start ./startup.sh
















http://public-yum.oracle.com/RPM-GPG-KEY-oracle-ol6


-----BEGIN PGP PUBLIC KEY BLOCK-----
Version: GnuPG v1.4.5 (GNU/Linux)

mQENBEwtJWoBCACpiY2rGA6T0ceBi92X88/QclytVBjtDRohOVzs3pmIPh3ULqsW
G323nmyKbKQBBSjh9OnuO9Y09VG8mzr/w9YV0Ix4cI9/HDTERZ2+TR5u+VNn5J5h
yvwQSN/FEK6oH2+mz7O0yUNleN7UltR4MOEkHIoAhIvv+1AQQKN3OM8oalz+3gv/
zz9rAoQczQzT7QWOtBrsRMZgBrKXY/TpJrpVSO3Hx8CnbhKGtLxCCrxZ5v7hh1ht
3CRAr2+h5bDA9KP6vBZWKEs7NgcvtZFDY6EJc7AoApr3phX9hHE2+snTxe82DkFT
uA69C8wLyjPCoSy+tcaCqJKOZelNy9RN/WKRABEBAAG0RE9yYWNsZSBPU1MgZ3Jv
dXAgKE9wZW4gU291cmNlIFNvZnR3YXJlIGdyb3VwKSA8YnVpbGRAb3NzLm9yYWNs
ZS5jb20+iQE8BBMBAgAmBQJMLSVqAhsDBQkWjmoABgsJCAcDAgQVAggDBBYCAwEC
HgECF4AACgkQcvl7dOxVHwMiNAf/cD8R74fCBeQsAYid5slIz7CG8xEOBUTDNEJT
p/owtzr7m7Ydp1txNBOkVeVkUP8czX5EldcmoxA4kCCyHhnxmpJnOt52Fy5ZRnYh
Ll5gYdpJpXGVScB7fnlh3rJAaesSTacVFC5MKIYPZBiTo9soSXMLNcG8WqHPasdd
AblC4t5BTDNYlX1RiPeP6m5egHnnxyAXsis8fqIZY0RC9hERxWQ6hdDAX0tJXY8F
88HDUozvo8jqTlg/5GZcfqcbUjjMUJQ5cBtH3adCthMycdPpPXWJQBuzMIdFJ03u
YuQ3XrKxBkOLips+OZuWNVZzrPOHsenb49aX4yQsLVc2E2fhKQ==
=M8XY
-----END PGP PUBLIC KEY BLOCK-----













https://flashdba.com/2012/10/08/this-system-is-not-registered-with-uln-rhn/



This system is not registered with ULN / RHN
OCTOBER 8, 2012 13 COMMENTS
One of the features of WordPress is the ability to see search terms which are taking viewers to your blog. One of the all-time highest searches bringing traffic to my site is “This system is not registered with ULN”… and sure enough if I search for that phrase on Google my site is one of the top links, taking people to one of my Violin Memory array Installation Cookbooks.
So I guess it’s only fair that I give these passers by some sort of advice on what to do if you see this message…
1. Don’t PanicChances are you have built a new Linux system using Red Hat Enterprise Linux or its twin sister Oracle Linux. You are probably now trying to use yum to install software packages, but every time you do so you see something similar to this:
# yum install oracle-validated -y
Loaded plugins: rhnplugin, security
This system is not registered with ULN.
ULN support will be disabled.
ol5_u7_base | 1.1 kB 00:00
Setting up Install Process
Resolving Dependencies
--> Running transaction check
---> Package oracle-validated.x86_64 0:1.1.0-14.el5 set to be updated
...

This is the Oracle Linux variant. If it was Red Hat you would see:
This system is not registered with RHN
RHN support will be disabled.
The first thing to understand is that you can quite happily build and run a system in this state – in fact I’m willing to bet there are many systems out there exhibiting this message every time somebody calls yum.
The message simply means that you have not registered this build of your system with Oracle or Red Hat. Both companies have a paid support offering which allows you to register a system and do things like get software updates. Red Hat’s is call the Red Hat Network (RHN) and Oracle’s, with their marketing department’s usual sense of humour, is called the Oracle Unbreakable Linux Network (ULN). [I’ve been critical of some Oracle products in the past but I have to say that I love Oracle Linux, even if I do find the name “Unbreakable” a bit daft…]
You don’t have to register your system with the vendor’s support network in order to be able to use it. I’m not making any statements about your support contract, if you have one – I’m just saying that it will work quite normally without it.
2. Register Your SystemIf you have Oracle or Red Hat support then you might as well register your system so that it can take advantage of their yum channels.
In systems prior to RHEL6 / OL6 you used a utility called up2date to register:
# up2date --register

Or if you want to use the text-mode version:
# up2date-nox --register

You can find a good tutorial explaining the process here. In RH6 / OL6 the process changed, so now you call the relevant utility.
For Red Hat you need to use the rhn_register command (actually this also became available in RHEL5). You will need your Red Hat Network login and password.
For Oracle Linux you need to use the uln_register command. You will need your Oracle ULN login, password and Customer Service Identifier (CSI).
Once your registration is complete the message “This system is not registered” should leave you alone.
3. Don’t Have Support?Of course, not everybody has a support contract with Red Hat or Oracle. Some people have one but can’t find the details. Others can’t be bothered to set it up. If any of these applies to you then there is another alternative, which is the Oracle Public Yum Server. [Fair play to Wim and the team for making this available, because it’s been making my life easier for years now…]
Oracle’s public yum server is a freely available source of Linux OS downloads. Simply point your browser here and follow the instructions: http://public-yum.oracle.com/
In essence, you use wget to download the Oracle repo file which relates to your system and then (optionally) edit it to choose the yum channel you want to subscribe to (otherwise it will use the latest publicly-available stuff). The versions of the Linux software on the public yum repositories are (I believe) not as up-to-date as those you would get if you subscribed to a support contract, but they are still very new.
And the best bit is you can also use it if you have Red Hat installed; it isn’t restricted to Oracle Linux users. Having said that, make sure you don’t do anything which invalidates your support contracts. By pointing a RHEL system at the Oracle public yum server and running an update you are effectively converting your system to become Oracle Linux.
Here’s an example of how to set it up for OL6:
# cd /etc/yum.repos.d
# wget http://public-yum.oracle.com/public-yum-ol6.repo



https://unix.stackexchange.com/questions/207907/how-to-fix-gpg-key-retrieval-failed-errno-14


How to fix GPG key retrieval failed: [Errno 14]?
up vote3down votefavorite
I'm using Centos 6.5 and when I want to install packages from yum I get this error:
GPG key retrieval failed: [Errno 14] Could not open/read file:///etc/pki/rpm-gpg/RPM-GPG-KEY-puias

How can I fix this?
rpm repository
shareimprove this question
asked Jun 6 '15 at 6:30
ehsan88
153116

add a comment
4 Answers
activeoldestvotes
up vote4down voteaccepted
This error happens because you have some YUM repository configuration in /etc/yum.repos.d/ that lists a GPG key like this:
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-puias
This configuration is telling YUM that the GPG key for the repository exists on disk. The error you get from YUM is YUM letting you know that it couldn't find the GPG key at the path /etc/pki/rpm-gpg/RPM-GPG-KEY-puias
So, by manually writing the GPG key to /etc/pki/rpm-gpg/RPM-GPG-KEY-puias like you did, YUM was then able to find the key at that path.
Alternatively, you could have set gpgkey to the URL of the key, like this:
gpgkey=http://springdale.math.ias.edu/data/puias/6/x86_64/os/RPM-GPG-KEY-puias
in you repository configuration.
GPG and YUM/RPM can be quite tricky. If you are curious about how more of the internals work, check out this blog post.
shareimprove this answer
answered Jun 6 '15 at 18:19
Joe Damato
39425

add a comment
up vote1down vote
If you trust the repo, you can simply edit the file /etc/yum.repos.d/mysql-community.repo and disable the gpgcheck
[mysql57-community]
name=MySQL 5.7 Community Server
baseurl=http://repo.mysql.com/yum/mysql-5.7-community/el/6/$basearch/
enabled=1
gpgcheck=0

shareimprove this answer
answered Mar 13 at 14:13
Adam Deng
111

add a comment
up vote0down vote
This worked for me: Go to /etc/pki/rpm-gpg directory and download the RPM-GPG-KEY-puias fromhttp://springdale.math.ias.edu/data/puias/6/x86_64/os/RPM-GPG-KEY-puias :
su - root
cd /etc/pki/rpm-gpg
wget http://springdale.math.ias.edu/data/puias/6/x86_64/os/RPM-GPG-KEY-puias

By the way, I appreciate if someone explains the issue more.
shareimprove this answer
answered Jun 6 '15 at 6:30
ehsan88
153116

add a comment
u



p vote

0down vote
This issue occurs when you try to install Docker on CentOS using the standard installation guide available on the Official Website
In the Step 3 change the baseurl and gpgkey URL from https to http and it works, example below
$ sudo tee /etc/yum.repos.d/docker.repo <<-'EOF'
[dockerrepo]
name=Docker Repository
baseurl=**http**://yum.dockerproject.org/repo/main/centos/$releasever/
enabled=1
gpgcheck=1
gpgkey=**http**://yum.dockerproject.org/gpg
EOF

shareimprove this answer


https://docs.oracle.com/cd/E37670_01/E39381/html/ol_import_gpg.html


2.4 Downloading and Importing a GPG Key
Under some circumstances, such as when installing additional software in a virtual machine domain, you might need to download and import the GPG key to use with yum. To obtain and import a GPG key from the public yum repository:

	1. Download the GPG key, for example with the the wget command.
# wget http://public-yum.oracle.com/RPM-GPG-KEY-oracle-ol7
The following are the available GPG keys:

		* http://public-yum.oracle.com/RPM-GPG-KEY-oracle-ol7

		* http://public-yum.oracle.com/RPM-GPG-KEY-oracle-ol6

		* http://public-yum.oracle.com/RPM-GPG-KEY-oracle-el5

		* http://public-yum.oracle.com/RPM-GPG-KEY-oracle-el4


	2. 

	3. Check the fingerprint of the GPG key with the gpg command to make sure it matches the key published by Oracle.
# gpg --quiet --with-fingerprint ./RPM-GPG-KEY-oracle-0l7
The following are the published keys:

		* Oracle Linux 6 and 7:
pub 2048R/EC551F03 2010-07-01 Oracle OSS group (Open Source Software group)
      Key fingerprint = 4214 4123 FECF C55B 9086 313D 72F9 7B74 EC55 1F03



		* Oracle Linux 5:
pub 1024D/1E5E0159 2007-05-18 Oracle OSS group (Open Source Software group)
      Key fingerprint = 99FD 2766 28EE DECB 5E5A F5F8 66CE D3DE 1E5E 0159 
sub 1024g/D303656F 2007-05-18 [expires: 2015-05-16]



		* Oracle Linux 4:
pub 1024D/B38A8516 2006-09-05 Oracle OSS group (Open Source Software group)
      Key fingerprint = 1122 A29A B257 825F 322C 234E 2E2B CDBC B38A 8516
sub 2048g/0042D4F4 2006-09-05 [expires: 2011-09-04]




	4. If the fingerprint matches, import the GPG key with the rpm command.
# rpm --import ./RPM-GPG-KEY-oracle-ol7























































