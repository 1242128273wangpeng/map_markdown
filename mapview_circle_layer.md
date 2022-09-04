##  < CircleLayer/>

### 绘制圆形图层

### props

| Prop          | Type     | Default                                | Required | Note          |
|---------------|----------|----------------------------------------|----------|---------------|
| id            | `string` | `none`                                 | `false`  | 样式唯一标识id      |
| sourceID      | `string` | `MapboxGL.StyleSource.DefaultSourceID` | `false`  | 样式源id         |                                                                                                                           |
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
* <a href="#name-1">circleRadius</a><br/>
* <a href="#name-2">circleColor</a><br/>
* <a href="#name-3">circleBlur</a><br/>
* <a href="#name-4">circleOpacity</a><br/>
* <a href="#name-5">circleTranslate</a><br/>
* <a href="#name-6">circleTranslateAnchor</a><br/>
* <a href="#name-7">circlePitchScale</a><br/>
* <a href="#name-8">circlePitchAlignment</a><br/>
* <a href="#name-9">circleStrokeWidth</a><br/>
* <a href="#name-10">circleStrokeColor</a><br/>
* <a href="#name-11">circleStrokeOpacity</a><br/>

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

`circleRadius`

#### Description

圆形的半径

#### Type

`number`

#### Default Value

`5`

#### Units

`pixels`

#### Minimum

`0`
___

#### Name

`circleColor`

#### Description

圆形的填充色

#### Type

`color`

#### Default Value

`#000000`

___

#### Name

`circleOpacity`

#### Description

圆形的透明度

#### Type

`number`

#### Default Value

`1`

#### Minimum

`0`

#### Maximum

`1`

___

#### Name

`circleStrokeWidth`

#### Description

圆形的描边宽度

#### Type

`number`

#### Default Value

`0`

#### Units

`pixels`

#### Minimum

`0`
___

#### Name

`circleStrokeColor`

#### Description

圆形的描边颜色

#### Type

`color`

#### Default Value

`#000000`
___

#### Name

`circleStrokeOpacity`

#### Description

圆形描边的透明度

#### Type

`number`

#### Default Value

`1`

#### Minimum

`0`

#### Maximum

`1`

