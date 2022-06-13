# DO180-apps
DO180 Repository for Sample Applications

=====================
```

nikhil@nimone-mac DO180 % mv ~/Downloads/rht_classroom.rsa ~/.ssh/
chmod 0600 ~/.ssh/rht_classroom.rsa
ssh-add ~/.ssh/rht_classroom.rsa
Identity added: /Users/nikhil/.ssh/rht_classroom.rsa (/Users/nikhil/.ssh/rht_classroom.rsa)
nikhil@nimone-mac DO180 % ssh -i ~/.ssh/rht_classroom.rsa -J cloud-user@169.56.41.225:22022 student@172.25.252.1 -p 53009
The authenticity of host '[172.25.252.1]:53009 (<no hostip for proxy command>)' can't be established.
ED25519 key fingerprint is SHA256:kms08uEzMMkZKPygxhZ5POSpCpCQW6t7q94RzsqgZ9s.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[172.25.252.1]:53009' (ED25519) to the list of known hosts.
student@172.25.252.1's password: 
Activate the web console with: systemctl enable --now cockpit.socket

Register this system with Red Hat Insights: insights-client --register
Create an account or view all your systems at https://red.ht/insights-dashboard
Last login: Mon Jun 13 11:34:46 2022

[student@workstation ~]$ lab-configure 

This script configures the connection parameters to access the OpenShift cluster for your lab scripts

Verifying your API Endpoint...

Verifying your Nexus host...

Verifying your OpenShift developer user credentials...

Verifying your GitHub account name...

Verifying your Quay.io account name...

Verifying your cluster configuration...

Saving your lab configuration file...

All fine, lab config saved. You can now proceed with your exercises.

If you need to modify the configuration, rerun this script or directly modify the values in /usr/local/etc/ocp4.config.

[student@workstation ~]$ git clone https://github.com/nikhilmone/DO180-apps.git
Cloning into 'DO180-apps'...
remote: Enumerating objects: 74, done.
remote: Total 74 (delta 0), reused 0 (delta 0), pack-reused 74
Unpacking objects: 100% (74/74), 223.95 KiB | 432.00 KiB/s, done.


[student@workstation DO180-apps]$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
[student@workstation DO180-apps]$ git checkout -b testbranch
Switched to a new branch 'testbranch'
[student@workstation DO180-apps]$ echo "DO180" > TEST
[student@workstation DO180-apps]$ git add .
[student@workstation DO180-apps]$ git commit -m "DO180"
[testbranch b048340] DO180
 1 file changed, 1 insertion(+)
 create mode 100644 TEST
[student@workstation DO180-apps]$ git push --set-upstream origin testbranch

(process:3384): Gtk-WARNING **: 11:44:48.602: Locale not supported by C library.
	Using the fallback 'C' locale.

(gnome-ssh-askpass:3384): Gtk-WARNING **: 11:44:48.604: cannot open display: 
error: unable to read askpass response from '/usr/libexec/openssh/gnome-ssh-askpass'
Username for 'https://github.com': nikhilmone

(process:3402): Gtk-WARNING **: 11:46:16.305: Locale not supported by C library.
	Using the fallback 'C' locale.

(gnome-ssh-askpass:3402): Gtk-WARNING **: 11:46:16.306: cannot open display: 
error: unable to read askpass response from '/usr/libexec/openssh/gnome-ssh-askpass'
Password for 'https://nikhilmone@github.com': 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 284 bytes | 284.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'testbranch' on GitHub by visiting:
remote:      https://github.com/nikhilmone/DO180-apps/pull/new/testbranch
remote: 
To https://github.com/nikhilmone/DO180-apps.git
 * [new branch]      testbranch -> testbranch
Branch 'testbranch' set up to track remote branch 'testbranch' from 'origin'.
[student@workstation DO180-apps]$ 
[student@workstation DO180-apps]$ echo "OCP4" > TEST
[student@workstation DO180-apps]$ git add .
[student@workstation DO180-apps]$ git commit -m "OCP4"
[testbranch 8a9d6b8] OCP4
 1 file changed, 1 insertion(+), 1 deletion(-)
[student@workstation DO180-apps]$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 273 bytes | 273.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/nikhilmone/DO180-apps.git
   b048340..8a9d6b8  testbranch -> testbranch
[student@workstation DO180-apps]$ head README.md 
# DO180-apps
DO180 Repository for Sample Applications
[student@workstation DO180-apps]$ podman search rhel
INDEX       NAME                                                                    DESCRIPTION                                      STARS       OFFICIAL    AUTOMATED
                   
redhat.com  registry.access.redhat.com/rhel                                         This platform image provides a minimal runti...  0                       
                                                                                                0                       
[student@workstation DO180-apps]$ podman pull rhel
Resolved "rhel" as an alias (/etc/containers/registries.conf.d/001-rhel-shortnames.conf)
Trying to pull registry.access.redhat.com/rhel:latest...
Getting image source signatures
Checking if image destination supports signatures
Copying blob 2671352e0ee1 done  
Copying blob 61237c26b238 done  
Copying config acf3e09a39 done  
Writing manifest to image destination
Storing signatures
acf3e09a39c95d354539b6591298be0b0814f5d74e95e722863241192b9a079b
[student@workstation DO180-apps]$ podman images
REPOSITORY                       TAG         IMAGE ID      CREATED      SIZE
registry.access.redhat.com/rhel  latest      acf3e09a39c9  4 weeks ago  216 MB
[student@workstation DO180-apps]$ 
[student@workstation DO180-apps]$ 
[student@workstation DO180-apps]$ 
```
