# MEDIAFLUX

## Useful Aterm commands

```sh
# list document type namespaces
$ asset.doc.namespace.list

# create and describe document type namespaces
$ asset.doc.namespace.create :namespace <ns>
$ asset.namespace.describe :namespace <ns>

# list stores available
$ asset.store.list

# describe stores (places to store files, images, videos, asset content)
$ asset.store.describe :name <storeName>

# retrieve a data asset
$ asset.get :id <id>
$ asset.destroy :id <id>

# list available doc types
$ asset.doc.type.list

# view documentation for doc type (eg. mf-note)
$ asset.doc.type.describe :type <docTypeName>

# the in-file could be a Java inputstream
$ asset.create :namesapce <ns>
                :meta <: mf-note
                        <: note "Hello World" >>
                :in-file <local-path>

# view projects on the server
$ cd projects
$ ls
```

## MF Desktop (web client)
```sh
# use MF Desktop to add elements to doc types
$ asset.doc.type.list :namespace <ns>

# use MF Desktop to create dictionary items
$ dictionary.namespace.create : namesapce <ns>


```

## Export tcl script to install Doc type on another server (dev -> prod)
```sh
$ asset.doc.type.script.create :type <ns:doctype>
                                :out file://path/to/file.tcl

#example                                
$ asset.doc.type.script.create :type myns:people
                                :out file://home/user123/MakePeopleDocType.tcl
```
