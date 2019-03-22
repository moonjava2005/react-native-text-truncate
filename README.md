# react-native-text-truncate

## Getting started

`$ npm install react-native-text-truncate --save`

Or

`$ yarn add react-native-text-truncate`



## Usage
```javascript
import React,{Component} from 'react';
import TextTruncate from 'react-native-text-truncate';
import {
    Text
} from 'react-native';

export default class ImageViewer extends Component {
    
    render() {
       return(<TextTruncate
                style={{fontSize:16,fontWeight:'200',color:'black'}}
                numberOfLines={5}
                renderExpandor={this.renderExpandor}
                renderCollapsar={this.renderCollapsar}>
                    <Text>
                        {'This page will help you install and build your first React Native app. If you already have React Native installed, you can skip ahead to the Tutorial.If you are coming from a web background, the easiest way to get started with React Native is with Expo tools because they allow you to start a project without installing and configuring Xcode or Android Studio. Expo CLI sets up a development environment on your local machine and you can be writing a React Native app within minutes. For instant development, you can use Snack to try React Native out directly in your web browser.If you are familiar with native development, you will likely want to use React Native CLI. It requires Xcode or Android Studio to get started. If you already have one of these tools installed, you should be able to get up and running within a few minutes. If they are not installed, you should expect to spend about an hour installing and configuring them.'}
                    </Text>
        </TextTruncate>)
    }
    renderExpandor=()=>{
        return(<Text>
            {'Read More'}
        </Text>);
    }
    renderCollapsar=()=>{
            return(<Text>
                {'Read Less'}
            </Text>);
    }
}
```

### Configurable props
* [numberOfLines](#numberOfLines)
* [initExpanded](#initExpanded)
* [expansionDuration](#expansionDuration)
* [collapsionDuration](#collapsionDuration)
* [renderExpandor](#renderExpandor)
* [expandorStyle](#expandorStyle)
* [expandorActiveOpacity](#expandorActiveOpacity)
* [renderCollapsar](#renderCollapsar)

### Event props
* [onExpand](#onExpand)
* [onCollapse](#onCollapse)
* [onExpandorPress](#onExpandorPress)
* [onCollapsarPress](#onCollapsarPress)

### Methods
* [collapse](#collapse)


### Configurable props

#### numberOfLines
Number of lines you want to truncate

#### initExpanded
Init display as full text.
* **false (default)**

#### expansionDuration
Animation duration for expansion.
* **default** - 300

#### collapsionDuration
Animation duration for collapsion.
* **default** - 300

#### renderExpandor
Render expandor when the text is truncated.

#### expandorStyle
Style for expandor container

#### expandorActiveOpacity
Active opacity for expandor container touchable
* **0.8 (default)**

#### renderCollapsar
Render collapsar when the text is fully expanded.

#### collapsarStyle
Style for collapsar container

#### collapsarActiveOpacity
Active opacity for collapsar container touchable
* **0.8 (default)**

#### maximumZoomScale
The maximum zoom level.
* **default** - 3

#### onExpand
Callback function that is called when the text is expanded.

#### onCollapse
Callback function that is called when the text is truncated.

#### onExpandorPress
Callback function that is called when the expandor is pressed.

#### onCollapsarPress
Callback function that is called when the collapsar is pressed.

#### collapse()

Truncated the text.

#### expand()

Display full text.
