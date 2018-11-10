# NKF

## Options

* `--oc=<encoding>`: Specify the output encoding
* `--overwrite[=SUF]`: Preserve timestamp of original files

## Adding and Removing BOM (byte order mark)

nkf-add-bom.sh:

```sh
$ nkf --overwrite --oc=UTF-8-BOM $@
```

nkf-del-bom.sh:

```sh
$ nkf --overwrite --oc=UTF-8 $@
```

