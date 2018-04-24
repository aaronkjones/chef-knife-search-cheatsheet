# Find all the attributes you can use in search:
knife search node 'name:somenode' -F json | less
Each key value pair can be used in `search`  
For example,
```
"chef_environment": "_default"
```
Can be used like,
```
knife search node 'chef_environment:_default'
```
# Find total number of nodes managed by Chef:
knife search node '*:*' | grep Node\ Name | wc | cut -d ' ' -f6
# Find a node with a node name that begins with "jones":
knife search node 'name:jones*'
# Find all nodes that use Ubuntu:
knife search node 'platform:ubuntu'
# Find all nodes that use Ubuntu 16.04, Xenial:
knife search node 'codename:xenial'
# Find all nodes that use Ubuntu 16.04, Xenial:
knife search node 'platform_version:16.04'