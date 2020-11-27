---
layout: post
title: "Ten category"
description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit."
date:   2017-11-12 17:46:41 -0300
categories: start blog
by: 'Gustavo Quinalha'
icon: 'credit-card'
questions:
  - question: 'Question 10'
@@@@@@@@@@@@@@@@@@@@@@@@@@
@@			@@
@@    DISK ALERTS	@@
@@@@@@@@@@@@@@@@@@@@@@@@@@
 
##########################
#####   Home Alerts  #####    
##########################
/bin/ls -A /var/cpanel/users |xargs -n1 -I{}  sudo find  /home/{}/public_html/ -type f -name '*error_log' > testt.txt; while read file; do truncate -s 2 "$file"; done < testt.txt ;  rm -f testt.txt; echo -e "\n------------\n"; df -h | grep home
 
### ls -A /var/cpanel/users |xargs -n1 -I{}  sudo du -sh  /home/{}/public_html/error_log 2> /dev/null |xargs truncate -s 1 #### OLD COMMND
montool homediskusage
du -lh ~user| grep [0-9]G 
tail -20 /var/cpanel/accounting.log ; grep diskclean /opt/hgmods/monitoring/logs/montool.log ; montool homediskusage ; screen -S DiskClean -d -m -- /root/bin/montool diskclean  -d -a -p 90

screen -S chomex
find /home4/*/ -type d  \( -name *updraft\* -or -name *backup\* -or -name *Backup\* \)  -exec du -lh {} \;  | grep [0-9]G | grep -v eig | sort -rh > /ramdisk/homx.txt 
screen -S c1home1
find /homeX/*/ -type d  \( -name *updraft\* -or -name *backup\* -or -name *Backup\* -or -name *migration\* -or -name *old\* -or -name *Old\* -or -name *bak\* \)  -exec du -lh {} \;  | grep [0-9]G | grep -v eig | sort -rh > /ramdisk/homX.txt
screen -S c1lear 
find /home4 -name '**' -size +200M > /ramdisk/clear.txt

find -name '*uploads*' | grep -v 'uploads.zip\|uploads.php'| xargs rm -fv ; find -name '*others*' | grep -v 'others.zip\|others.php' | xargs rm -vf ; find -name '*plugins*' | grep -v 'plugins.zip\|pluginSs.php' | xargs rm -vf

find -name 'log.*' | xargs rm -f
for file in /path/sess_*; do rm -rfv "$file"; done
du -k | sort -n | perl -ne 'if ( /^(\d+)\s+(.*$)/){$l=log($1+.1);$m=int($l/log(1024)); printf  ("%6.1f\t%s\t%25s  %s\n",($1/(2**(10*$m))),(("K","M","G","T","P")[$m]),"*"x (1.5*$l),$2);}'
screen -ls | grep -e 'c1' -e 'cho'| awk '{print $1}' | xargs -I % -t screen -X -S % quit ; find /ramdisk | grep -e '.txt' -e 'clear.txt' | xargs rm -f ; service zabbix-agent restart; df -lh| grep /home
service zabbix-agent restart  ;sleep 5s ;service zabbix-agent restart

cd $(ls -d */ |sed -n '3p') ### Enter into Special type folder

##########################
##### /var / Alerts  #####
##########################
/bin/ls -A /var/cpanel/users |xargs -n1 -I{}  sudo du -sh  /home/{}/public_html/error_log 2> /dev/null  |grep G ; df -h| grep /var; w;screen -ls; history | grep scan.
lsof | grep "/var" | grep deleted ; ls -lhSr /var/log/domlogs | tail ; screen -S c1lear

