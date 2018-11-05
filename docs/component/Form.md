---
id: Form
title: 表单
sidebar_label: 表单
---

## 表单Form

NativeBase利用它List来设计包含一组相关输入组件的表单。包括NativeBase组件的任意组合以组成表单。
Input是一个构建在React Native之上的NativeBase组件TextInput。用于通过键盘将文本输入应用程序的基础组件。应用特定样式的项目组件包装器。

道具为多个功能提供可配置性，例如自动更正，自动大写，占位符文本和不同的键盘类型，例如数字小键盘。
提供遵循每个平台的样式和交互指南的许多属性，以便用户可以直观地进行交互。

__属性:__

属性     | 默认值       | 选项       | 描述
------------ | ------------- | ------------ | -----------
fixedLabel	| true	| boolean	| Label is fixed to the left of Input and does not hide when text is entered.
floatingLabel	| true	| boolean	| Label that animates upward when input is selected and animates downward when input is erased.
inlineLabel	| -	| boolean	| Label placed to the left of input element and does not hide when text is entered. This can also be used along with placeholder.
stackedLabel	| -	| -	| Places the label on top of input element which appears like a stack. This can also be used along with placeholder.
bordered	| -| 	-	| Includes border with the textbox
rounded	| -	| -	| Includes rounded border with the textbox.
regular	| -	| -	| Includes rectangluar border with the textbox.
underline	| true| 	-	| Includes underline border with the textbox
disabled	| -	| -| 	Disables inputting data
placeholderLabel	| -	| -	| Renders the same way the TextInput does with the form styling of NativeBase
placeholder	| -	| -| 	String that renders before text input is entered
last	| -	| -	| Styles last Item of the Form
error	| -| 	-	| Border color of textbox for invalid input
success	| -	| -	| Border color of textbox for valid input
picker	| -	| -	| Styles picker field with Input

> 注意： NativeBase中的表单只是输入的包装，因此没有任何onSubmit功能。

## 固定标签
该fixedLabel属性创建一个Input组件，其Label固定在Input的左侧，并且在输入文本时不会隐藏。无论标签的长度如何，输入都在同一位置对齐。它也可以与占位符一起使用。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/input-fixed.png" width=256 height=500 />

语法：
```js
import React, { Component } from 'react';
import { Container, Header, Content, Form, Item, Input, Label } from 'native-base';
export default class FixedLabelExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Form>
            <Item fixedLabel>
              <Label>Username</Label>
              <Input />
            </Item>
            <Item fixedLabel last>
              <Label>Password</Label>
              <Input />
            </Item>
          </Form>
        </Content>
      </Container>
    );
  }
}
```

## 内联标签
该inlineLabel属性创建一个Input组件，其Label与Input一致，并且在输入文本时不会隐藏。它也可以与占位符一起使用。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/input-fixed.png" width=256 height=500 />

语法：
```js
import React, { Component } from 'react';
import { Container, Header, Content, Form, Item, Input, Label } from 'native-base';
export default class InlineLabelExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Form>
            <Item inlineLabel>
              <Label>Username</Label>
              <Input />
            </Item>
            <Item inlineLabel last>
              <Label>Password</Label>
              <Input />
            </Item>
          </Form>
        </Content>
      </Container>
    );
  }
}
```

## 浮动标签
该floatingLabel属性创建一个Input组件，其Label在选择输入时向上动画，在擦除输入时向下动画。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/input-floating.gif" width=256 height=500 />

语法：
```js
import React, { Component } from 'react';
import { Container, Header, Content, Form, Item, Input, Label } from 'native-base';
export default class FloatingLabelExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Form>
            <Item floatingLabel>
              <Label>Username</Label>
              <Input />
            </Item>
            <Item floatingLabel last>
              <Label>Password</Label>
              <Input />
            </Item>
          </Form>
        </Content>
      </Container>
    );
  }
}
```

> When using floatingLabel, use getRef to get the reference of `<Input/>` component. Always wrap floatingLabel component with <Form/>

## 堆叠标签
该stackedLabel属性创建一个Input组件，将标签放在input元素的顶部，该元素看起来像一个堆栈。这也可以与占位符一起使用。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/input-stacked.png" width=256 height=500 />

语法：
```js
import React, { Component } from 'react';
import { Container, Header, Content, Form, Item, Input, Label } from 'native-base';
export default class StackedLabelExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Form>
            <Item stackedLabel>
              <Label>Username</Label>
              <Input />
            </Item>
            <Item stackedLabel last>
              <Label>Password</Label>
              <Input />
            </Item>
          </Form>
        </Content>
      </Container>
    );
  }
}
```

## 选择器输入
包含pickerprop <Item>以具有选择器类型的输入字段。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/input-picker.gif" width=256 height=500 />

