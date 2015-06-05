`keyczar-cli`
======================

Simple bash wrapper around [KeyczarTool]().

Nothing new or special here. The hosts of this jar seem to have been dismantled. This project provides it and a wrapper that makes it a bit more straightforward for non-java folks.

Install
---------------

```bash
cd /some/install/dir && git clone git@github.com:will-ob/keyczar-cli.git
# cd somewhere in $PATH
ln -s /some/install/dir/keyczar-cli/keyczar
```


Use
-----------

```
cd /path/to/keydir

keyczar create --purpose=(sign|crypt)

keyczar addkey [--status=primary]

keyczar promote --version=<version-number>
keyczar demote --version=<version-number>
keyczar revoke --version=<version-number>
```

See [keyczar documentation](http://keyczar.googlecode.com/files/keyczar05b.pdf) for more details on command use.

Caution
-------

This project is provided for development purposes. I could not locate the source for this project and the jar file does not include it. For production software, one ought to compile this tool from source or verify its checksum.

If you happen to know where to find the jars or the checksum, please open a github issue.

License
----------

Apache 2.0. Same as Keyczar