find /var/lib/puppet/clientbucket/* -type f -mtime +30 -atime +30 -delete -print ;/scripts/clear_orphaned_virtfs_mounts --clearall ;logrotate -vf /etc/logrotate.conf; sleep 10s; logrotate -vf /etc/logrotate.conf; find /var/log/domlogs -maxdepth 1 -size +1M -exec truncate -s 1k {} + ; find /tmp -printf "%u %s\n" 2>/dev/null |perl -lane '$user{$F[0]} += $F[1]; END { printf "%.02fM $_\n", $user{$_}/1024/1024 for sort { $user{$a} <=> $user{$b} } keys %user }' ; find /tmp -name 'magick*' -delete ; find /tmp -name 'sess_*' -delete ; service zabbix-agent restart ; df -lh

du -hx --max-depth=8 /|grep [0-9]G
du -xh /var/ |grep '^\S*[0-9\.]\+G'|sort -rn
du -xh --max-depth=1 --exclude="fake" |sort -rh
find . -path ./fake -prune -o -type f -size +300M -exec ls -lh {} \; 2>/dev/null |awk '{print $5, $9, $10,$11,$12}' |sort -h
find /var/cpanel/horde/tmp/ -name impatt\* -delete
find /var -size +100M -exec ls {} + > /ramdisk/clear.txt
find /var/log/domlogs -maxdepth 1 -size +10M -exec truncate -s 5M {} +
find  -type f -size +10M | xargs truncate --size 1M
screen -ls | grep -e 'c1' -e 'cho'| awk '{print $1}' | xargs -I % -t screen -X -S % quit ; find /ramdisk | grep -e '.txt' -e 'clear.txt' | xargs rm -f ; service zabbix-agent restart; df -lh| grep /var

find /var/lib/puppet/clientbucket/* -type f -mtime +30 -atime +30 -delete -print   ### Clearing Puppet Logs

ln -s /homeX/user/mailman_archives/fdsfsd.mbox/ /usr/local/cpanel/3rdparty/mailman/archives/private/
tmpwatch --mtime --all 744 /usr/local/cpanel/3rdparty/mailman/archives/private/@listname_clientdomain@/attachments  ### Clearing Mailman archives
ln -s 
##########################
#####   TMP Alerts   #####
##########################
find /tmp -name 'magick*' -delete ; find /tmp -name 'sess_*' -delete ; service zabbix-agent restart ;sleep 10s ; service zabbix-agent restart;  df -lh| grep /tmp

####################################################
##### Backup resize & Backup Not run/Post log  #####
####################################################
ssh -i /admin/hgbackupdir/backupkey root@'df -h | grep backup | head -1 | cut -d : -f1' 
df -h |  egrep "(100%|9[0-9]%)"
vgs ; pvs
exportfs -a ; maint status
screen -S resize
df -h| grep   
ps aux | grep 
/opt/eig_linux/bin/resize_volume -p ###SRVpartion### -s 0.2
service zabbix-agent restart ; df -h| grep /backup  

ps faux|grep backup|awk '{print $2}' | xargs kill -9
backuphelper reseed // backuphelper reset_queue

##############################
##### Inode/Quota Alerts #####
##############################

repquota -a| grep user
setquota -u user  ### Both used fro set inode/Disk quota	
edquota -u user
quota -suv user 

find  /var/cpanel/php/sessions/ea-*/ -name sess\* -mtime +10 -delete 
cat /usr/local/eig_zabbix/tmp/zabbix_inode_abuse

@@@@@@@@@@@@@@@@@@@@@@@@@@
@@			@@
@@    SERVICE ALERTS	@@
@@@@@@@@@@@@@@@@@@@@@@@@@@


======================================================================
======================================================================

baremetal boxes
----------------
box7, box8

clou boxes
----------------
box 3,4

find out instances  >>  virsh list --all
reset 		    >>  virsh reset instance_id


+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

https://www.redhat.com/en/engage/do101-introduction-openshift-s-202004060642
http://free.aicte-india.org/
https://smyl.es/complete-full-list-of-cpanel-scripts-under-the-scripts-directory/
https://www.thecpaneladmin.com/safely-removing-virtfs-on-a-cpanel-server/


==============================================================================================================
==============================================================================================================
==============================================================================================================
---
