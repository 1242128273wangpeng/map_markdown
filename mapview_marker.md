
## < MarkerView />

### MarkerView时提供一个可在rn交互的marker点，如果是静态点可考虑PointAnnotation或者SymbolLayer性能相对更好

### props

| Prop          | Type      | Default              | Required | Note                        |
|---------------|-----------|----------------------|----------|-----------------------------|
| coordinate    | `array`   | `none`               | `true`   | marker的坐标点                  |
| anchor        | `shape`   | `{ x: 0.5, y: 0.5 }` | `false`  | 相对方向 (0, 0) 对应左上(1, 1) 对应右下 |
| &nbsp;&nbsp;x | `number`  | `none`               | `true`   | `x` 横坐标上相对的锚点               |
| &nbsp;&nbsp;y | `number`  | `none`               | `true`   | `y` 纵坐标上相对的锚点               |
| children      | `element` | `none`               | `true`   | 孩子节点                        |


