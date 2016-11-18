# LC_*

## Priority

``LC_ALL`` > ``LC_*`` > ``LANG``

## LC_* Default

* Debian Series

  ```shell
  /etc/default/locale
  ```

* Redhat Series

  ```shell
  /etc/sysconfig/i18n
  ```

## LC_ALL

```shell
$ locale
LANG=en_US.UTF-8
LANGUAGE=en_US
LC_CTYPE="en_US.UTF-8"
LC_NUMERIC=zh_CN.UTF-8
LC_TIME=zh_CN.UTF-8
LC_COLLATE="en_US.UTF-8"
LC_MONETARY=zh_CN.UTF-8
LC_MESSAGES="en_US.UTF-8"
LC_PAPER=zh_CN.UTF-8
LC_NAME=zh_CN.UTF-8
LC_ADDRESS=zh_CN.UTF-8
LC_TELEPHONE=zh_CN.UTF-8
LC_MEASUREMENT=zh_CN.UTF-8
LC_IDENTIFICATION=zh_CN.UTF-8
LC_ALL=
$ export LC_ALL='C'
$ locale
LANG=en_US.UTF-8
LANGUAGE=en_US
LC_CTYPE="C"
LC_NUMERIC="C"
LC_TIME="C"
LC_COLLATE="C"
LC_MONETARY="C"
LC_MESSAGES="C"
LC_PAPER="C"
LC_NAME="C"
LC_ADDRESS="C"
LC_TELEPHONE="C"
LC_MEASUREMENT="C"
LC_IDENTIFICATION="C"
LC_ALL=C
```

## locales

```shell
/usr/share/i18n/locales
```

## References

[1] jcubic@Unix.StackExchange, [What does “LC_ALL=C” do?](http://unix.stackexchange.com/questions/87745/what-does-lc-all-c-do)