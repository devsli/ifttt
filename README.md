# IFTTT trigger

Simple CLI trigger for IFTTT Maker

```
$ ./ifttt light_on
No key is provided. Use option `-k` or environment variable IFTTT_KEY to set the key.
You can obtain it here: https://ifttt.com/maker
```

You have to connect your IFTTT account to [IFTTT Maker channel][1] and either
use your key as `-k` option, or save it to your init script:
```
$ ./ifttt -k 123MyDemoKey123 light_on
Congratulations! You've fired the light_on event%
```
```shell
$ grep IFTTT_KEY ~/.bashrc
export IFTTT_KEY="123MyDemoKey123"

$ ./ifttt light_on
Congratulations! You've fired the light_on event%
```

It's possible to use [up to 3][2] custom variables:
```shell
$ ./ifttt -1 "some param" -2 "another one param" -3 "third" light_on
Congratulations! You've fired the light_on event%
```
Values will be accessible with names `Value1`, `Value2` and `Value3`.

[1]: https://ifttt.com/maker
[2]: https://ifttt.com/channels/maker/triggers/1636368624-receive-a-web-request
