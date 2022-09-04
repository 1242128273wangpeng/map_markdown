## < MapView />

### Props

| Prop                        | Type      | Default | Required | Note                                                                                                              |
|-----------------------------|-----------|---------|----------|-------------------------------------------------------------------------------------------------------------------|
| `provider`                  | `string`  | MapBox  | false    | 地图的提供方 (`MapBox`) 后续再支持(`MapKit`,`BaiDu`,`GaoDe`,`GoogleMaps` in iOS and `BaiDu`,`GaoDe`,`GoogleMaps` in android) |
| `centerCoordinate`          | `arrayOf` | none    | false    | 地图初始化时的中心点                                                                                                        |
| `visibleCoordinateBounds`   | `arrayOf` | none    | false    | 初始化时显示的区域左上右下                                                                                                     |
| `showUserLocation`          | `bool`    | false   | false    | 显示获取当前定位的icon                                                                                                     |
| `style`                     | `any`     | false   | false    | React Native View的style                                                                                           |
| `styleURL`                  | `string`  | false   | false    | 地图的样式url                                                                                                          |
| `rotateEnabled`             | `bool`    | `false` | false    | 是否允许旋转                                                                                                            |
| `compassEnabled`            | `Boolean` | `true`  | false    | 是否显示指南针                                                                                                           |
| `showScale`                 | `Boolean` | `true`  | false    | 是否显示缩放比例尺                                                                                                         |
| `scrollEnabled`             | `Boolean` | `true`  | false    | 是否允许滑动                                                                                                            |
| `zoomEnabled`               | `Boolean` | `true`  | false    | 是否允许缩放                                                                                                            |
| `localizeLabels`            | `Boolean` | `true`  | false    | 根据系统语言设置改变地图的上的文案信息                                                                                               |
| `zoomLevel`                 | `Number`  | `16`    | false    | 当前的缩放级别                                                                                                           |
| `minZoomLevel`              | `Number`  | `0`     | false    | 最小的缩放比例（0 - 20）                                                                                                   |
| `maxZoomLevel`              | `Number`  | `20`    | false    | 最大的缩放比例（0 - 20）                                                                                                   |
| `onRegionDidChange`         | `func`    | `none`  | false    | 显示区域变化的回调                                                                                                         |
| `onDidFinishRenderingFrame` | `func`    | `none`  | false    | 当滑动地图后地图渲染完成的回调                                                                                                   |
| `onDidFinishLoadingStyle`   | `func`    | `none`  | false    | 地图样式加载完成的回调                                                                                                       |

### methods

#### getPointInView(coordinate)

将坐标信息转换成视图view的点位置

##### arguments

| Name | Type | Required | Description  |
|---|----------|-------------|---|
| `coordinate` | `Array` | `Yes` | 地图上的坐标信息|

```javascript
const pointInView = await this._map.getPointInView([-37.817070, 144.949901]);
```

#### getCoordinateFromView(point)

将视图view的点信息转换成对应的坐标信息

##### arguments

| Name | Type | Required | Description  |
|---|----------|-------------|---|
| `point` | `Array` | `Yes` | 视图view的坐标点信息|

```javascript
const coordinate = await this._map.getCoordinateFromView([100, 100]);
```

#### getVisibleBounds()

用户在地图上可见的范围坐标左上右下 coordinate bounds(ne, sw)

```javascript
const visibleBounds = await this._map.getVisibleBounds();
```

#### fitBounds(northEastCoordinates, southWestCoordinates[, padding][, duration])

地图窗口移动到给定的边界和间距

##### arguments

| Name | Type | Required | Description                  |
|---|----------|-------------|------------------------------|
| `northEastCoordinates` | `Array` | `Yes` | 右上         |
| `southWestCoordinates` | `Array` | `Yes` | 左下       |
| `padding` | `Number` | `No` | 地图的间距      |
| `duration` | `Number` | `No` | 地图镜头移动动画时间 |

```javascript
this.map.fitBounds([lng, lat], [lng, lat])
this.map.fitBounds([lng, lat], [lng, lat], 20, 1000) // padding for all sides
this.map.fitBounds([lng, lat], [lng, lat], [verticalPadding, horizontalPadding], 1000)
this.map.fitBounds([lng, lat], [lng, lat], [top, right, bottom, left], 1000)
```

#### flyTo(coordinates[, duration])

地图镜头显示到指定的坐标点

##### arguments

| Name | Type | Required | Description  |
|---|----------|-------------|---|
| `coordinates` | `Array` | `Yes` |  移动的坐标点位置   |
| `duration` | `Number` | `No` |地图镜头移动动画时间|

```javascript
this.map.flyTo([lng, lat])
this.map.flyTo([lng, lat], 12000)
```

#### moveTo(coordinates[, duration])

地图镜头以比例尺不变的状态移动到指定的坐标点

##### arguments

| Name | Type | Required | Description                  |
|---|----------|-------------|------------------------------|
| `coordinates` | `Array` | `Yes` | 移动的坐标点位置    |
| `duration` | `Number` | `No` |  地图镜头移动动画时间  |

```javascript
this.map.moveTo([lng, lat], 200) // eases camera to new location based on duration
this.map.moveTo([lng, lat]) // snaps camera to new location without any easing
```

#### zoomTo(zoomLevel[, duration])

地图镜头以指定的比例尺缩放

##### arguments

| Name | Type | Required | Description |
|---|----------|-------------|-------------|
| `zoomLevel` | `Number` | `Yes` | 缩放级别        |
| `duration` | `Number` | `No` | 地图镜头移动动画时间  |

```javascript
this.map.zoomTo(16)
this.map.zoomTo(16, 100)
```

#### getZoom()

获得当前地图的比例尺

```javascript
const zoom = await this._map.getZoom();
```

#### getCenter()

获得当前地图的中心点

```javascript
const center = await this._map.getCenter();
```

