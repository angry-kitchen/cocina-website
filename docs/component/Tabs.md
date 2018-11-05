---
id: tabs
title: 页卡
sidebar_label: 页卡
---

## tabs

选项卡是按钮或链接的水平区域，允许在屏幕之间提供一致的导航体验。它可以包含文本和图标的任意组合，是一种支持移动导航的流行方法。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/tabs-basic.gif" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Content, Tab, Tabs } from 'native-base';
import Tab1 from './tabOne';
import Tab2 from './tabTwo';
import Tab3 from './tabThree';
​export default class TabsExample extends Component {
  render() {
    return (
      <Container>
        <Header hasTabs />
        <Tabs>
          <Tab heading="Tab1">
            <Tab1 />
          </Tab>
          <Tab heading="Tab2">
            <Tab2 />
          </Tab>
          <Tab heading="Tab3">
            <Tab3 />
          </Tab>
        </Tabs>
      </Container>
    );
  }
}
```

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
locked	| false	| boolean	| Disable swipe
initialPage	| -	| integer	| Set default active tab
page	| -	| -	| Set selected tab
tabBarPosition	| top	| top, bottom, overlayTop, overlayBottom	| Set position of Tabs
tabBarUnderlineStyle	| -	| -	| Style of the default tab bar's underline
onChangeTab	| Function	| -	| Function to call when tab changes
onScroll	| Function	| -	| Function to call when pages are sliding

> 已知问题：ScrollableTab标题仅接受字符串时，尚不支持自定义tabHeading 。
专业提示：建议hasTabs在使用标签时使用标头和标题

## 高级选项卡
<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/tabs-advanced.gif" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Tab, Tabs, TabHeading, Icon, Text } from 'native-base';
import Tab1 from './tabOne';
import Tab2 from './tabTwo';
import Tab3 from './tabThree';
​export default class TabsAdvancedExample extends Component {
  render() {
    return (
      <Container>
        <Header hasTabs/>
        <Tabs>
          <Tab heading={ <TabHeading><Icon name="camera" /><Text>Camera</Text></TabHeading>}>
            <Tab1 />
          </Tab>
          <Tab heading={ <TabHeading><Text>No Icon</Text></TabHeading>}>
            <Tab2 />
          </Tab>
          <Tab heading={ <TabHeading><Icon name="apps" /></TabHeading>}>
            <Tab3 />
          </Tab>
        </Tabs>
      </Container>
    );
  }
}
```

## 滚动的tabs
<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/tabs-scrollable.gif" width=256 height=500 />

代码示例：

```js
import React, { Component } from 'react';
import { Container, Header, Tab, Tabs, ScrollableTab } from 'native-base';
import Tab1 from './tabOne';
. . .
import Tab5 from './tabFive';
​export default class TabsScrollableExample extends Component {
  render() {
    return (
      <Container>
        <Header hasTabs/>
        <Tabs renderTabBar={()=> <ScrollableTab />}>
          <Tab heading="Tab1">
            <Tab1 />
          </Tab>
          <Tab heading="Tab2">
            <Tab2 />
          </Tab>
          <Tab heading="Tab3">
            <Tab3 />
          </Tab>
          <Tab heading="Tab4">
            <Tab4 />
          </Tab>
          <Tab heading="Tab5">
            <Tab5 />
          </Tab>
        </Tabs>
      </Container>
    );
  }
}
```

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
heading	| -	| string,	| Label String, or Component
tabStyle	| -	| style object	| Style for tab bar
activeTabStyle	| -	| style object	| Style for active tab bar
textStyle	| -	| style object	| Style for text
activeTextStyle	| -	| style object	| Style for active text

