# Git

## サブモジュール追加した後に手で削除してまたsubmodule addしようとするとエラーになる

```sh
A git directory for 'xxxx/git' is found locally with remote(s):
  origin        https://github.com/nabetama/xxxx.git
If you want to reuse this local git directory instead of cloning again from
  https://github.com/nabetama/xxxx.git
use the '--force' option. If the local git directory is not the correct repo
or you are unsure what this means choose another name with the '--name' option.
```

## 対応
1. .gitmodulesから対象のモジュールを削除
1. .git/configの対象モジュールを削除
1. .git/modules/以下のsubmoduleでとってきたリポジトリを削除

