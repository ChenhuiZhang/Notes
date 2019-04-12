# Find symbol link and replace it with real file
find -L . -maxdepth 1 -xtype l | xargs readlink {} | xargs -i cp --remove-destination {} .


