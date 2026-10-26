# ks-context-menu

## Overview

The `ks-context-menu` component provides a customizable right-click or contextual action menu. It supports dynamic menu items, programmatic opening and closing, and item selection events, making it useful for actions related to specific content, records, or UI elements.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `items` | Collection of menu items displayed in the context menu. | `KsContextMenuItem[]` | `[]` |

### KsContextMenuItem

```typescript
export interface KsContextMenuItem {
  key: string;
  label?: string;
  icon?: string;
  divider?: boolean;
  disabled?: boolean;
  danger?: boolean;
}
```
Set `divider:true` for a divider inbetween context menu

### KsContextMenuPosition

```typescript
export interface KsContextMenuPosition {
  x: number;
  y: number;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `itemClicked` | Fired when a menu item is selected. Returns the clicked item key. | `string` |

## Methods

### open(pos)

Opens the context menu at the specified screen position.

```typescript
open(pos: KsContextMenuPosition): Promise<void>
```

### close()

Closes the context menu.

```typescript
close(): Promise<void>
```

# Usage

## React

```tsx
import { KsContextMenu } from '@kraft.stitch/react';
import { useRef } from 'react';

function App() {
  const menuRef = useRef(null);

  const items = [
    { key: 'edit', label: 'Edit' },
    { key: 'copy', label: 'Copy' },
    { key: 'delete', label: 'Delete' }
  ];

  const onContextMenu = async (event) => {
    event.preventDefault();

    await menuRef.current?.open({
      x: event.clientX,
      y: event.clientY
    });
  };

  return (
    <div onContextMenu={onContextMenu}>
      Right-click me

      <KsContextMenu
        ref={menuRef}
        items={items}
      />
    </div>
  );
}
```

## Angular

```typescript
import { KsContextMenuComponent } from '@kraft.stitch/angular';
```

```html
<div (contextmenu)="onContextMenu($event)">
  Right-click me
</div>

<ks-context-menu
  [items]="items">
</ks-context-menu>
```

```typescript
onContextMenu(event: MouseEvent) {
  event.preventDefault();

  this.contextMenu.open({
    x: event.clientX,
    y: event.clientY
  });
}
```