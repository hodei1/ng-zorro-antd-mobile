---
category: Components
type: Feedback
title: Toast
---


A lightweight feedback or tips, used to display content that does not interrupt user operations. Suitable for page transitions, data interaction and other scenes.


### Rules
- Only one Toast is allowed at a time.
- Toast with Icon, 4-6 words is recommended.; Toast without Icon, the number of words should not exceed 14.


## API

- `ToastService.success(content, duration, onClose, mask)`
- `ToastService.fail(content, duration, onClose, mask)`
- `ToastService.info(content, duration, onClose, mask)`
- `ToastService.loading(content, duration, onClose, mask)`
- `ToastService.offline(content, duration, onClose, mask)`

The component provide several static methods：

Properties | Descrition | Type | Default
-----------|------------|------|--------
| content    | Toast content       | TemplateRef or String    | -           |
| duration   | Delay time to close, which units is millisecond | number                 | 3000          |
| onClose    | A callback function Triggered when the Toast is closed |  Function                 | -          |
| mask    | Whether to show a transparent mask, which will prevent touch event of the whole page |  Boolean  | true          |
| position    | enum{'top', 'middle', 'bottom'} |  string  | 'middle'      |

> **Notice：** OnClose is invalid and Toast does not hide, If set duration = 0, toast will not auto hide, you have to manually do it.

Provides global configuration and global destroy methods:

- `ToastService.hide()`
