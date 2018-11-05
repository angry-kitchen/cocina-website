---
id: Spinner
title: 加载器
sidebar_label: 加载器
---

## Spinner 加载器
如果您的应用程序的某些屏幕需要一些时间来加载，您可能需要考虑页面加载器。页面加载器是一种任何类型的动画，可以直观地向访问者传达页面正在加载并且只能坐下几秒钟。如果没有页面加载器，用户可能会认为应用程序没有响应，只是沮丧地点击即可。页面加载器也提供了一个小的分心，实际上可以使等待看起来更短。

<img src="https://raw.githubusercontent.com/GeekyAnts/NativeBase-KitchenSink/v2.6.1/screenshots/ios/spinner.gif" width=256 height=500 />

句法
```js
import React, { Component } from 'react';
import { Container, Header, Content, Spinner } from 'native-base';
export default class SpinnerExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Spinner />
          <Spinner color='red' />
          <Spinner color='green' />
          <Spinner color='blue' />
        </Content>
      </Container>
    );
  }
}
```