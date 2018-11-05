---
id: Button
title: 按钮
sidebar_label: 按钮
---

## Button 按钮

`Button`是一个纯`NativeBase`组件。按钮是应用程序的组成部分。它们用于各种目的，例如，提交或重置表单，导航，执行交互式操作，例如在点击按钮时在应用中显示或隐藏某些内容等。

> 注意：始终从带有按钮的`NativeBase`导入和使用Text

句法
```js
import React, { Component } from 'react';
import { Container, Header, Content, Button, Text } from 'native-base';
export default class ButtonExample extends Component {
    render() {
        return (
        <Container>
            <Header />
            <Content>
            <Button>
                <Text>Click Me!</Text>
            </Button>
            </Content>
        </Container>
        );
    }
}
```

__属性:__

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
active       | -             | boolean      | 按钮状态
transparent	 |true           | boolean	    | 是否透明
bordered	 |-	             |-	            | 应用 outline 按钮样式
rounded	|-	|-	|呈现略微圆边的按钮
block	|-	|-	|块级按钮
full	|-	|-	|全宽按钮
disabled	|true	|boolean	|不能点击
small	|-	|-	|小按钮
large	|-	|-	|大按钮
iconRight	|-	|-	|图标的右填充
iconLeft	|-	|-	|图标的左边填充
light	|-	|boolean	|按钮的浅白色背景颜色
primary	|-	|boolean	|按钮的蓝色背景颜色
success	|-	|boolean	|按钮的绿色背景颜色
info	|-	|boolean	|按钮的浅绿色背景颜色
warning	|-	|boolean	|按钮的黄色背景颜色
danger	|-	|boolean	|按钮的红色背景颜色
dark	|-	|boolean	|按钮的黑色背景颜色

## 按钮主题

NativeBase提供多种颜色的按钮。

NativeBase提供以下颜色主题：

- `Primary (default)`
- `Success`
- `Info`
- `Warning`
- `Danger`
- `Light`
- `Dark`

<img src="https://raw.githubusercontent.com/GeekyAnts/NativeBase-KitchenSink/v2.6.1/screenshots/ios/buttons.png" width=256 height=500 />

## 透明按钮 Transparent Button
transparent将呈现没有边框且没有背景颜色的按钮。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/button-transparent.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Content, Button, Text } from 'native-base';
export default class ButtonTransparentExample extends Component {
    render() {
        return (
            <Container>
                <Header />
                <Content>
                <Button transparent light>
                    <Text>Light</Text>
                </Button>
                <Button transparent>
                    <Text>Primary</Text>
                </Button>
                <Button transparent success>
                    <Text>Success</Text>
                </Button>
                <Button transparent info>
                    <Text>Info</Text>
                </Button>
                <Button transparent warning>
                    <Text>Warning</Text>
                </Button>
                <Button transparent danger>
                    <Text>Danger</Text>
                </Button>
                <Button transparent dark>
                    <Text>Dark</Text>
                </Button>
                </Content>
            </Container>
        );
    }
}
```

## 轮廓按钮 Outline Button
Outline轮廓按钮样式

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/button-outline.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Content, Button, Text } from 'native-base';
export default class ButtonOutlineExample extends Component {
    render() {
        return (
            <Container>
                <Header />
                <Content>
                <Button bordered light>
                    <Text>Light</Text>
                </Button>
                <Button bordered>
                    <Text>Primary</Text>
                </Button>
                <Button bordered success>
                    <Text>Success</Text>
                </Button>
                <Button bordered info>
                    <Text>Info</Text>
                </Button>
                <Button bordered warning>
                    <Text>Warning</Text>
                </Button>
                <Button bordered danger>
                    <Text>Danger</Text>
                </Button>
                <Button bordered dark>
                    <Text>Dark</Text>
                </Button>
                </Content>
            </Container>
        );
    }
}
```

