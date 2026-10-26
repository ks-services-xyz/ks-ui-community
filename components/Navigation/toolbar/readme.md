# ks-toolbar

## Overview

The `ks-toolbar` component provides a horizontal collection of actions and tools commonly used for page-level or content-level operations. It supports icons, labels, dividers, active states, disabled items, visual variants, and custom content through slots.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `items` | Collection of toolbar items. | `KsToolbarItem[]` | `[]` |

### KsToolbarItem

```typescript
export interface KsToolbarItem {
  key: string;
  icon?: string;
  label?: string;
  divider?: boolean;
  disabled?: boolean;
  active?: boolean;
  variant?: KsVariant;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `itemClicked` | Fired when a toolbar item is clicked. Returns the item key. | `string` |

## Slots

| Slot | Description |
| ---- | ----------- |
| Default | Additional custom toolbar content. |

# Usage

## React

```tsx
import { KsToolbar } from '@kraft.stitch/react';

function App() {
  const items = [
    {
      key: 'save',
      label: 'Save',
      icon: 'ks-icon-save',
      variant: 'success'
    },
    {
      key: 'edit',
      label: 'Edit',
      icon: 'ks-icon-pencil'
    },
    {
      divider: true
    },
    {
      key: 'delete',
      label: 'Delete',
      icon: 'ks-icon-trash',
      variant: 'danger'
    }
  ];

  return (
    <KsToolbar items={items} />
  );
}
```

## Angular

```typescript
import { KsToolbarComponent } from '@kraft.stitch/angular';
```

```html
<ks-toolbar
  [items]="toolbarItems">
</ks-toolbar>
```