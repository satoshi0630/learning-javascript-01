# learning-javascript-01

テクノロジー（藤原）JavaScriptの練習 (1)

## Q1の回答「コメントを解除したことで、どう変化しましたか？」

【表示ができるようになった】

## Q2の回答「エラーの原因は何でしょうか？（調べてみましょう）」

【参照エラー：ウィンドウが定義されていません　　と訳せたのでエラーの原因はウィンドウが定義されていないから。】

## Chromeデベロッパーツール：Consoleの実行結果

```
【おはよう！
index.html:56 Live reload enabled.
favicon.ico:1 Failed to load resource: the server responded with a status of 404 (Not Found)
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！
index.html:52 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
socket.onmessage @ index.html:52
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！
index.html:52 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
socket.onmessage @ index.html:52
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！
index.html:1 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！】
```

## ターミナルの実行結果

```
【Last login: Tue Jun 18 09:02:15 on console
takedareishinoMacBook-Pro:~ takedasatoshi$ cd ~/fujiwara
takedareishinoMacBook-Pro:fujiwara takedasatoshi$ git clone git@github.com:satoshi0630/learning-javascript-01.git
Cloning into 'learning-javascript-01'...
remote: Enumerating objects: 10, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (8/8), done.
remote: Total 10 (delta 0), reused 7 (delta 0), pack-reused 0
Receiving objects: 100% (10/10), done.
takedareishinoMacBook-Pro:fujiwara takedasatoshi$ cd learning-javascript-01
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ code .
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ node node-main.js
-bash: node: command not found
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ cat ~/.bash_profile
if [ -f ~/.bashrc ]; then
  . ~/.bashrc
fi
if [ -f ~/.bashrc ]; then
  . ~/.bashrc
fi
if [ -f ~/.bashrc ]; then
  . ~/.bashrc
fi
if [ -f ~/.bashrc ]; then
  . ~/.bashrc
fi
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ curl -L git.io/nodebrew | perl - setup
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
  0     0    0     0    0     0      0      0 --:--:--  0:00:01 --:--:--     0
  0     0    0     0    0     0      0      0 --:--:--  0:00:03 --:--:--     0
100 24634  100 24634    0     0   6874      0  0:00:03  0:00:03 --:--:--  6874
Fetching nodebrew...
Installed nodebrew in $HOME/.nodebrew

========================================
Export a path to nodebrew:

export PATH=$HOME/.nodebrew/current/bin:$PATH
========================================
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ echo "export PATH=$HOME/.nodebrew/current/bin:$PATH" >> ~/.bashrc
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ source ~/.bashrc
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ nodebrew 
nodebrew 1.0.1

Usage:
    nodebrew help                         Show this message
    nodebrew install <version>            Download and install <version> (from binary)
    nodebrew compile <version>            Download and install <version> (from source)
    nodebrew install-binary <version>     Alias of `install` (For backward compatibility)
    nodebrew uninstall <version>          Uninstall <version>
    nodebrew use <version>                Use <version>
    nodebrew list                         List installed versions
    nodebrew ls                           Alias for `list`
    nodebrew ls-remote                    List remote versions
    nodebrew ls-all                       List remote and installed versions
    nodebrew alias <key> <value>          Set alias
    nodebrew unalias <key>                Remove alias
    nodebrew clean <version> | all        Remove source file
    nodebrew selfupdate                   Update nodebrew
    nodebrew migrate-package <version>    Install global NPM packages contained in <version> to current version
    nodebrew exec <version> -- <command>  Execute <command> using specified <version>

Example:
    # install
    nodebrew install v8.9.4

    # use a specific version number
    nodebrew use v8.9.4
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ nodebrew install-binary latest
v12.4.0 is already installed
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ nodebrew ls
v12.4.0

current: v12.4.0
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ nodebrew use latest
use v12.4.0
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ node -v
v12.4.0
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ node node-main.js
/Users/takedasatoshi/Documents/fujiwara/learning-javascript-01/node-main.js:1
window.alert("Hello, Node.js!!");
^

ReferenceError: window is not defined
    at Object.<anonymous> (/Users/takedasatoshi/Documents/fujiwara/learning-javascript-01/node-main.js:1:1)
    at Module._compile (internal/modules/cjs/loader.js:774:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:785:10)
    at Module.load (internal/modules/cjs/loader.js:641:32)
    at Function.Module._load (internal/modules/cjs/loader.js:556:12)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ node node-main.js
/Users/takedasatoshi/Documents/fujiwara/learning-javascript-01/node-main.js:1
window.alert("Hello, Node.js!!");
^

ReferenceError: window is not defined
    at Object.<anonymous> (/Users/takedasatoshi/Documents/fujiwara/learning-javascript-01/node-main.js:1:1)
    at Module._compile (internal/modules/cjs/loader.js:774:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:785:10)
    at Module.load (internal/modules/cjs/loader.js:641:32)
    at Function.Module._load (internal/modules/cjs/loader.js:556:12)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ node node-main.js
Goodmorning, Node.js!!
takedareishinoMacBook-Pro:learning-javascript-01 takedasatoshi$ 
】
```

