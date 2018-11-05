---
id: Layout布局
title: 布局
sidebar_label: 布局
---

## Layout布局
布局系统是一个必不可少的概念，需要掌握才能创建出色的布局和UI。React Native使用Flexbox创建布局，这在我们需要适应不同屏幕尺寸甚至不同设备的组件和视图时非常有用。Flexbox很棒但对新手来说可能很烦人。

不是很擅长Flexbox？
这里是Easy Grid of NativeBase，Flexbox的包装器。NativeBase中

的布局系统非常强大且灵活。不再担心Flexbox的道具，如alignItems，flexDirection，justifyContent，margin，填充，位置，宽度等。您可以使用我们拥有的所有可用选项创建任何布局。为了构建自定义布局和组件，了解布局在NativeBase中的工作方式并不像Flexbox那么难。
Flexbox使它看起来像百分比，但实际发生的只是比率。在更容易的部分，比率比百分比/小数更容易表示。因此，Easy Grid采用比率代替百分比。
性能方面，Easy Grid值得注意，并且与Flexbox一样好用，计算量不大。
<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/layout.png" width=256 height=500 />

句法
```js
import React, { Component } from 'react';
import { Container, Header } from 'native-base';
import { Col, Row, Grid } from 'react-native-easy-grid';
export default class LayoutExample extends Component {
  render() {
    return (
      <Container>
        <Header />
          <Grid>
            <Col style={{ backgroundColor: '#635DB7', height: 200 }}></Col>
            <Col style={{ backgroundColor: '#00CE9F', height: 200 }}></Col>
          </Grid>
      </Container>
    );
  }
}复制

```
> 注意：如果您<Row />在a内部使用<ScrollView />，组件的高度将根据内容灵活，但您始终可以应用高度样式。
NativeBase <Content>组件使用<ScrollView>。这需要Easy-Grid的元素<Col>和<Row>元素具有定义的高度。
替换Grid，Col，Row的组件：React Native View
