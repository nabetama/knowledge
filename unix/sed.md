## macのsedだと -i の振る舞いが違う
macのsedはBSD sedとかいうやつ

```sh
nabetama@localhost ~/Desktop/sed-test
$ cat hoge1.txt                                                                                       [2.0.0-p645]
foo
nabetama@localhost ~/Desktop/sed-test
$ sed -i '' -e 's/foo/bar/' $( ls . | grep .txt$ )                                                   [2.0.0-p645]
nabetama@localhost ~/Desktop/sed-test
$ cat hoge1.txt                                                                                       [2.0.0-p645]
bar
```
