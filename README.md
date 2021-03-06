# markdownToHtmlAndNav
>  Output a htmlString(based on [marked](https://github.com/chjj/marked)) and a navString (based on the hierarchical relationship of headers'[h1, h2, h3])

## Install
```
npm install markdown-to-nav
```

## Usage
1. Use with a config file:  
```
mdToNav generate -c md-to-nav-config.js
```
md-to-nav-config.js
```
module.exports = {
    inputAndOutputConf: [
        {
            inputFileName: "./a.md",
            outputContentName: "./output/a.html",
            outputNavName: "./output/a_nav.html",
        },
        {
            inputFileName: "./b.md",
            outputContentName: "./output/b.html",
            outputNavName: "./output/b_nav.html",
        }
    ],
    nav: {
        levelStart: 2,
        levelEnd: 3
    }
}

```
2. Minimal usage：  
```
mdToNav generate  -i input/a.md -o output/content.html -n output/nav.html
```
## Options
```
  .option('-h, --help', 'input:指定输入的MD文件路径, outContent:指定输出的内容.html文件的路径, outNav:指定输出的导航.html文件的路径')
  .option('-i, --input <input>', 'input: Path of the markdown file')
  .option('-o, --outContent <outContent>', 'outContent: Path of the markdownString')
  .option('-n, --outNav <outNav>', 'outNav: Path of the navString')
  .option('-c, --config <config>', 'config: Path of the config file')
```

