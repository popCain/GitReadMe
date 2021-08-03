npm package manage(node_modules)
===

1.node_modules list
---

### *(i).* npm install modules(package.json file base)

|モジュール名|`SSL古いバージョン`|成田バージョン|`SSL新しいバージョン`|最新バージョン(2021/08/03)|
|:---|:---:|:---:|:---:|:---:|
|✅ archiver|1.3.0(keep)|1.3.0|1.3.0|5.3.0|
|✅ async|1.5.2(keep)|1.5.2|1.5.2|3.2.0|
|✅ bignumber|2.0.7(not-exist)|2.0.7|1.1.0|1.1.0|
|✅ cheerio|0.22.0(keep)|0.22.0|0.22.0|1.0.0|
|chokidar|1.7.0(deprecated)|1.7.0|3.5.2|3.5.2|
|✅ connect-flash|0.1.1(keep)|0.1.1|0.1.1|0.1.1|
|✅ cron|1.0.5(keep)|1.0.5|1.0.5|1.8.2|
|✅ crypto-js|3.1.4(keep)|3.1.4|3.1.4|4.1.1|
|⭕ csv|0.4.6(update)|0.4.6|5.5.0|5.5.0|
|✅ deepcopy|0.5.0(keep)|0.5.0|0.5.0|2.1.0|
|🟫 ejs|0.8.4(deprecated)|0.8.4|3.1.6|3.1.6|
|✅ encoding-japanese|1.0.24(keep)|1.0.24|1.0.24|1.0.30|
|🟡 express|3.21.2(keep)|3.3.4|3.21.2|4.17.1|
|☑ express-mysql-session|1.3.0(update)|1.3.0|2.1.6|2.1.6|
|☑ express-session|1.17.1(update)|1.17.1|1.17.2|1.17.2|
|🔴 ~~jade~~|0.34.1(delete)|0.34.1|-|1.11.0|
|🟢 pug|-(new add)|-|3.0.2|3.0.2|
|✅ jconv|0.1.5(keep)|0.1.5|0.1.5|0.1.5|
|⭕ jsrsasign|0.0.3(update)|0.0.3|10.3.0|10.3.0|
|✅ log4js|0.6.26(keep)|0.6.26|0.6.26|6.3.0|
|✅ mysql|2.18.1(keep)|2.18.1|2.18.1|2.18.1|
|✅ opts|1.2.2(keep)|1.2.2|1.2.2|2.0.2|
|✅ passport|0.1.17(keep)|0.1.17|0.1.17|0.4.1|
|✅ passport-local|0.1.6(keep)|0.1.6|0.1.6|1.0.0|
|✅ run-sequence|1.1.0(keep)|1.1.0|1.1.0|2.2.1|
|✅ underscore|1.13.1(keep)|1.13.1|1.13.1|1.13.1|
|🟡 gulp|3.9.0(update)|4.0.2|4.0.2|4.0.2|
|🟤 gulp-concat|2.5.2(deprecated)|2.5.2|2.6.1|2.6.1|
|🔴 ~~gulp-minify-css~~|1.1.1(delete)|1.1.1|-|1.2.4|
|🟢 gulp-clean-css|-(new add)|-|4.3.0|4.3.0|
|☑ gulp-rename|1.2.2(update)|1.2.2|2.0.0|2.0.0|
|🟤 gulp-sourcemaps|1.5.2(deprecated)|1.12.1|3.0.0|3.0.0|
|🟤 gulp-uglify|1.2.0(deprecated)|1.5.4|3.0.2|3.0.2|
|🔴 ~~gulp-uglifyjs~~|0.6.2(delete)|0.6.2|-|0.6.2|

**Note:** 

>  ✅ - 同じバージョンのまま         
>  🔴 - 削除　|　🟢 - 追加                   
>  🟤 - アップデート(内部依存モジュール廃棄の予定)　|　🟫 - アップデート(自分自身廃棄の予定)               
>  ☑ - アップデート(しなくても良い）                  
>  🟡 - 注意(deprecated warning)    
<br>

### *(ii).* copy custom modules(three custom modules)

|bit|narwhal|xmljson|
|:---:|:---:|:---:|
<br>

2.node_modules analysis
---

### *(i)* Deprecated Packages(廃棄予定のパッケージ)

[**[NPMGraph]**](https://npmgraph.js.org/): Site to show dependency graph of npm modules(ex. 'express@3' ).

* express@3.21.2(now) 🟡   
    * connect@2.30.2 (deprecated:x:)
    * mkdirp@0.5.1 (deprecated:x:)    
* gulp@4.0.2(now) 🟡
    * glob-watcher@5.0.5 (latest)
      * chokidar@2.1.8 (deprecated:x:): watch filesystem directories for events - (for win, linux, mac)
         * fsevents@1.2.13 (deprecated:x:) - (for mac)
* gulp-concat@2.5.2     ==:up:==>      @2.6.1 (now) 🟤
    * gulp-util@3.0.8 (deprecated:x:)
* gulp-uglify@1.2.0     ==:up:==>      @3.0.2 (now) 🟤
    * gulp-util@3.0.8 (deprecated:x:)
* gulp-sourcemaps@1.5.2    ==:up:==>      @3.0.0 (now) 🟤
    * natives@1.1.6 (deprecated:x:)
    * urix@0.1.0 (deprecated::x:)
    * resolve-url@0.2.1 (deprecated:x:)
* ejs@0.8.4(deprecated:x:)    ==:up:==>      @3.1.6 (now) 🟫
* jade(delete 🔴)    ==replace==>      pug@3.0.2 🟢
* gulp-minify-css(delete 🔴)  ==replace==>    gulp-clean-css@4.3.0 🟢

### *(ii)* vulnerable package(脆弱なパッケージ)

[**[Vulnerability DB]**](https://snyk.io/vuln?type=npm): Detailed information and remediation guidance for known vulnerabilities.

```bash
npm audit # 
```

* csv@0.4.6 ==:up:==> @5.5.0 ⭕ 
   * resolve 1 vulnerability(High)
* jsrsasign@0.0.3 ==:up:==> @10.3.0(>=8.0.13) ⭕
   * Timing Attack(High)
   * RSA signature validation vulnerability(Critical)

<br>

[[TOPへ]](#npm-package-managenode_modules)