语法：
```js
import React, { Component } from 'react';
import { Container, Header, Content, Form, Item, Picker } from 'native-base';
export default class PickerInputExample extends Component {
    constructor(props) {
    super(props);
    this.state = {
      selected2: undefined
    };
  }
  onValueChange2(value: string) {
    this.setState({
      selected2: value
    });
  }
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Form>
            <Item picker>
              <Picker
                mode="dropdown"
                iosIcon={<Icon name="ios-arrow-down-outline" />}
                style={{ width: undefined }}
                placeholder="Select your SIM"
                placeholderStyle={{ color: "#bfc6ea" }}
                placeholderIconColor="#007aff"
                selectedValue={this.state.selected2}
                onValueChange={this.onValueChange2.bind(this)}
              >
                <Picker.Item label="Wallet" value="key0" />
                <Picker.Item label="ATM Card" value="key1" />
                <Picker.Item label="Debit Card" value="key2" />
                <Picker.Item label="Credit Card" value="key3" />
                <Picker.Item label="Net Banking" value="key4" />
              </Picker>
            </Item>
          </Form>
        </Content>
      </Container>
    );
  }
}
```


## 常规文本框
要使用形状为矩形的常规文本框，请包含regularprop Item。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/input-regular.png" width=256 height=500 />

语法：
```js
import React, { Component } from 'react';
import { Container, Header, Content, Input, Item } from 'native-base';
export default class RegularTextboxExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Item regular>
            <Input placeholder='Regular Textbox' />
          </Item>
        </Content>
      </Container>
    );
  }
}
```

## 带下划线的文本框
要使用带下划线的文本框，请包含underlineprop Item。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/input-underline.png" width=256 height=500 />

语法：
```js
import React, { Component } from 'react';
import { Container, Header, Content, Item, Input } from 'native-base';
export default class UnderlinedTextboxExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Item>
            <Input placeholder="Underline Textbox" />
          </Item>
        </Content>
      </Container>
    );
  }
}
```

## 圆形文本框
要有一个圆形类型边框的文本框，请包含rounded prop Item。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/input-rounded.png" width=256 height=500 />

语法：
```js
import React, { Component } from 'react';
import { Container, Header, Content, Item, Input } from 'native-base';
export default class RoundedTextboxExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Item rounded>
            <Input placeholder='Rounded Textbox'/>
          </Item>
        </Content>
      </Container>
    );
  }
}
```

## 图标文本框
图标可以轻松添加到NativeBase文本框中。为此，请在其中包含一个图标<Item>。
图标按其定义的顺序呈现Item。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/input-icon.png" width=256 height=500 />

语法：
```js
import React, { Component } from 'react';
import { Container, Header, Content, Item, Input, Icon } from 'native-base';
export default class IconTextboxExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          // Text input box with icon aligned to the left
          <Item>
            <Icon active name='home' />
            <Input placeholder='Icon Textbox'/>
          </Item>
          // Text input box with icon aligned to the right
          <Item>
            <Input placeholder='Icon Alignment in Textbox'/>
            <Icon active name='swap' />
          </Item>
        </Content>
      </Container>
    );
  }
}
```

## 成功输入文本框
要显示包含有效数据的文本框，请包含successprop Item。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/input-success.png" width=256 height=500 />

语法：
```js
import React, { Component } from 'react';
import { Container, Header, Content, Item, Input, Icon } from 'native-base';
export default class SuccessInputTextboxExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Item success>
            <Input placeholder='Textbox with Success Input'/>
            <Icon name='checkmark-circle' />
          </Item>
        </Content>
      </Container>
    );
  }
}
```

## 错误输入文本框
要显示包含无效数据的文本框，请包含errorprop Item。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/input-error.png" width=256 height=500 />

语法：
```js
import React, { Component } from 'react';
import { Container, Header, Content, Item, Input, Icon } from 'native-base';
export default class ErrorInputTextboxExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Item error>
            <Input placeholder='Textbox with Error Input'/>
            <Icon name='close-circle' />
          </Item>
        </Content>
      </Container>
    );
  }
}
```
## 禁用文本框
要限制将数据输入到文本框中，请disabled使用Item和包含prop Input。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/input-disabled.png" width=256 height=500 />

语法：
```js
import React, { Component } from 'react';
import { Container, Header, Content, Item, Input, Icon } from 'native-base';
export default class DisabledTextboxExample extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content>
          <Item disabled>
            <Input disabled placeholder='Disabled Textbox'/>
            <Icon name='information-circle' />
          </Item>
        </Content>
      </Container>
    );
  }
}
```

## 多行文本
要限制将数据输入到文本框中，请disabled使用Item和包含prop Input。

<img src="https://github.com/GeekyAnts/NativeBase-KitchenSink/raw/v2.6.1/screenshots/ios/input-textarea.png" width=256 height=500 />

语法：
```js
import React, { Component } from "react";
import { Container, Header, Content, Textarea, Form } from "native-base";
export default class TextArea extends Component {
  render() {
    return (
      <Container>
        <Header />
        <Content padder>
          <Form>
            <Textarea rowSpan={5} bordered placeholder="Textarea" />
          </Form>
        </Content>
      </Container>
    );
  }
}
```