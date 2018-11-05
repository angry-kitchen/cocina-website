---
id: Drawer
title: 抽屉滑动
sidebar_label: 抽屉滑动
---

## Drawer 抽屉
抽屉可以是提供导航选项的完美选择。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/drawer.png" width=256 height=500 />

语法：

```js
import React, { Component } from 'react';
import { Drawer } from 'native-base';
import SideBar from './yourPathToSideBar';
export default class DrawerExample extends Component {
  render() {
    closeDrawer = () => {
      this.drawer._root.close()
    };
    openDrawer = () => {
      this.drawer._root.open()
    };
    return (
      <Drawer
        ref={(ref) => { this.drawer = ref; }}
        content={<SideBar navigator={this.navigator} />}
        onClose={() => this.closeDrawer()} >
      // Main View
      </Drawer>
    );
  }
}

```

__属性:__

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
type	| overlay	| -	| type of drawer
tapToClose	| true	| boolean	| Close drawer on tap
openDrawerOffset	| 0.2	| number	| Defines right hand margin when drawer open
panCloseMask	| 0.2	| number	| Defines the screen width for the start of pan close action
closedDrawerOffset	| 0	| number	| Defines left hand margin when drawer closed
tweenHandler	| -	| Function	| Takes in pan ratio that represents the tween percent and returns an object of native props to be set on constituent views
