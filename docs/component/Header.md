---
id: Header
title: 顶部栏
sidebar_label: 顶部栏
---

## Header 顶部栏
为屏幕呈现为标题（导航栏）

__属性:__

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
Left	| -	| -	| Components render to the left in Header
Body	| -	| -	| Components render at the center of Header
Right	| -	| -	| Components render to the right in Header
iosBarStyle	| -	| light-content, dark-content, default	| Set iOS barStyle
androidStatusBarColor	| -	| -	| Set background color for status bar in android
noShadow	| -	| boolean	| Removes elevation from android
searchBar	| -	| boolean	| Add searchbar to header or not
rounded	| -	| boolean	| Make header searchbar rounded
hasSubtitle	| -	| boolean	| Add subtitle to header
hasSegment	| -	| boolean	| Add segments to header
hasTabs	| -	| boolean	| Add tabs to header
hasText	| -	| boolean	| This is button prop. Adds necessary padding when Text button defined in Left / Right of Header (iOS)
noLeft	| -	| boolean	| Eliminates Left component and moves Title towards left (Android)
span	| -	| boolean	| Doubles the header size

## 只有标题的导航

<img src="https://raw.githubusercontent.com/GeekyAnts/NativeBase-KitchenSink/v2.6.1/screenshots/ios/header-with-title.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Left, Body, Right, Title } from 'native-base';
export default class HeaderTitleExample extends Component {
  render() {
    return (
      <Container>
        <Header>
          <Left/>
          <Body>
            <Title>Header</Title>
          </Body>
          <Right />
        </Header>
      </Container>
    );
  }
}

```

## 标题和副标题的导航

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/header-with-title-and-subtitle.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Left, Body, Right, Title, Subtitle } from 'native-base';
export default class HeaderTitleSubtitleExample extends Component {
  render() {
    return (
      <Container>
        <Header>
          <Left />
          <Body>
            <Title>Title</Title>
            <Subtitle>Subtitle</Subtitle>
          </Body>
          <Right />
        </Header>
      </Container>
    );
  }
}
```

## 带图标按钮的导航

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/header-with-icons.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Left, Body, Right, Button, Icon, Title } from 'native-base';
export default class HeaderIconExample extends Component {
  render() {
    return (
      <Container>
        <Header>
          <Left>
            <Button transparent>
              <Icon name='arrow-back' />
            </Button>
          </Left>
          <Body>
            <Title>Header</Title>
          </Body>
          <Right>
            <Button transparent>
              <Icon name='menu' />
            </Button>
          </Right>
        </Header>
      </Container>
    );
  }
}
```

## 带有文本按钮的导航

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/header-with-text-button.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Left, Body, Right, Button, Title, Text } from 'native-base';
export default class HeaderTextExample extends Component {
  render() {
    return (
      <Container>
        <Header>
          <Left>
            <Button hasText transparent>
              <Text>Back</Text>
            </Button>
          </Left>
          <Body>
            <Title>Header</Title>
          </Body>
          <Right>
            <Button hasText transparent>
              <Text>Cancel</Text>
            </Button>
          </Right>
        </Header>
      </Container>
    );
  }
}
```
## 带有图标按钮和文本按钮的导航

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/header-with-icon-button-text-button.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Left, Body, Right, Button, Icon, Title, Text } from 'native-base';
export default class HeaderIconButtonTextButtonExample extends Component {
  render() {
    return (
      <Container>
        <Header>
          <Left>
            <Button transparent>
              <Icon name='arrow-back' />
            </Button>
          </Left>
          <Body>
            <Title>Header</Title>
          </Body>
          <Right>
            <Button transparent>
              <Text>Cancel</Text>
            </Button>
          </Right>
        </Header>
      </Container>
    );
  }
}
```

## 带有图标和文本按钮的导航

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/header-with-icon-text-button.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Left, Body, Right, Button, Icon, Title, Text } from 'native-base';
export default class HeaderIconTextButtonExample extends Component {
  render() {
    return (
      <Container>
        <Header>
          <Left>
            <Button transparent>
              <Icon name='arrow-back' />
              <Text>Back</Text>
            </Button>
          </Left>
          <Body>
            <Title>Header</Title>
          </Body>
          <Right>
            <Button transparent>
              <Text>Cancel</Text>
            </Button>
          </Right>
        </Header>
      </Container>
    );
  }
}
```

## 带有多个图标按钮的导航

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/header-with-multiple-icon-button.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Left, Body, Right, Button, Icon, Title } from 'native-base';
export default class HeaderMultipleIconExample extends Component {
  render() {
    return (
      <Container>
        <Header>
          <Left>
            <Button transparent>
              <Icon name='arrow-back' />
            </Button>
          </Left>
          <Body>
            <Title>Header</Title>
          </Body>
          <Right>
            <Button transparent>
              <Icon name='search' />
            </Button>
            <Button transparent>
              <Icon name='heart' />
            </Button>
            <Button transparent>
              <Icon name='more' />
            </Button>
          </Right>
        </Header>
      </Container>
    );
  }
}
```
## 标题跨度

<img src="https://raw.githubusercontent.com/GeekyAnts/NativeBase-KitchenSink/v2.6.1/screenshots/ios/header-span.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from "react";
import { Container, Header, Title, Button, Icon, Left, Right, Body } from "native-base";
export default class HeaderSpan extends Component {
  render() {
    return (
      <Container>
        <Header span>
          <Left>
            <Button transparent>
              <Icon name="arrow-back" />
            </Button>
          </Left>
          <Body>
            <Title>Header Span</Title>
          </Body>
          <Right />
        </Header>
      </Container>
    );
  }
}
```

## 标题去除阴影

<img src="https://raw.githubusercontent.com/GeekyAnts/NativeBase-KitchenSink/v2.6.1/screenshots/ios/header-noshadow.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from "react";
import { Container, Header, Title, Button, Icon, Left, Right, Body } from "native-base";
export default class HeaderNoShadow extends Component {
  render() {
    return (
      <Container>
        <Header noShadow>
          <Left>
            <Button transparent>
              <Icon name="arrow-back" />
            </Button>
          </Left>
          <Body>
            <Title>Header No Shadow</Title>
          </Body>
          <Right>
            <Button transparent>
              <Icon name="menu" />
            </Button>
          </Right>
        </Header>
      </Container>
    );
  }
}
```

## 标题透明

<img src="https://raw.githubusercontent.com/GeekyAnts/NativeBase-KitchenSink/v2.6.1/screenshots/ios/header-transparent.png" width=256 height=500 />

代码示例：

```js
import React, { Component } from "react";
import { Container, Header, Title, Content, Button, Icon, Left, Body, Text } from "native-base";
export default class HeaderTransparent extends Component {
  render() {
    return (
      <Container style={{backgroundColor: "#87cefa"}}>
        <Header transparent>
          <Left>
            <Button transparent>
              <Icon name="arrow-back" />
            </Button>
          </Left>
          <Body>
            <Title>Transparent</Title>
          </Body>
          <Right>
            <Button transparent>
              <Text>Cancel</Text>
            </Button>
          </Right>
        </Header>
        <Content padder>
          <Text>
            Header with transparent prop
          </Text>
        </Content>
      </Container>
    );
  }
}
```