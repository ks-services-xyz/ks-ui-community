# ks-checkbox

## Overview

The `ks-checkbox` component provides checkbox functionality for both single-selection and multi-selection scenarios. It can be used as a standalone checkbox or as a checkbox group with multiple options. The component supports disabled states, labels, controlled values, and programmatic value updates.

In Angular, the component supports two-way binding through the `checked` and `selected` inputs with their corresponding `ksCheckedChange` and `ksSelectedChange` outputs.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `checked` | Checked state for single-checkbox mode. Supports Angular two-way binding. | `boolean` | `false` |
| `disabled` | Disables the component. | `boolean` | `false` |
| `label` | Label displayed next to the checkbox. | `string` | `''` |
| `options` | Collection of checkbox options for group mode. | `KsCheckboxOption[]` | `[]` |
| `selected` | Selected values for checkbox group mode. Supports Angular two-way binding. | `string[]` | `[]` |

### KsCheckboxOption

```typescript
export interface KsCheckboxOption {
  value: string;
  label?: string;
  disabled?: boolean;
  checked?: boolean;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksCheckedChange` | Fired when the checked state changes in single-checkbox mode. | `boolean` |
| `ksSelectedChange` | Fired when the selected values change in group mode. | `string[]` |

## Methods

### writeValue(val)

Programmatically updates the checkbox value or selected values.

```typescript
writeValue(val: any): Promise<void>
```

# Usage

## React

### Single Checkbox

```tsx
import { KsCheckbox } from '@kraft.stitch/react';

function App() {
  return (
    <KsCheckbox
      label="Accept Terms and Conditions"
      checked={true}
    />
  );
}
```

### Checkbox Group

```tsx
import { KsCheckbox } from '@kraft.stitch/react';

function App() {
  const options = [
    { value: 'angular', label: 'Angular' },
    { value: 'react', label: 'React' },
    { value: 'vue', label: 'Vue' }
  ];

  return (
    <KsCheckbox
      options={options}
      selected={['react']}
    />
  );
}
```

## Angular

```typescript
import { KsCheckboxComponent } from '@kraft.stitch/angular';
```

### Single Checkbox

```html
<ks-checkbox
  label="Accept Terms and Conditions"
  [(checked)]="accepted">
</ks-checkbox>
```

### Checkbox Group

```html
<ks-checkbox
  [options]="options"
  [(selected)]="selectedValues">
</ks-checkbox>
```