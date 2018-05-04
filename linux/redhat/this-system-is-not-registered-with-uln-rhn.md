this-system-is-not-registered-with-uln-rhn

https://flashdba.com/2012/10/08/this-system-is-not-registered-with-uln-rhn/





<pre>

This system is not registered with ULN / RHN
OCTOBER 8, 2012 13 COMMENTS

One of the features of WordPress is the ability to see search terms which are taking viewers to your blog. One of the all-time highest searches bringing traffic to my site is “This system is not registered with ULN”… and sure enough if I search for that phrase on Google my site is one of the top links, taking people to one of my Violin Memory array Installation Cookbooks.

So I guess it’s only fair that I give these passers by some sort of advice on what to do if you see this message…

1. Don’t Panic
Chances are you have built a new Linux system using Red Hat Enterprise Linux or its twin sister Oracle Linux. You are probably now trying to use yum to install software packages, but every time you do so you see something similar to this:

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

2. Register Your System
If you have Oracle or Red Hat support then you might as well register your system so that it can take advantage of their yum channels.

In systems prior to RHEL6 / OL6 you used a utility called up2date to register:

# up2date --register
Or if you want to use the text-mode version:

# up2date-nox --register
You can find a good tutorial explaining the process here. In RH6 / OL6 the process changed, so now you call the relevant utility.

For Red Hat you need to use the rhn_register command (actually this also became available in RHEL5). You will need your Red Hat Network login and password.

For Oracle Linux you need to use the uln_register command. You will need your Oracle ULN login, password and Customer Service Identifier (CSI).

Once your registration is complete the message “This system is not registered” should leave you alone.

3. Don’t Have Support?
Of course, not everybody has a support contract with Red Hat or Oracle. Some people have one but can’t find the details. Others can’t be bothered to set it up. If any of these applies to you then there is another alternative, which is the Oracle Public Yum Server. [Fair play to Wim and the team for making this available, because it’s been making my life easier for years now…]

Oracle’s public yum server is a freely available source of Linux OS downloads. Simply point your browser here and follow the instructions: http://public-yum.oracle.com/

In essence, you use wget to download the Oracle repo file which relates to your system and then (optionally) edit it to choose the yum channel you want to subscribe to (otherwise it will use the latest publicly-available stuff). The versions of the Linux software on the public yum repositories are (I believe) not as up-to-date as those you would get if you subscribed to a support contract, but they are still very new.

And the best bit is you can also use it if you have Red Hat installed; it isn’t restricted to Oracle Linux users. Having said that, make sure you don’t do anything which invalidates your support contracts. By pointing a RHEL system at the Oracle public yum server and running an update you are effectively converting your system to become Oracle Linux.

Here’s an example of how to set it up for OL6:

# cd /etc/yum.repos.d
# wget http://public-yum.oracle.com/public-yum-ol6.repo


This gets yum working and so allows for the Oracle Validated / Oracle Preinstall RPM to be installed in order to setup the database…

Hopefully that will satisfy some of my wayward blog visitors!




</pre>



