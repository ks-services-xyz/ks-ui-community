# ks-switch

## Overview

The `ks-switch` component provides a toggle control for switching between two states, such as enabled/disabled or on/off. It supports labels, configurable label positioning, visual variants, disabled states, and controlled value management.

In Angular, the component supports two-way binding through the `checked` input and `ksCheckedChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `checked` | Current switch state. Supports Angular two-way binding. | `boolean` | `false` |
| `disabled` | Disables the component. | `boolean` | `false` |
| `formDisabled` | Internal disabled state applied by forms integration. | `boolean` | `false` |
| `label` | Label displayed alongside the switch. | `string` | `''` |
| `labelPosition` | Position of the label relative to the switch. | `"left" \| "right"` | `'left'` |
| `variant` | Visual style variant. | `"brand" \| "danger" \| "info" \| "neutral" \| "success" \| "warning"` | `'brand'` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksCheckedChange` | Fired when the switch state changes. | `boolean` |

## Methods

### setDisabledState(isDisabled)

Programmatically updates the disabled state.

```typescript
setDisabledState(isDisabled: boolean): Promise<void>
```

# Usage

## React

```tsx
import { KsSwitch } from '@kraft.stitch/react';

function App() {
  return (
    <KsSwitch
      label="Enable Notifications"
      checked={true}
      variant="brand"
    />
  );
}
```

## Angular

```typescript
import { KsSwitchComponent } from '@kraft.stitch/angular';
```

```html
<ks-switch
  label="Enable Notifications"
  variant="brand"
  [(checked)]="notificationsEnabled">
</ks-switch>
```