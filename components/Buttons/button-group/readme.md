# ks-button-group

## Overview

The `ks-button-group` component displays a collection of related buttons as a single grouped control. It supports standard button groups, selectable button groups, toggle behavior, single or multiple selection modes, and switch-style presentation for creating segmented controls and option selectors.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `buttons` | The buttons to render. | `KsButtonGroupItem[]` | `[]` |
| `disabled` | Disables the entire button group. | `boolean` | `false` |
| `displayStyle` | Display style of the button group. | `"default" \| "switch"` | `'default'` |
| `multi` | Allows multiple selected buttons. | `boolean` | `false` |
| `selectable` | Enables selection mode and active states. | `boolean` | `false` |
| `size` | Button group size. | `"lg" \| "md" \| "sm"` | `'md'` |
| `variant` | Visual variant applied to the group. | `"brand" \| "danger" \| "info" \| "neutral" \| "success" \| "warning"` | `'brand'` |

### KsButtonGroupItem

```ts
export interface KsButtonGroupItem {
  key: string;
  label?: string;
  icon?: string;
  disabled?: boolean;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `clicked` | Fired when a button is clicked. Returns the clicked button key. | `string` |
| `selectionChanged` | Fired when the selected buttons change. Returns the selected button keys. | `string[]` |

# Usage

## React

```tsx
import { KsButtonGroup } from '@kraft.stitch/react';

function App() {
  const buttons = [
    { key: 'save', label: 'Save', icon: 'ks-icon-save' },
    { key: 'edit', label: 'Edit', icon: 'ks-icon-pencil' },
    { key: 'delete', label: 'Delete', icon: 'ks-icon-trash' },
  ];

  return (
    <KsButtonGroup
      buttons={buttons}
      variant="brand"
      size="md"
      selectable={true}
    />
  );
}
```

## Angular

```ts
import { KsButtonGroupComponent } from '@kraft.stitch/angular';
```

```html
<ks-button-group
  [buttons]="buttons"
  variant="brand"
  size="md"
  [selectable]="true">
</ks-button-group>
```