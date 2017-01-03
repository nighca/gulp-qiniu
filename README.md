# [gulp](http://gulpjs.com)-[qiniu](http://qiniu.com)-upload

Forked from [gulp-qiniu](https://github.com/hfcorriez/gulp-qiniu) & fix bug.

> 上传静态资源到七牛 CDN

## Install

```
npm install gulp-qiniu-upload --save-dev
```

## Usage

实例代码:

```js
const qiniu = require('gulp-qiniu-upload')

gulp.src('./public/**')
  .pipe(qiniu({
    accessKey: "xxxx",
    secretKey: "xxxx",
    bucket: "bucket",
    private: false
  }, {
    dir: 'assets/',
    versioning: true,
    versionFile: './cdn.json',
    concurrent: 10
  }))
```

## License

MIT
