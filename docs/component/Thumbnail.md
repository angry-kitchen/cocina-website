---
id: Thumbnail
title: 缩略图
sidebar_label: 缩略图
---

缩略图组件与Image非常相似。它可以帮助您展示具有各种尺寸和形状的图像。默认情况下，缩略图呈现圆形图像。
<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/thumbnail.png" width=256 height=500 />

句法
```js
import React, { Component } from 'react';
import { Container, Header, Content, Thumbnail, Text } from 'native-base';
export default class ThumbnailExample extends Component {
  render() {
    const uri = "https://facebook.github.io/react-native/docs/assets/favicon.png";
    return (
      <Container>
        <Header />
        <Content>
          <Text>Square Thumbnail</Text>
          <Thumbnail square small source={{uri: uri}} />
          <Thumbnail square source={{uri: uri}} />
          <Thumbnail square large source={{uri: uri}} />
          <Text>Circular Thumbnail</Text>
          <Thumbnail small source={{uri: uri}} />
          <Thumbnail source={{uri: uri}} />
          <Thumbnail large source={{uri: uri}} />
        </Content>
      </Container>
    );
  }
}
```
> 注意：要具有自定义大小的缩略图，请包括高度和宽度style。

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
source	| -	| -	| Image path for thumbnail.
circle	| true	| -	| Represents shape of thumbnail.By default thumbnail is circle in shape.
square	| -	| -	| Represents shape of thumbnail
small	| -	| -	| Small thumbnail with width and height of 36px
large	| -	| -	| Large thumbnail with width and height of 80px