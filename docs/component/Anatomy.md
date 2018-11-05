---
id: Anatomy
title: 结构
sidebar_label: 结构
---

## 结构

使用NativeBase屏幕结构的常用方法是在`<Container>`包含所有组件
- `<Container>`由三个组成部分：`<Header>`，`<Content>`和`<Footer>`。
一般用法：
```js
import React, { Component } from 'react';
import { Container, Header, Title, Content, Footer, FooterTab, Button, Left, Right, Body, Icon, Text } from 'native-base';
export default class AnatomyExample extends Component {
  render() {
    return (
      <Container>
        <Header>
          <Left>
            <Button transparent>
              <Icon name='menu' />
            </Button>
          </Left>
          <Body>
            <Title>Header</Title>
          </Body>
          <Right />
        </Header>
        <Content>
          <Text>
            This is Content Section
          </Text>
        </Content>
        <Footer>
          <FooterTab>
            <Button full>
              <Text>Footer</Text>
            </Button>
          </FooterTab>
        </Footer>
      </Container>
    );
  }
}
```
<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/anatomy.png" width=256 height=500 />


__属性:__

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
Header	| -	| -	| Renders as Header (navbar) of your screen.Input values: Button, Title (Text).
Content	| -	| -	| Represents the main content of your screen.There can be only one <Content> component in a screen.
Footer	| -	| -	| Renders as Footer of your screen.Input values: FooterTab