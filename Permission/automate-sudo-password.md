# Automate Sudo Password

## Options
```shell
-S, --stdin
     Write the prompt to the standard error and read the password from the standard input instead of using the terminal device.
     The password must be followed by a newline character.
```

## Usage
* echo & pipe
    ```shell
    echo pwd | sudo -S service nginx reload
    ```
* yes & pipe
    ```shell
    yes pwd | sudo -S service nginx reload
    ```
* <<EOF
    ```shell
    sudo -S service nginx reload <<EOF
    pwd
    EOF
    ```

## References

[1] Alexander@AskUbuntu, [How to automate sudo password [duplicate]](https://askubuntu.com/questions/452345/how-to-automate-sudo-password)