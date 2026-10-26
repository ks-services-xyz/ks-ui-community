# ks-radio

## Overview

The `ks-radio` component provides a radio button group for selecting a single value from a predefined set of options. It supports customizable sizes, visual variants, disabled states, labels, and controlled value management.

In Angular, the component supports two-way binding through the `value` input and `ksValueChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `disabled` | Disables the component. | `boolean` | `false` |
| `label` | Label displayed above the radio group. | `string` | `''` |
| `name` | Name shared across all radio inputs within the group. | `string` | `'ks-radio'` |
| `options` | Collection of radio button options. | `KsRadioOption[]` | `[]` |
| `size` | Size variant applied to the radio group. | `"sm" \| "md" \| "lg" \| "xl"` | `'md'` |
| `value` | Currently selected value. Supports Angular two-way binding. | `string` | `''` |
| `variant` | Visual variant applied to the selected indicator. | `"brand" \| "danger" \| "info" \| "neutral" \| "success" \| "warning"` | `'brand'` |

### KsRadioOption

```typescript
export interface KsRadioOption {
  value: string;
  label?: string;
  disabled?: boolean;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksValueChange` | Fired when the selected value changes. | `string` |

## Methods

### writeValue(val)

Programmatically updates the selected value.

```typescript
writeValue(val: string): Promise<void>
```

# Usage

## React

```tsx
import { KsRadio } from '@kraft.stitch/react';

function App() {
  const options = [
    { value: 'angular', label: 'Angular' },
    { value: 'react', label: 'React' },
    { value: 'vue', label: 'Vue' }
  ];

  return (
    <KsRadio
      label="Framework"
      options={options}
      value="react"
    />
  );
}
```

## Angular

```typescript
import { KsRadioComponent } from '@kraft.stitch/angular';
```

```html
<ks-radio
  label="Framework"
  [options]="options"
  [(value)]="selectedFramework">
</ks-radio>
```