# HTML/CSS

## 1. HTML

### 構文

``` html
<tagname attribute="value">Contents</tagname>
```

* `<タグ名 属性名="属性値">`
* 開始タグと終了タグで囲む
* 属性値は `""` で囲む

### 1.1 文書構造を定義するタグ

|タグ|意味|
|:--|:--|
|h1|見出し|
|p|段落|
|img|画像|
|ul, li|箇条書き（リスト）|
|table, tr, th, td|表（テーブル）|
|hr|水平線|
|pre|フォーマット済みテキスト|

### 演習1 (page1.html)

``` html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page 1</title>
</head>
<body>
  <h3>GAFA</h3>
  <hr>
  <ul>
    <li><a href="https://google.com">Google</a></li>
    <li><a href="https://apple.com">Apple</a></li>
    <li><a href="https://facebook.com">Facebook</a></li>
    <li><a href="https://amazon.com">Amazon</a></li>
  </ul>
</body>
</html>
```

---

### 1.2 入力フォームを定義するタグ

|タグ|意味|
|:--|:--|
|form|入力フォーム|
|input|入力部品|
|textarea|テキストエリア|
|select, option|セレクトボックス|

### 演習2 (page2.html)

``` html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page 2</title>
</head>
<body>
  <h3>Search</h3>
  <hr>
  <form action="https://www.google.com/search" method="get">
    <input type="text" name="q">
    <input type="submit" value="search">
  </form>
</body>
</html>
```

---

### 1.3 汎用的なタグ

|タグ|意味|
|:--|:--|
|div|汎用的に使うタグ（ブロック要素）|
|span|汎用的に使うタグ（インライン要素）|

### 演習3 (page3.html)

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page 3</title>
</head>
<body>
  <div>
    <div>1 - A</div>
    <div>1 - B</div>
    <div>1 - C</div>
  </div>
  <div>
    <div>2 - A</div>
    <div>2 - B</div>
    <div>2 - C</div>
  </div>  
</body>
</html>
```

### 演習4 (page4.html)

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page 4</title>
</head>
<body>
  <h3></h3>
  <p>
    Programming is <span>the process of designing</span> and building executable computer programs.
  </p>
</body>
</html>
```

---

## 2. CSS

### 構文

```css
selector {
  property1: value1,
  property2: value2,
  property3: value1,
}
```

* 何を（selector）、どうする（property & value）
* tag selector, id selector, class selector
* component, layout

---

### 2.1 指定方法

* インラインスタイルシート
* 内部スタイルシート
* 外部スタイルシート

### 演習 (page5.html)

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page 5</title>
</head>
<body>
  <h3>GAFA</h3>
  <hr>
  <ul>
    <li><a href="https://google.com">Google</a></li>
    <li><a href="https://apple.com">Apple</a></li>
    <li><a href="https://facebook.com">Facebook</a></li>
    <li><a href="https://amazon.com">Amazon</a></li>
  </ul>
</body>
</html>
```

### 演習 (style.css)

```css
h3 {
  color: #123456;
  background-color: #efefef;
  border-bottom: 5px solid #123456 ;
  padding: 10px;
  margin: 0;
}
```

---

### 2.2 セレクター

* タグセレクター
* idセレクター
* classセレクター

### 演習 (page6.html)

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page 6</title>
  <style>
    li {
      border: 1px solid #ddd;
      padding: 10px 0 10px 10px;
      margin-bottom: 10px;
      box-shadow: 4px 4px rgba(0,0,0,0.3);
      list-style: none;
      transition: all 300ms 0s ease;
    }
    .my-class-a {
      font-size: 1.2rem;
    }
    #my-id-4 {
      background-color: #eee;
    }
  </style>
</head>
<body>
  <h3>GAFA</h3>
  <ul>
    <li id="my-id-1"><a href="https://google.com">Google</a></li>
    <li id="my-id-2" class="my-class-a"><a href="https://apple.com">Apple</a></li>
    <li id="my-id-3"><a href="https://facebook.com">Facebook</a></li>
    <li id="my-id-4" class="my-class-a"><a href="https://amazon.com">Amazon</a></li>
  </ul>
</body>
</html>
```


---

### 2.3 レイアウトとコンポーネント

* レイアウト
* コンポーネント

### 演習 (page7.html)

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page 7</title>
  <style>
    div {
      border: 1px solid grey;
    }

    .row {
      display: flex;
    }
    
    .row div {
      flex: 1;
    }
  </style>
</head>
<body>
  <div class="row">
    <div>1 - A</div>
    <div>1 - B</div>
    <div>1 - C</div>
  </div>
  <div class="row">
    <div>2 - A</div>
    <div>2 - B</div>
    <div>2 - C</div>
  </div>  
</body>
</html>
```

