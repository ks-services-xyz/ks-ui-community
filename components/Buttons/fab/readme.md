# ks-fab

## Overview

The `ks-fab` component provides a floating action button (FAB) for highlighting primary actions within an application. It supports configurable positioning, multiple visual variants, different sizes, disabled states, and expandable speed-dial actions for quick access to related functionality.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `actions` | Collection of speed-dial actions displayed when expanded. | `KsFabAction[]` | `[]` |
| `appendToParent` | When enabled, the FAB is positioned relative to its nearest positioned parent; otherwise it is fixed to the viewport. | `boolean` | `true` |
| `disabled` | Disables the component. | `boolean` | `false` |
| `icon` | Icon displayed on the main FAB button. | `string` | `''` |
| `label` | Accessible label and tooltip text. | `string` | `''` |
| `position` | Position of the FAB within its container. | `"bottom-left" \| "bottom-right" \| "top-left" \| "top-right"` | `'bottom-right'` |
| `size` | FAB size. | `"lg" \| "md" \| "sm"` | `'md'` |
| `variant` | Visual variant. | `"brand" \| "danger" \| "info" \| "neutral" \| "success" \| "warning"` | `'brand'` |

### KsFabAction

```ts
export interface KsFabAction {
  key: string;
  label: string;
  icon?: string;
  disabled?: boolean;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `clicked` | Fired when the main FAB or a speed-dial action is clicked. Returns the action key. | `string` |

# Usage

## React

```tsx
import { KsFab } from '@kraft.stitch/react';

function App() {
  const actions = [
    { key: 'add', label: 'Add', icon: 'ks-icon-plus' },
    { key: 'edit', label: 'Edit', icon: 'ks-icon-pencil' },
    { key: 'delete', label: 'Delete', icon: 'ks-icon-trash' }
  ];

  return (
    <KsFab
      icon="ks-icon-plus"
      label="Actions"
      variant="brand"
      actions={actions}
    />
  );
}
```

## Angular

```ts
import { KsFabComponent } from '@kraft.stitch/angular';
```

```html
<ks-fab
  icon="ks-icon-plus"
  label="Actions"
  variant="brand"
  [actions]="actions">
</ks-fab>
```