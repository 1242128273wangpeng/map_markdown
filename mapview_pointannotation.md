## < PointAnnotation />

### 静态的标签信息

### props

| Prop         | Type      | Default            | Required    | Note                        |
|--------------|-----------|--------------------|-------------|-----------------------------|
| id           | `string`  | `none`             | `true`      | 静态点的唯一Id                    |
| title        | `string`  | `none`             | `false`     | 头部标题信息                      |
| snippet      | `string`  | `none`             | `false`     | 小标题                         |
| selected     | `bool`    | `none`             | `false`     | 是否被选中                       |
| coordinate   | `arrayOf` | `none`             | `true` 坐标信息 |
| anchor       | `shape`   | `{x: 0.5, y: 0.5}` | `false`     | 相对方向 (0, 0) 对应左上(1, 1) 对应右下 |
| onSelected   | `func`    | `none`             | `false`     | 被选中的回调                      |
| onDeselected | `func`    | `none`             | `false`     | 反选的回调                       |


