# ping-automation-in-bash

#!/bin/bash
read -p "enter the site name" site
ping -c $site | cat>>file.txt
sleep 10s
if [[ $? -eq  0 ]]
then
  echo "successful"
else
  echo "unsuccessful"
fi
