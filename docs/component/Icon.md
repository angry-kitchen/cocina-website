---
id: Icon
title: 图标
sidebar_label: 图标
---

## Icon 图标
由NativeBase驱动的完美，清晰，高清图标和像素理想字体，这是一个回购列表，列出了可用react-native-vector-icons图标系列的图标

- [点击查看更多图标](https://oblador.github.io/react-native-vector-icons/)

<img src="https://raw.githubusercontent.com/GeekyAnts/NativeBase-KitchenSink/v2.6.1/screenshots/ios/icons.png" width=256 height=500 />

句法
```js
import React, { Component } from 'react';
import { Container, Header, Content, Icon } from 'native-base';
export default class IconExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Icon name='home' />
          <Icon ios='ios-menu' android="md-menu" style={{fontSize: 20, color: 'red'}}/>
          <Icon type="FontAwesome" name="home" />
        </Content>
      </Container>
    );
  }
}
```
- Icon 可以采用以下任何两个属性：name，ios，android。
- 如果你想要包含自定义颜色，大小等图标，那么应该进入style。
- NativeBase图标库中的所有图标都是可缩放的矢量图标，可以根据大小，颜色等进行自定义。

__属性:__

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
name	| -	| -	| Name of the icon.
ios	| -	| -	| Name of the icon for iOS devices.
android	| -	| -	| Name of the icon for Android devices.
active	| true	| boolean	| Renders filled icons
color	| black	| user-defined	| Renders icon with defined color.Include this prop within style
fontSize	| 27	| user-defined	| Renders icon with defined icon-size.Include this prop within style
type	| Ionicons	| Ionicons, Entypo, EvilIcons, Feather, FontAwesome, Foundation, MaterialIcons, MaterialCommunityIcons, Octicons,SimpleLineIcons, Zocial	| Specifies icon family from IonIcons
