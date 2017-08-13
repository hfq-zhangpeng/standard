# 会分期SaaS前端组开发规范

## 命名规范
### 项目命名
采用小写方式，以下划线分割。
例：my_first_project

### 目录命名
采用小写方式，以下划线分割。完整英文命名使用复数，缩写采用单数。
例：scripts,lib,data_modules

### js文件命名
与项目命名规则一致。
例：contract_tmp.js

### css文件命名
与项目命名规则一致。
例：apartment_list.css

### html文件命名
与项目命名规则一致。
例：list_tab.html

## css开发时书写规范
### 命名
使用小写字母，以中划线分割
    .list-tab {
        ...
    }

### 使用tab缩进
    .tab {
        width: 100%;
        height: 100%;
    }

### 每个属性声明末尾添加分号

### 添加空格
属性值前。
选择器'>','+','~'等前后。
'{'前。
'!important'的'!'前。
    .element {
        width: 100%;
        height: 100%;
    }

    .element + div {
        font-size: 16px !important;
    }

### 统一使用双引号

### 其他项
不允许有空的规则。
选择器不要超过4层。
尽量少用'*'选择器。

## JavaScript开发时书写规范
### 变量命名
标准变量采用驼峰式。
'ID','URL'在变量名中全大写。
'Android'在变量名中首字母大写，其他字母小写。
'iOS'在变量名中首字母小写，其他字母大写。
常量全大写，使用下划线链接。
构造函数大写第一个字母。
jquery对象使用'$'开头。

    var thisIsObj;

    var myID, myURL;

    var isAndroid, iOSVersion;

    var MAX_COUNT = 6;

    function Person(name) {
        ...
    }

    var $body = $('body');

### 变量声明
一个函数作用域中所有变量声明提前到函数首部，除了for中使用的一次性变量。
一行定义一个var。
    function doSomethingHandle() {
        var num;
        var value;
        var COUNT = 5;
        for(var i = 0; i < COUNT; i++){
            var something;
            ...
        }
    }

### 函数
声明函数和函数表达式，'('前不要有空格，'{'前一定要有空格。
立即执行函数必须包一层'()'。
参数之间使用','分割，逗号后要有一个空格。
    function doSomething(name, age, sex) {
        ...
    }

    (function() {
        ...
    })();

### 最外层统一使用单引号

### 单行长度
单行长度不超过120。

### 换行
代码块'{'后和'}'前。
定义变量后。

### 空行
代码块后需要空行。

### 其他项
'_'使用表示私有变量。
不允许使用三元运算符嵌套。
不允许使用空的代码块。
函数未被使用时应及时删除。
注释的无用的代码在上线前予以删除。

## git使用规范
1. 对于线上问题紧急修复时，必须从master创建新分支，在新分支修改。不允许在master上直接修改。
2. 创建新分支时，必须从最新版本的master上创建。
3. 提交commit之前，必须更新当前分支。
4. 向master上合并代码时，必须从github web端创建新的pull request。
5. 如果出现冲突，在解决冲突之后需要告知该文件的相关负责人员。

## 项目上线规范
>目前部署方式，和ci部分还未调整完成。所以该部分可能会后期进行修改。

1. 构建正式tag首先更新当前分支，保证当前分支为最新。
2. 上线完成之后，需要将开发分支合并至master上，并且存在其他正在开发分支需要从master上更新代码。


文件命名与书写规范参考[腾讯imweb团队规范](http://imweb.github.io/CodeGuide/#js-variable-declaration)
