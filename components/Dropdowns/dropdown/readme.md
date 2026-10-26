# ks-dropdown

## Overview

The `ks-dropdown` component provides a customizable dropdown selection control for choosing one or multiple options from a list. It supports single-select and multi-select modes, optional search functionality, disabled states, placeholders, and programmatic value updates.

In Angular, the component supports two-way binding through the `selectedValues` input and `ksSelectedValuesChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `disabled` | Disables the component. | `boolean` | `false` |
| `label` | Label displayed above the field. | `string` | `''` |
| `multi` | Allows selecting multiple options. | `boolean` | `false` |
| `options` | Collection of available dropdown options. | `KsDropdownOption[]` | `[]` |
| `placeholder` | Placeholder text displayed when no option is selected. | `string` | `'Select…'` |
| `searchable` | Displays a search box inside the dropdown. | `boolean` | `false` |
| `selectedValues` | Currently selected value(s). Supports Angular two-way binding. | `(string \| number)[]` | `[]` |

### KsDropdownOption

```ts
export interface KsDropdownOption {
  value: string | number;
  label: string;
  icon?: string;
  disabled?: boolean;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksSelectedValuesChange` | Fired when the selected value(s) change. | `(string \| number)[] \| string \| number` |

## Methods

### writeValue(val)

Programmatically updates the selected value(s).

```ts
writeValue(val: any): Promise<void>
```

# Usage

## React

```tsx
import { KsDropdown } from '@kraft.stitch/react';

function App() {
  const options = [
    { value: 1, label: 'Angular' },
    { value: 2, label: 'React' },
    { value: 3, label: 'Vue' }
  ];

  return (
    <KsDropdown
      label="Framework"
      options={options}
      selectedValues={[2]}
    />
  );
}
```

## Angular

```ts
import { KsDropdownComponent } from '@kraft.stitch/angular';
```

```html
<ks-dropdown
  label="Framework"
  [options]="options"
  [(selectedValues)]="selectedValues">
</ks-dropdown>
```