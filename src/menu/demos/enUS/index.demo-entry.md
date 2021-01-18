# Menu

<!--single-column-->

No Food.

## Demos

```demo
horizontal
default-expanded-names
indent
collapse
```

## Props

### Menu Props

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| collapsed-icon-size | `number` | `undefined` | The icon size when menu is collapsed. If not set, menu will use `icon-size` in place of it. |
| collapsed-width | `number` | `undefined` | The menu width after collapsed. |
| collapsed | `boolean` | `false` | The collapsed status of menu, only works when menu is vertical. |
| default-expand-all | `boolean` | `false` |  |
| default-expanded-keys | `Array<string>` | `[]` | The default expanded submenu keys of menu in uncontrolled manner. |
| default-value | `string \| null` | `null` |  |
| expanded-keys | `Array<string>` | `undefined` | The expanded submenu keys. If set, menu will work in controlled manner and `default-expanded-names` won't work. |
| icon-size | `number` | `20` | The icon size when menu is not collapsed. |
| indent | `number` | `32` | The indend of menu |
| items | `Array<MenuItem \| Submenu \| MenuItemGroup>` | `[]` | Items data of menu. |
| mode | `'vertical' \| 'horizontal'` | `'vertical'` |  |
| root-indent | `number` | `undefined` | The indent of menu's first level children. If not set, menu will use `indent` in place of it. |
| value | `string \| null` | `undefined` | The selected name of menu. |
| on-update:expanded-keys | `(value: string[]) => any` | `undefined` |  |
| on-update:value | `(value: string, item: MenuItem) => any` | `undefined` |  |

### MenuItem Properties

| Name     | Type          | Description                                    |
| -------- | ------------- | ---------------------------------------------- |
| disabled | `boolean`     |                                                |
| extra    | `string`      |                                                |
| icon     | `() => VNode` |                                                |
| key      | `string`      | The indentifier of the menu item. **required** |
| title    | `string`      |                                                |

### Submenu Properties

| Name | Type | Description |
| --- | --- | --- |
| children | `Array<MenuItem \| Submenu \| MenuItemGroup>` | **required** |
| disabled | `boolean` |  |
| extra | `string` |  |
| icon | `() => VNode` |  |
| key | `string` | The indentifier of the submenu. **required** |
| title | `string` |  |

### MenuItemGroup Properties

| Name | Type | Description |
| --- | --- | --- |
| children | `Array<MenuItem \| Submenu \| MenuItemGroup>` | **required** |
| key | `string` | 菜单项的标识符，**必需** |
| title | `string` |  |
| type | `'group'` | **required** |