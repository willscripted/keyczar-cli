`keyczar-cli`
======================

Simple bash wrapper around [KeyczarTool](https://github.com/google/keyczar). KeyczarTool manages your keyczar crypto keys. Its design makes key-rotation a trivial task.

Nothing new or special here. The hosts of this jar seem to have been dismantled. This project provides it and a wrapper that makes it a bit more straightforward for non-java folks.

Install
---------------

1. `mkdir ~/bin`
2. Add `PATH=$PATH:~/bin` to `~/.profile`
3. `cd ~/ && git clone git@github.com:will-ob/keyczar-cli.git`
4. `ln -s ~/keyczar-cli/keyczar ~/bin`


Use
-----------

```
mkdir -p /path/to/project/keyset
cd /path/to/project/keyset

keyczar create --purpose=(sign|crypt)

keyczar addkey [--status=primary]

keyczar promote --version=<version-number>
keyczar demote --version=<version-number>
keyczar revoke --version=<version-number>
```

See [keyczar documentation](http://keyczar.googlecode.com/files/keyczar05b.pdf) for more details on command use.

Caution
-------

This project is provided for development purposes. For production software, one ought to compile this tool from source or verify its checksum (which will fail, because the manifest was modified).

See Also
------------

- [clj-keyczar](https://github.com/circleci/clj-keyczar) clojure keyczar bindings

Thanks
-------------

Thanks much to the Keyczar team for doing all the hard work.

License
----------

Apache 2.0. Same as Keyczar
