# Insufficient Disk Space

## Useful Commands

* df

  ```shell
  df -h
  ```

* du

  ```shell
  sudo du -sh
  sudo du -lh --max-depth=1
  sudo du -sh * | grep G | sort -nr
  ```
  * If not use ``sudo``, will see lots of ``du: cannot read directory `xxx': Permission denied``

* lsof

  ```shell
  lsof | grep deleted
  ```

## Recomend Commands

* tune2fs

  ```shell
  sudo tune2fs -m 1 /dev/sda7
  ```

## References