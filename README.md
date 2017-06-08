# EZproxy database configurations

This repository will store our database stanzas and some of our configuration settings for using EZproxy

We use includes for many of the database stanzas to make editing easier.

## To add additional database stanzas

If the stanza is fairly short and simple, add it to the end of the databases/basic_proxies.cfg file, following the format

```
Title European Mathematical Society
URL http://www.ems-ph.org
HJ http://ems-ph.org
DJ ems-ph.org
```

If you have a longer, more complex stanza, add the entire stanza to a new file in the databases directory and append the line

`IncludeFile databases/[new_file_name]`

At the end of the config.txt file

## Group access

Groups are defined in the user.txt file with the associated authentication scheme.  
Currently we have 6 groups assigned via the patron type.

They are allowed access to databases by Addint a line in the config.txt file such as:

 `Group Faculty+Staff`  

before the databases they are allowed access to
