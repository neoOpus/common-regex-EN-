<div align="center">
  <p><img src="http://openlogos.org/logos/sage.jpg" /></p>
  <img src="https://img.shields.io/badge/branch-master-brightgreen.svg">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg">
  <img src="https://jaywcjlove.github.io/sb/lang/chinese.svg">
</div>

## Table of contents

- [E-mail](#e-mail)
- [Phone Number](#phone-number)
- [Domain Name](#domain-name)
- [IP](#ip)
- [Account verification](#account-verification)
- [Character verification](#characters-verification)
  - [Chinese characters](#chinese-characters)
  - [English characters and numbers](#English-characters-and-numbers)
  - [All characters from 3 to 20 in length](#all-characters-from-3-to-20-in-length)
  - [English characters](#english-characters)
    - [String consisting of 26 letters of the alphabet](#string-consisting-of-26-letters-of-the-alphabet)
    - [String consisting of 26 uppercase letters](#string-consisting-of-26-uppercase-letters)
    - [String consisting of 26 lowercase letters](#string-consisting-of-26-lowercase-letters)
    - [由数字和26个英文字母组成的字符串](#由数字和26个英文字母组成的字符串)
    - [由数字、26个英文字母或者下划线组成的字符串](#由数字26个英文字母或者下划线组成的字符串)
  - [中文、英文、数字包括下划线](#中文英文数字包括下划线)
  - [中文、英文、数字但不包括下划线等符号](#中文英文数字但不包括下划线等符号)
  - [禁止输入含有^%&',;=?$\"等字符](#禁止输入含有等字符)
  - [禁止输入含有~的字符](#禁止输入含有的字符)
- [数字正则](#数字正则)
  - [整数](#整数)
    - [正整数](#正整数)
    - [负整数](#负整数)
    - [非负整数](#非负整数)
    - [非正整数](#非正整数)
  - [浮点数](#浮点数)
    - [正浮点数](#正浮点数)
    - [负浮点数](#负浮点数)
    - [非负浮点数](#非负浮点数)
    - [非正浮点数](#非正浮点数)

## E-mail

`gaozihang-001@gmail.com` Only letters, numbers, underscores, periods, and underscores are allowed

```regex
^[a-zA-Z0-9_-]+@[a-zA-Z0-9_-]+(\.[a-zA-Z0-9_-]+)+$
```

![email](images/email.png)

`高子航001Abc@bowbee.com.cn` The name allows Chinese characters, letters and numbers, and the domain name only allows English domain names

```regex
^[A-Za-z0-9\u4e00-\u9fa5]+@[a-zA-Z0-9_-]+(\.[a-zA-Z0-9_-]+)+$
```

![email](images/email2.png)

## Phone Number

`13012345678` mobile phone number

```regex
^1(3|4|5|6|7|8|9)\d{9}$
```

![phone](images/phone.png)

`XXX-XXXXXXX` `XXXX-XXXXXXXX` landline phone number

```regex
(\(\d{3,4}\)|\d{3,4}-|\s)?\d{8}
```

![email](images/phone2.png)

## Domaine Name

`https://google.com/`

```regex
^((http:\/\/)|(https:\/\/))?([a-zA-Z0-9]([a-zA-Z0-9\-]{0,61}[a-zA-Z0-9])?\.)+[a-zA-Z]{2,6}(\/)
```

![domain-name](images/domain-name.png)

## IP

`127.0.0.1`

```regex
((?:(?:25[0-5]|2[0-4]\d|[01]?\d?\d)\.){3}(?:25[0-5]|2[0-4]\d|[01]?\d?\d))
```

![ip](images/ip.png)

## Account verification

`gaozihang_001` Start with a letter, allow 5-16 bytes, allow alphanumeric underscore

```regex
^[a-zA-Z][a-zA-Z0-9_]{4,15}$
```

![user](images/userid.png)

## Character verification

### Chinese characters

`高子航`

```regex
^[\u4e00-\u9fa5]{0,}$
```

![chinese](images/chineses.png)

### English characters and numbers

```regex
^[A-Za-z0-9]+$
```

![char](images/char1.png)

### All characters from 3 to 20 in length

```regex
^.{3,20}$
```

![char](images/char2.png)

### English characters

#### String consisting of 26 letters of the alphabet

```regex
^[A-Za-z]+$
```

![char](images/char3.png)

#### String consisting of 26 uppercase letters

```regex
^[A-Z]+$
```

![char](images/char4.png)

#### String consisting of 26 uppercase letters

```regex
^[a-z]+$
```

![char](images/char5.png)

#### 由数字和26个英文字母组成的字符串

```regex
^[A-Za-z0-9]+$
```

![char](images/char6.png)

#### 由数字、26个英文字母或者下划线组成的字符串 

```regex
^\w+$
```

![char](images/char7.png)

### 中文、英文、数字包括下划线

```regex
^[\u4E00-\u9FA5A-Za-z0-9_]+$
```

![char](images/char8.png)

### 中文、英文、数字但不包括下划线等符号

```regex
^[\u4E00-\u9FA5A-Za-z0-9]+$
```

![char](images/char9.png)

### 禁止输入含有%&',;=?$\"等字符

```regex
[^%&',;=?$\x22]+
```

![char](images/char10.png)

### 禁止输入含有~的字符

```regex
[^~\x22]+
```

![char](images/char11.png)

## 数字正则

### 整数

```regex
^-?[1-9]\d*$
```

![num](images/num1.png)

#### 正整数

```regex
^[1-9]\d*$
```

![num](images/num2.png)

#### 负整数

```regex
^-[1-9]\d*$
```

![num](images/num3.png)

#### 非负整数

```regex
^[1-9]\d*|0$
```

![num](images/num4.png)

#### 非正整数

```regex
^-[1-9]\d*|0$
```

![num](images/num5.png)

### 浮点数

```regex
^-?([1-9]\d*\.\d*|0\.\d*[1-9]\d*|0?\.0+|0)$
```

![num](images/num6.png)

#### 正浮点数

```regex
^[1-9]\d*\.\d*|0\.\d*[1-9]\d*$
```

![num](images/num7.png)

#### 负浮点数

```regex
^-([1-9]\d*\.\d*|0\.\d*[1-9]\d*)$
```

![num](images/num8.png)

#### 非负浮点数

```regex
^[1-9]\d*\.\d*|0\.\d*[1-9]\d*|0?\.0+|0$
```

![num](images/num9.png)

#### 非正浮点数

```regex
^(-([1-9]\d*\.\d*|0\.\d*[1-9]\d*))|0?\.0+|0$
```

![num](images/num10.png)

## License

MIT License. See the [LICENSE](LICENSE) file.

**[⬆ top](#目录)**
