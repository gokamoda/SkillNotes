# Markdownで便利なStyle（CSS）

- [1. 画像中央揃え（Github非対応）](#1-画像中央揃えgithub非対応)
- [2. 画像中央揃え（Github対応）](#2-画像中央揃えgithub対応)

## 1. 画像中央揃え（Github非対応）
```html
<style>
  img{
    margin: 0 auto;
    display: block;
  }
</style>
<img src="xxx.png">
```

## 2. 画像中央揃え（Github対応）
```html
<p align="center">
  <img src="xxx.png">
</p>
```