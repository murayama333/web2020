# 1 Webプログラミング

## 1.1 Webプログラミングとは

TODO
<br>
<br>

---

## 1.2 プログラミング言語

|言語|特徴|
|:--|:--|
|HTML|TODO|
|CSS|TODO|
|JavaScript|TODO|
|Python|TODO|
|PHP|TODO|
|Java|TODO|

---

## 1.3 プログラミングを始める前に

+ ファイルとフォルダ
+ GUIとCUI
+ テキストエディタ


---

## 1.4 プログラミング

### hello.html

```html
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    h3 {
      color: #123456;
      background-color: #efefef;
      border-bottom: 5px solid #123456 ;  
      padding: 10px;
      margin: 0;
    }
    button {
      width: 100px;
      height: 40px;
    }
    div {
      margin-top: 20px;
    }
  </style>
  <script>
    function hello() {
      document.querySelector("h3").innerHTML = "Hello";
    }

    function world() {
      document.querySelector("h3").innerHTML = "World";
    }
  </script>
</head>
<body>
  <h3>Click button.</h3>
  <div>
    <button onclick="hello()">Hello</button>
    <button onclick="world()">World</button>  
  </div>
</body>
</html>
```

<img src="img/01.png" width="700px">
