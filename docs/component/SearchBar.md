---
id: SearchBar
title: 搜索栏
sidebar_label: 搜索栏
---

## SearchBar搜索栏
它在互联网上很常见 - 如果我们无法在网站上找到我们想要的东西，我们就会求助于搜索。搜索框一直是任何应用程序的重要组成部分。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/searchbar.png" width=256 height=500 />

句法
```js
import React, { Component } from 'react';
import { Container, Header, Item, Input, Icon, Button, Text } from 'native-base';
export default class SearchBarExample extends Component {
  render() {
    return (
      <Container>
        <Header searchBar rounded>
          <Item>
            <Icon name="ios-search" />
            <Input placeholder="Search" />
            <Icon name="ios-people" />
          </Item>
          <Button transparent>
            <Text>Search</Text>
          </Button>
        </Header>
      </Container>
    );
  }
}
```

__属性:__

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
rounded	| regular	| -	| Wraps the search bar with predefined border options.
