# LinuxCentOS_system-Network_Guide

#!/bin/bash
IPLIST="path_to_the_Ip_list_file"


for ip in $(cat $IPLIST)

do
   ping -c1 $ip &> /dev/null
   if [ $? -eq 0 ]
   then
   echo $ip ping passed
   else
   echo $ip ping failed
   fi
done
