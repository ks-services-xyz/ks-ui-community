# ks-colour-picker

## Overview

The `ks-colour-picker` component allows users to select and manage color values through an interactive color picker interface. It supports custom color selection, predefined color swatches, disabled states, and programmatic value updates.

In Angular, the component supports two-way binding through the `value` input and `ksValueChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `disabled` | Disables the component. | `boolean` | `false` |
| `label` | Label displayed above the field. | `string` | `''` |
| `swatches` | Collection of predefined color swatches. | `string[]` | Preset color palette |
| `value` | Currently selected color value. Supports Angular two-way binding. | `string` | `'#3b82f6'` |
| `variant` | Display style of the color picker. | `"input" \| "swatch"` | `'input'` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksValueChange` | Fired when the selected color changes. | `string` |

## Methods

### writeValue(val)

Programmatically updates the selected color.

```typescript
writeValue(val: string): Promise<void>
```

# Usage

## React

```tsx
import { KsColourPicker } from '@kraft.stitch/react';

function App() {
  return (
    <KsColourPicker
      label="Primary Color"
      value="#3b82f6"
      variant="input"
    />
  );
}
```

## Angular

```typescript
import { KsColourPickerComponent } from '@kraft.stitch/angular';
```

```html
<ks-colour-picker
  label="Primary Color"
  variant="input"
  [(value)]="color">
</ks-colour-picker>
```