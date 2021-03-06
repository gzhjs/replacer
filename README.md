### replacer
一个字符替换器。可以批量处理所有指定文件中的字符。比如，你想把所有文件里的一些特殊字符处理掉，可以试试它。

### 安装
用npm: `npm install char-replacer --save-dev`

用yarn: `yarn add char-replacer --dev`

### 使用

```
var replacer = require('replacer');
var config = {
    src: './src',
    dest: './dest',
    '<': '&lt;'
};
replacer(config);
```

关于config:

- src是源路径，可指定单个文件，也可指定一批文件，当然通配符也是可以的，比如'./src/test.txt'、'./src'、'./src/*'。
- dest是目标路径，可指定单个文件，也可指定一批文件，当然通配符也是可以的，比如'./dest/test.txt'、'./dest'、'./dest/*'。默认值取config.src，此时源文件将会被替换掉，这可能并不是你想要的结果，所以请务必指定dest。
