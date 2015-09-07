# gulp-template
gulpのよく使うやつ集めたテンプレート

## 構造
```
├─ dest	  // コンパイル先ディレクトリ
│
├─ gulp   // gulpファイル
│   ├── config.js  // パス等設定ファイル
│   ├── tasks      // 実行されるタスク
│   └── util
│
├─ node_modules
│
└─ src    // 開発用ディレクトリ
    ├── img    // そのままdest/imgへコピーされる
    ├── js     // main.jsをコンパイルしてdestへ
    └── sass   // sassファイルをコンパイルしてdestへ
```

### ビルドツール  

* Gulp              （ タスクランナー )
* gulp-ejs          （ ejs -> html コンパイル )
* gulp-ruby-sass    （ sass -> css コンパイル )
* browserify        （ jsファイルを統合 )
* js-hint           （ jsファイルのチェック )
* BrowserSync       （ ローカルサーバーを起動 )
* gulp.spritesmith  （ スプライト画像を作成 )


## インストール

npm install する

```
$ cd [プロジェクのディレクトリネーム]
$ npm i
```
　
## 実行


### sprite画像を作成
```
$ gulp sprite
```

### gulp起動
BrowserSyncでサーバーを起動し、sass, ejs, jsファイルをwatchする

```
$ gulp
```

## 変えるとこ
#### gulpのパス設定
gulp/config.js
```
└─ gulp
   └── config.js  // 設定ファイル
```
コンパイルに用いる各ディレクトリパス, autoprefixerに用いるブラウザバージョンを変える

#### jquery, normalize.css のバージョンを最新に
