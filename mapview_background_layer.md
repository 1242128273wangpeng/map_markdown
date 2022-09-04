## < BackgroundLayer />

###  绘制背景图层

### props

| Prop          | Type     | Default                                | Required | Note          |
|---------------|----------|----------------------------------------|----------|---------------|
| id            | `string` | `none`                                 | `false`  | 样式唯一标识id      |
| sourceID      | `string` | `MapboxGL.StyleSource.DefaultSourceID` | `false`  | 样式源的id        |
| sourceLayerID | `string` | `none`                                 | `false`  | 样式层源的id       |
| aboveLayerID  | `string` | `none`                                 | `false`  | 插入相对样式层上方的id  |
| belowLayerID  | `string` | `none`                                 | `false`  | 插入相对样式层下方的id  |
| layerIndex    | `number` | `none`                                 | `false`  | 插入样式层的index   |
| filter        | `array`  | `none`                                 | `false`  | 样式层的过滤        |
| minZoomLevel  | `number` | `none`                                 | `false`  | 最小的缩放比例       |
| maxZoomLevel  | `number` | `none`                                 | `false`  | 最大的缩放比例       |
| style         | `union`  | `none`                                 | `false`  | 自定义的style样式属性 |

### styles

* <a href="#name">visibility</a><br/>
* <a href="#name-1">backgroundColor</a><br/>
* <a href="#name-2">backgroundOpacity</a><br/>

___

#### Name

`visibility`

#### Description

该样式层是否显示

#### Type

`enum`

#### Default Value

`visible`

#### Supported Values

**visible** -视图被显示<br />
**none** - 试图不被显示<br />

___

#### Name

`backgroundColor`

#### Description

背景的颜色

#### Type

`color`

#### Default Value

`#000000`

#### Name

`backgroundOpacity`

#### Description

背景的透明度0-1

#### Type

`number`

#### Default Value

`1`