## 圆形按钮 Rounded Button
圆形按钮样式

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/button-rounded.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Content, Button, Text } from 'native-base';
export default class ButtonRoundedExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Button rounded light>
            <Text>Light</Text>
          </Button>
          <Button rounded>
            <Text>Primary</Text>
          </Button>
          <Button rounded success>
            <Text>Success</Text>
          </Button>
          <Button rounded info>
            <Text>Info</Text>
          </Button>
          <Button rounded warning>
            <Text>Warning</Text>
          </Button>
          <Button rounded danger>
            <Text>Danger</Text>
          </Button>
          <Button rounded dark>
            <Text>Dark</Text>
          </Button>
        </Content>
      </Container>
    );
  }
}
```

## 块状按钮 Block Button
块状按钮样式

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/button-block.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Content, Button, Text } from 'native-base';
export default class ButtonBlockExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Button block light>
            <Text>Light</Text>
          </Button>
          <Button block>
            <Text>Primary</Text>
          </Button>
          <Button block success>
            <Text>Success</Text>
          </Button>
          <Button block info>
            <Text>Info</Text>
          </Button>
          <Button block warning>
            <Text>Warning</Text>
          </Button>
          <Button block danger>
            <Text>Danger</Text>
          </Button>
          <Button block dark>
            <Text>Dark</Text>
          </Button>
        </Content>
      </Container>
    );
  }
}
```

## 全按钮 Full Button
全按钮样式

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/button-full.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Content, Button, Text } from 'native-base';
export default class ButtonFullExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Button full light>
            <Text>Light</Text>
          </Button>
          <Button full>
            <Text>Primary</Text>
          </Button>
          <Button full success>
            <Text>Success</Text>
          </Button>
          <Button full info>
            <Text>Info</Text>
          </Button>
          <Button full warning>
            <Text>Warning</Text>
          </Button>
          <Button full danger>
            <Text>Danger</Text>
          </Button>
          <Button full dark>
            <Text>Dark</Text>
          </Button>
        </Content>
      </Container>
    );
  }
}
```

## 图标按钮 Icon Button
图标按钮样式

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/button-icon.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Content, Button, Icon, Text } from 'native-base';
export default class ButtonIconExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Button iconLeft light>
            <Icon name='arrow-back' />
            <Text>Back</Text>
          </Button>
          <Button iconRight light>
            <Text>Next</Text>
            <Icon name='arrow-forward' />
          </Button>
          <Button iconLeft>
            <Icon name='home' />
            <Text>Home</Text>
          </Button>
          <Button iconLeft transparent primary>
            <Icon name='beer' />
            <Text>Pub</Text>
          </Button>
          <Button iconLeft dark>
            <Icon name='cog' />
            <Text>Settings</Text>
          </Button>
        </Content>
      </Container>
    );
  }
}
```

## 按钮大小 Button Size
small：适用于小尺寸按钮。
large：适用于大尺寸按钮。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/button-size.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Content, Button, Text } from 'native-base';
export default class ButtonSizeExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          //Small size button
          <Button small primary>
            <Text>Default Small</Text>
          </Button>
          //Regular size button
          <Button success>
            <Text>Success Default</Text>
          </Button>
          //Large size button
          <Button large dark>
            <Text>Dark Large</Text>
          </Button>
        </Content>
      </Container>
    );
  }
}
```


## 禁用按钮 Disabled Button
禁用的按钮无法使用且无法点击

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/button-disabled.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Content, Button, Text, Icon } from 'native-base';
export default class ButtonDisabledExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Button disabled>
              <Text>Default</Text>
            </Button>
            <Button disabled bordered>
              <Text>Outline</Text>
            </Button>
            <Button disabled rounded>
              <Text>Rounded</Text>
            </Button>
            <Button disabled large>
              <Text>Custom</Text>
            </Button>
            <Button disabled iconRight>
              <Text>Icon Button</Text>
              <Icon name="home" />
            </Button>
            <Button disabled block>
              <Text>Block</Text>
            </Button>
        </Content>
      </Container>
    );
  }
}

```