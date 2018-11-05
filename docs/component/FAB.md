---
id: FAB
title: 浮动按钮
sidebar_label: 浮动按钮
---

## FAB 浮动按钮
FAB（浮动动作按钮）用于特殊类型的提升动作。它们的特征在于在UI上方浮动的带圆圈的图标处于固定位置并具有特殊的运动行为。单击时，它可能包含更多相关操作。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/FAB-single.gif" width=256 height=500 />

句法
```js
import React, { Component } from 'react';
import { Container, Header, View, Button, Icon, Fab } from 'native-base';
export default class FABExample extends Component {
  constructor() {
    this.state = {
      active: 'true'
    };
  }
  render() {
    return (  
      <Container>
        <Header />
        <View style={{ flex: 1 }}>
          <Fab
            active={this.state.active}
            direction="up"
            containerStyle={{ }}
            style={{ backgroundColor: '#5067FF' }}
            position="bottomRight"
            onPress={() => this.setState({ active: !this.state.active })}>
            <Icon name="share" />
            <Button style={{ backgroundColor: '#34A34F' }}>
              <Icon name="logo-whatsapp" />
            </Button>
            <Button style={{ backgroundColor: '#3B5998' }}>
              <Icon name="logo-facebook" />
            </Button>
            <Button disabled style={{ backgroundColor: '#DD5144' }}>
              <Icon name="mail" />
            </Button>
          </Fab>
        </View>
      </Container>
    );
  }
}
```
__属性:__

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
active	| true	| boolean	| Toggle status of FAB
direction	| up	| up, down, left, right	| Direction of buttons that popup on click of FAB
position	| bottomRight	| topLeft, topRight bottomLeft, bottomRight | Position of FAB on screen
containerStyle	| -	| user-defined	| Padding options to render FAB

## 多个浮动按钮

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/FAB-multiple.gif" width=256 height=500 />

句法
```js
import React, { Component } from 'react';
import { Container, Header, View, Fab, Button, Icon } from 'native-base';
​export default class FABMultipleExample extends Component {
  constructor() {
    this.state = {
      active: 'true'
    };
  }
  render() {
    return (
      <Container>
        <Header />
        <View style={{ flex: 1 }}>
          <Fab
            active={this.state.active}
            direction="up"
            containerStyle={{ }}
            style={{ backgroundColor: '#5067FF' }}
            position="bottomRight"
            onPress={() => this.setState({ active: !this.state.active })}>
              ....
            </Fab>
          <Fab direction="left" position="topRight">
            ....
          </Fab>
          <Fab direction="down" position="topLeft">
            ....
          </Fab>
          <Fab direction="right" position="bottomLeft">
            ....
          </Fab>
        </View>
      </Container>
    );
  }
}
```
> 建议把FAB放在`<Container/>`中,而不是`<Content/>`中，因为它是一个`<ScrollView/>`的实现