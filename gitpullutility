#/usr/bin/bash

path=/path/to/repositories
GREEN='\033[0;32m'
NC='\033[0m'

eval "$(ssh-agent -s)"
ssh-add ~/.ssh/specified_key

for i in $path/*
do
  cd $i
  txt=$(basename $i)
  echo -e "${GREEN}Updating $txt${NC}"
  git pull
  git gc --auto
done
