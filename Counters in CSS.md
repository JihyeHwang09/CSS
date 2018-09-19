```html
<!DOCTYPE html>
<html lang="ko-KR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Counters in CSS</title>
    <link rel="stylesheet" href="css counter.css" type="text/css">
</head>
<body>
    <h1>Counters in CSS:</h1>
    <h2>Operating Systems</h2>
    <h3>Windows</h3>
    <h3>Macintosh</h3>
    <h3>Linux</h3>
</body>
</html>
```

```css
body{
    counter-reset: myCounter mySecondCounter 40;
}
h3:before{
    counter-increment: myCounter mySecondCounter -10;
    content: "OS No. "counter(myCounter)". ";
    color: blue;
    font-size: 12px;
    font-style: italic;
}

h3:after{
    content: "" counter(mySecondCounter);
    color: red;
    vertical-align: super;
    font-size: 10pt;
}
```
![counters in css](C:\Users\raye0\Desktop\마크다운 문서에 넣을 이미지\counters in css.png “css 카운터 예제”) 
