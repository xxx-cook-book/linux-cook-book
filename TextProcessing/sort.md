# sort

## Default Order 

*** WARNING *** The locale specified by the environment affects sort order.  Set LC_ALL=C to get the traditional sort order that uses native byte values.

* ``LC_ALL=''`` 

  ```shell
  $ echo $LC_ALL

  $ ls | sort
  Desktop
  Documents
  Downloads
  examples.desktop
  Music
  Pictures
  Public
  Templates
  Videos
  ```

* ``LC_ALL=C`` 

  ```shell
  $ echo $LC_ALL

  $ LC_ALL=C ls | sort
  Desktop
  Documents
  Downloads
  Music
  Pictures
  Public
  Templates
  Videos
  examples.desktop
  ```
  or
  ```shell
  $ export LC_ALL=C
  $ echo $LC_ALL
  C
  $ ls | sort
  Desktop
  Documents
  Downloads
  Music
  Pictures
  Public
  Templates
  Videos
  examples.desktop
  ```

* Recommend

  * ``vim ~/.bashrc``

    ```shell
    alias sort='LC_ALL=C sort'
    ```

  * ``source ~/.bashrc``

## Redirect

-o, --output=FILE
　　write result to FILE instead of standard output

* ``>``

  ```shell
  $ cat sort.txt 
  Desktop
  Documents
  Downloads
  Music
  Pictures
  Public
  Templates
  Videos
  examples.desktop
  $ sort sort.txt -f > sort2.txt
  $ cat sort2.txt 
  Desktop
  Documents
  Downloads
  examples.desktop
  Music
  Pictures
  Public
  Templates
  Videos
  ```

* ``> sort.txt``

  ```shell
  $ sort sort.txt -f > sort.txt
  $ cat sort.txt
  ```

* ``-o sort.txt``

  ```shell
  $ sort sort.txt -f > sort.txt
  $ cat sort.txt 
  $ sort sort2.txt > sort.txt
  $ cat sort.txt             
  Desktop
  Documents
  Downloads
  Music
  Pictures
  Public
  Templates
  Videos
  examples.desktop
  $ sort sort.txt -f -o sort.txt
  $ cat sort.txt
  Desktop
  Documents
  Downloads
  examples.desktop
  Music
  Pictures
  Public
  Templates
  Videos
  ```

## References