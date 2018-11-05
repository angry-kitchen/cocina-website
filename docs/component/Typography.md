---
id: Typography
title: 标题大小
sidebar_label: 标题大小
---

## Typography标题大小
NativeBase为您提供了标题标签，即H1，H2和H3组件。这些标题标记可帮助您确定屏幕内容的优先级。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/typography.png" width=256 height=500 />

句法
```js
import React, { Component } from 'react';
import { Container, Header, Content, H1, H2, H3, Text } from 'native-base';
export default class TypographyExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <H1>Header One</H1>
          <H2>Header Two</H2>
          <H3>Header Three</H3>
          <Text>Default</Text>
        </Content>
      </Container>
    );
  }
}
```
属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
H1	| font-size: 27	| string, number	| Heading tag <H1>
H2	| font-size: 24	| string, number	| Heading tag <H2>
H3	| font-size: 21	| string, number	| Heading tag <H3>
