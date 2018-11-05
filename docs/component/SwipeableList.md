---
id: SwipableList
title: 滑动listItem
sidebar_label: 滑动listItem
---

## 滑动ListItem
SwipableList是可以滑动打开和关闭的ListItem。处理默认的本机行为，例如在打开其他行时关闭行。

<img src="https://raw.githubusercontent.com/GeekyAnts/NativeBase-KitchenSink/v2.6.1/screenshots/ios/list-swipe-multiple.gif" width=256 height=500 />

句法
```js
import React, { Component } from 'react';
import { ListView } from 'react-native';
import { Container, Header, Content, Button, Icon, List, ListItem, Text } from 'native-base';
const datas = [
  'Simon Mignolet',
  'Nathaniel Clyne',
  'Dejan Lovren',
  'Mama Sakho',
  'Alberto Moreno',
  'Emre Can',
  'Joe Allen',
  'Phil Coutinho',
];
export default class SwipeableListExample extends Component {
  constructor(props) {
    super(props);
    this.ds = new ListView.DataSource({ rowHasChanged: (r1, r2) => r1 !== r2 });
    this.state = {
      basic: true,
      listViewData: datas,
    };
  }
  deleteRow(secId, rowId, rowMap) {
    rowMap[`${secId}${rowId}`].props.closeRow();
    const newData = [...this.state.listViewData];
    newData.splice(rowId, 1);
    this.setState({ listViewData: newData });
  }
  render() {
    const ds = new ListView.DataSource({ rowHasChanged: (r1, r2) => r1 !== r2 });
    return (
      <Container>
        <Header />
        <Content>
          <List
            leftOpenValue={75}
            rightOpenValue={-75}
            dataSource={this.ds.cloneWithRows(this.state.listViewData)}
            renderRow={data =>
              <ListItem>
                <Text> {data} </Text>
              </ListItem>}
            renderLeftHiddenRow={data =>
              <Button full onPress={() => alert(data)}>
                <Icon active name="information-circle" />
              </Button>}
            renderRightHiddenRow={(data, secId, rowId, rowMap) =>
              <Button full danger onPress={_ => this.deleteRow(secId, rowId, rowMap)}>
                <Icon active name="trash" />
              </Button>}
          />
        </Content>
      </Container>
    );
  }
}
```
__属性:__

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
dataSource	| -	| user defined object	| data chunks to render iteratively
renderRow	| -	| Function| 	Callback which takes a chunk of data from dataSource and returns as a body component, which is visible.
renderLeftHiddenRow	| -	| Function	| Callback which takes a chunk of data from dataSource and returns as a left component, which is hidden.
renderRighHiddenRow	| -	| Function	| Callback which takes a chunk of data from dataSource and returns as a right component, which is hidden.
leftOpenValue	| -	| number	| TranslateX value for opening the row to the left (Positive Value)
rightOpenValue	| -	| number	| TranslateX value for opening the row to the right (Negative Value)
closeOnRowBeginSwipe	| false	| boolean	| Open row be closed as soon as a row begin to swipe open swipeToOpenPercent	50%	%	Swipe percent of left/right component's width to trigger the row opening
disableLeftSwipe	| false	| boolean	| Disable ability to swipe the row left
disableRightSwipe	| false	| boolean	| Disable ability to swipe the row right
onRowOpen, onRowClose	| -	| Function	| Callback function which triggers when a swipe row is animating open/close
onRowDidOpen, onRowDidClose	| -	| Function	| Callback function which triggers when a swipe row has animated open/close

## SwipeRow

Single Swipable ListItem（外部列表）

<img src="https://raw.githubusercontent.com/GeekyAnts/NativeBase-KitchenSink/v2.6.1/screenshots/ios/list-swipe-single-row.gif" width=256 height=500 />

句法
```js
import React, { Component } from 'react';
import { Container, Header, Content, SwipeRow, View, Text, Icon, Button } from 'native-base';
​export default class SwipeRowExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content scrollEnabled={false}>
          <SwipeRow
            leftOpenValue={75}
            rightOpenValue={-75}
            left={
              <Button success onPress={() => alert('Add')}>
                <Icon active name="add" />
              </Button>
            }
            body={
              <View>
                <Text>SwipeRow Body Text</Text>
              </View>
            }
            right={
              <Button danger onPress={() => alert('Trash')}>
                <Icon active name="trash" />
              </Button>
            }
          />
        </Content>
      </Container>
    );
  }
}
```
__属性:__

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
body	| -	| -	| Native Base or React Native component(Visible Component).
left	| -	| -	| Native Base or React Native component(Left hidden Component).
right	| -	| -	| Native Base or React Native component(Right hidden Component).
leftOpenValue	| -	| number	| TranslateX value for opening the row to the left (Positive Value)
rightOpenValue	| -	| number	| TranslateX value for opening the row to the right (Negative Value)
stopLeftSwipe	| -	| number	| TranslateX value to stop the row to the swipe left (Positive number)
stopRightSwipe	| -	| number	| TranslateX value to stop the row to the swipe left (Negative number)
swipeToOpenPercent	| 50%	| %	| Swipe percent of left/right component's width to trigger the row opening
disableLeftSwipe	| false| 	boolean	| Disable ability to swipe the row left
disableRightSwipe	| false	| boolean	| Disable ability to swipe the row right
onRowOpen, onRowClose	| -	| Function	| Callback function which triggers when a swipe row is animating open/close
style	| -	| style | object	| Style body