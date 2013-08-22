#!/bin/bash

dir(){
X=`ls -l ~/$1 | awk '{print $5}' | awk '{total = total + $1}END{print total}'`;
if [ -z $X ];
  then
  echo "Empty";

elif [ $X -ge 1 -a $X -le 999 ];
  then
  echo "$X B";

elif [ $X -ge 1000 -a $X -le 999999 ];
  then
  X=$(awk -v X=$X 'BEGIN { print ((X) / 1000) }');
  echo $X | awk '{printf("%.2f", $1)}';
  echo " KB";

elif [ $X -ge 1000000 -a $X -le 999999999 ];
  then
  X=$(awk -v X=$X 'BEGIN { print ((X) / 1000000) }');
  echo $X | awk '{printf("%.2f", $1)}';
  echo " MB";

elif [ $X -ge 1000000000 -a $X -le 999999999999 ];
  then
  X=$(awk -v X=$X 'BEGIN { print ((X) / 1000000000) }');
  echo $X | awk '{printf("%.2f", $1)}';
  echo " GB";

elif [ $X -ge 1000000000000  ];
  then
  X=$(awk -v X=$X 'BEGIN { print ((X) / 1000000000000) }');
  echo $X | awk '{printf("%.2f", $1)}';
  echo " TB";
fi
}
# Add your own directory here `dir Directory`
echo -e "Downloads Directory: \t" `dir Downloads`;
echo -e "Trash Directory: \t\t" `dir \.Trash`;