# ks-chips

## Overview

The `ks-chips` component provides a selectable list of chips that can be used for filtering, categorization, tagging, and option selection. It supports both single-select and multi-select modes, customizable sizes, disabled states, and controlled value management.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `disabled` | Disables the component. | `boolean` | `false` |
| `isRounded` | Renders chips with fully rounded pill corners. | `boolean` | `true` |
| `label` | Label displayed above the chip group. | `string` | `''` |
| `multi` | Allows selecting multiple chips. | `boolean` | `false` |
| `options` | Collection of available chip options. | `KsChipOption[]` | `[]` |
| `size` | Chip size. | `"lg" \| "md" \| "sm"` | `'md'` |
| `value` | Selected value or values. | `(string \| number)[] \| string \| number` | `null` |

### KsChipOption

### KsChipOption

```ts
export interface KsChipOption {
  value: string | number;
  label: string;
  icon?: string;
  disabled?: boolean;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `valueChange` | Fired when the selected value(s) change. | `(string \| number)[] \| string \| number` |

## Methods

### writeValue(val)

Programmatically updates the selected value or values.

```ts
writeValue(val: any): Promise<void>
```

# Usage

## React

```tsx
import { KsChips } from '@kraft.stitch/react';

function App() {
  const options = [
    { label: 'Angular', value: 'angular' },
    { label: 'React', value: 'react' },
    { label: 'Vue', value: 'vue' }
  ];

  return (
    <KsChips
      label="Framework"
      options={options}
      value="react"
    />
  );
}
```

## Angular

```ts
import { KsChipsComponent } from '@kraft.stitch/angular';
```

```html
<ks-chips
  label="Framework"
  [options]="options"
  value="react">
</ks-chips>
```