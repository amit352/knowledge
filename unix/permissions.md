# permissions
Manage who can do what on the system.

## users
### create user
Either `useradd` or `adduser`
```sh
$ sudo adduser -m <name>   # create user + home dir

# now it's time to make the user the owner of the home dir,
# and set the right permissions for all files within.

$ chown <user>:<user> -R ~/<user>      # recursively change owner
$ chmod 700 /home/<user>               # hide dir from other users
$ chsh -s /usr/local/bin/bash <user>   # change login shell
```
or alternatively:
```sh
$ sudo adduser -m <user>  # does all of the above in a single command except
```

## groups
Groups have combined settings; individual users can be added to groups which
then inherit the permissions of the group.

### create group
```sh
$ groupadd <name>
```

### add user to group
```sh
$ sudo usermod -G <group> <user>
```

## passwords
### edit password
```sh
# opens interactive session
$ sudo passwd <user>
```

## namespaces
[tbi]

## default dir permissions
```sh
$ chmod 07555
```
