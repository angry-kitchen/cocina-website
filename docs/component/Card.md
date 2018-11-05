---
id: Card
title: 卡片
sidebar_label: 卡片
---

## Card 卡片

Card是一个灵活且可扩展的内容容器。它包括页眉和页脚选项，各种内容，上下文背景颜色和强大的显示选项。

__Card属性:__

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
transparent	| -	| -	| Removes card shadow from iOS and elevation from android
dataArray	| Array	| user-defined array	| Array of data chunks to render iteratively.
renderRow	| Function	| -	| Callback which takes a chunk of data from dataArray and returns as a component.

__CardItem属性:__

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
header	| -	| -	| Displays text as header for cards
cardBody	| -	| -	| Defines section for body of card. The child components are rendered with proper spacing and alignment.
footer	| -	| -	| Displays text as footer for cards
button	| -	| -	| To navigate on click of a card item.
bordered	| false	| boolean	| Adds border to the cardItems
first	| -	| -	| First CardItem, use in case of custom Card BorderRadius
last	| -	| -	| Last CardItem, use in case of custom Card BorderRadius

## Card 头部 and 尾部
<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/card-header-and-footer.png" width=256 height=500 />

> 要在卡中添加可选的页眉和/或页脚，请在header/中添加/ footerprop CardItem。
卡头：header在卡内包含CardItem第一个实例的道具。
卡片页脚：footer在卡片中包含最后一个CardItem实例的道具。

```js
import React, { Component } from 'react';
import { Container, Header, Content, Card, CardItem, Text, Body } from 'native-base';
export default class CardHeaderFooterExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Card>
            <CardItem header>
              <Text>NativeBase</Text>
            </CardItem>
            <CardItem>
              <Body>
                <Text>
                  //Your text here
                </Text>
              </Body>
            </CardItem>
            <CardItem footer>
              <Text>GeekyAnts</Text>
            </CardItem>
         </Card>
        </Content>
      </Container>
    );
  }
}
```

## CardItem边框
<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/card-bordered.png" width=256 height=500 />

> 包含bordered<CardItem>的道具，以便为卡片项目设置borderBottom。

```js
import React, { Component } from 'react';
import React, { Component } from "react";
import { Container, Header, Content, Card, CardItem, Text, Body } from "native-base";
export default class CardItemBordered extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content padder>
          <Card>
            <CardItem header bordered>
              <Text>NativeBase</Text>
            </CardItem>
            <CardItem bordered>
              <Body>
                <Text>
                  NativeBase is a free and open source framework that enable
                  developers to build
                  high-quality mobile apps using React Native iOS and Android
                  apps
                  with a fusion of ES6.
                </Text>
              </Body>
            </CardItem>
            <CardItem footer bordered>
              <Text>GeekyAnts</Text>
            </CardItem>
          </Card>
        </Content>
      </Container>
    );
  }
}
```

## CardItem按钮
<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/card-button.gif" width=256 height=500 />

> button使用<CardItem> 包含prop以使用卡项目实现onClick功能。

```js
import React, { Component } from "react";
import { Container, Header, Content, Card, CardItem, Text, Body } from "native-base";
export default class CardItemButton extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content padder>
          <Card>
            <CardItem header button onPress={() => alert("This is Card Header")}>
              <Text>NativeBase</Text>
            </CardItem>
            <CardItem button onPress={() => alert("This is Card Body")}>
              <Body>
                <Text>
                  Click on any carditem
                </Text>
              </Body>
            </CardItem>
            <CardItem footer button onPress={() => alert("This is Card Footer")}>
              <Text>GeekyAnts</Text>
            </CardItem>
          </Card>
        </Content>
      </Container>
    );
  }
}
```

## 透明卡
<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/card-transparent.png" width=256 height=500 />

> 可以使用transparent带有<CardItem>的道具创建透明卡。

```js
import React, { Component } from "react";
import { Container, Header, Content, Card, CardItem, Text, Body } from "native-base";
export default class CardTransparentExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content padder>
          <Card transparent>
            <CardItem>
              <Body>
                <Text>
                  This is just a transparent card with some text to boot.
                </Text>
              </Body>
            </CardItem>
          </Card>
        </Content>
      </Container>
    );
  }
}
```

## 卡片列表
<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/card-list.png" width=256 height=500 />

> CardItem随后包括在内Card创建一张带有列表的卡片。

```js
import React, { Component } from 'react';
import { Container, Header, Content, Card, CardItem, Text, Icon, Right } from 'native-base';
export default class CardListExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Card>
            <CardItem>
              <Icon active name="logo-googleplus" />
              <Text>Google Plus</Text>
              <Right>
                <Icon name="arrow-forward" />
              </Right>
             </CardItem>
           </Card>
        </Content>
      </Container>
    );
  }
}
```
## 卡片图片
<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/card-image.png" width=256 height=500 />

> 想要通过卡片列表获得更多信息吗？
包括与图像CardItem内Card以及一些文本之前和之后的图像来创建列表卡。
这是你的卡片图像准备好了！

```js
import React, { Component } from 'react';
import { Image } from 'react-native';
import { Container, Header, Content, Card, CardItem, Thumbnail, Text, Button, Icon, Left, Body, Right } from 'native-base';
export default class CardImageExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Card>
            <CardItem>
              <Left>
                <Thumbnail source={{uri: 'Image URL'}} />
                <Body>
                  <Text>NativeBase</Text>
                  <Text note>GeekyAnts</Text>
                </Body>
              </Left>
            </CardItem>
            <CardItem cardBody>
              <Image source={{uri: 'Image URL'}} style={{height: 200, width: null, flex: 1}}/>
            </CardItem>
            <CardItem>
              <Left>
                <Button transparent>
                  <Icon active name="thumbs-up" />
                  <Text>12 Likes</Text>
                </Button>
              </Left>
              <Body>
                <Button transparent>
                  <Icon active name="chatbubbles" />
                  <Text>4 Comments</Text>
                </Button>
              </Body>
              <Right>
                <Text>11h ago</Text>
              </Right>
            </CardItem>
          </Card>
        </Content>
      </Container>
    );
  }
}
```

## 卡展示
<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/card-showcase.png" width=256 height=500 />

> Card Showcase是Card Image的进一步定制。它使用了几个不同的项目。
从卡列表组件开始，类似于我们的列表头像。
使用Left，Body和Right组件来对齐Card标头的内容。
要将Image与单个CardItem中的其他NativeBase组件混合，请在Body组件中包含内容。

```js
import React, { Component } from 'react';
import { Image } from 'react-native';
import { Container, Header, Content, Card, CardItem, Thumbnail, Text, Button, Icon, Left, Body } from 'native-base';
export default class CardShowcaseExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Card style={{flex: 0}}>
            <CardItem>
              <Left>
                <Thumbnail source={{uri: 'Image URL'}} />
                <Body>
                  <Text>NativeBase</Text>
                  <Text note>April 15, 2016</Text>
                </Body>
              </Left>
            </CardItem>
            <CardItem>
              <Body>
                <Image source={{uri: 'Image URL'}} style={{height: 200, width: 200, flex: 1}}/>
                <Text>
                  //Your text here
                </Text>
              </Body>
            </CardItem>
            <CardItem>
              <Left>
                <Button transparent textStyle={{color: '#87838B'}}>
                  <Icon name="logo-github" />
                  <Text>1,926 stars</Text>
                </Button>
              </Left>
            </CardItem>
          </Card>
        </Content>
      </Container>
    );
  }
}
```
