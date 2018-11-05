---
id: Badge
title: 角标
sidebar_label: 角标
---

## Badge 角标
角标是与元素关联的项目的数字指示符。徽章可以通知您有新的或未读的消息或通知。这些可以非常有效地提醒用户应用程序上的新内容。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/badge.png" width=256 height=500 />

```js
import React, { Component } from 'react';
import { Container, Header, Content, Badge, Text, Icon } from 'native-base';
export default class BadgeExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Badge>
            <Text>2</Text>
          </Badge>
          <Badge primary>
            <Text>2</Text>
          </Badge>
          <Badge success>
            <Text>2</Text>
          </Badge>
          <Badge info>
            <Text>2</Text>
          </Badge>
          <Badge warning>
            <Text>2</Text>
          </Badge>
          <Badge danger>
            <Text>2</Text>
          </Badge>
          <Badge primary>
          <Icon name="star" style={{ fontSize: 15, color: "#fff", lineHeight: 20 }}/>
          </Badge>
          <Badge style={{ backgroundColor: 'black' }}>
            <Text style={{ color: 'white' }}>1866</Text>
          </Badge>
        </Content>
      </Container>
    );
  }
}
```
__属性:__

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
primary	| -	| boolean	| Add a blue background color to your component
success	| -	| boolean	| Add a green background color to your component
info	| -	| boolean	| Add a light blue background color to your component as shown
warning	| -	| boolean	| Add a yellow warning background color to your component
danger	| -	| boolean	| Add a red background color to your component
