# ks-listbox

## Overview

The `ks-listbox` component provides a selectable list of options for single or multiple selection scenarios. It supports optional search functionality, grouped options, disabled states, and programmatic value updates.

In Angular, the component supports two-way binding through the `selected` input and `ksSelectedChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `disabled` | Disables the component. | `boolean` | `false` |
| `groupBy` | Enables grouping using the `group` field on each option. | `boolean` | `false` |
| `multi` | Allows selecting multiple options. | `boolean` | `false` |
| `options` | Collection of available list box options. | `KsListBoxOption[]` | `[]` |
| `searchable` | Displays a search box for filtering options. | `boolean` | `false` |
| `selected` | Currently selected value(s). Supports Angular two-way binding. | `(string \| number)[]` | `[]` |

### KsListBoxOption

```typescript
export interface KsListBoxOption {
  value: string | number;
  label: string;
  icon?: string;
  disabled?: boolean;

  /** Optional group key used when groupBy is enabled */
  group?: string;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksSelectedChange` | Fired when the selected value(s) change. | `(string \| number)[] \| string \| number` |

## Methods

### writeValue(val)

Programmatically updates the selected value(s).

```typescript
writeValue(val: any): Promise<void>
```

# Usage

## React

```typescript
import { KsListbox } from '@kraft.stitch/react';

function App() {
  const options = [
    { value: 1, label: 'Angular', group: 'Frontend' },
    { value: 2, label: 'React', group: 'Frontend' },
    { value: 3, label: 'Node.js', group: 'Backend' }
  ];

  return (
    <KsListbox
      options={options}
      selected={[2]}
      searchable={true}
      groupBy={true}
    />
  );
}
```

## Angular

```typescript
import { KsListboxComponent } from '@kraft.stitch/angular';
```

```html
<ks-listbox
  [options]="options"
  [searchable]="true"
  [groupBy]="true"
  [selected]="selected"
  (ksSelectedChange)="selected = $event">
</ks-listbox>
```