---
id: Ref
title: 关联组件
sidebar_label: 关联组件
---

## Ref关联组件
NativeBase构建于React Native之上。因此，NativeBase的组件各自具有替换React Native元素。
NativeBase现在使开发人员可以轻松地使用ref访问其任何组件，以及相关的React Native元素。
在构建组件之后，您可能会发现自己想要伸出并调用从render（）返回的组件实例上的方法。
这可以通过refs来实现。Refs是向特定子实例发送消息的好方法。
该REF属性需要一个回调函数，该组件被安装或卸载之后立即回调将被执行。

句法
```js
import React, { Component } from 'react';
import { Container, Header, Content, Button } from 'native-base';
export default class RefExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Button ref={ (c) => this._button = c }>
            Click Me
          </Button>
        </Content>
      </Container>
    );
  }
}
```

> this._button 为您提供NativeBase Button的参考。
this._button._root 为您提供NativeBase Button替换React Native元素的引用，即TouchableOpacity。
所有NativeBase组件都可以访问此功能。