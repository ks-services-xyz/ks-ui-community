# ks-daterange

## Overview

The `ks-daterange` component allows users to select a start and end date as a single date range. It supports minimum and maximum date constraints, predefined date range presets, customizable placeholders, disabled states, and programmatic value updates.

In Angular, the component supports two-way binding through the `range` input and `ksRangeChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `disabled` | Disables the component. | `boolean` | `false` |
| `label` | Label displayed above the field. | `string` | `''` |
| `maxDate` | Maximum selectable date. | `Date` | `null` |
| `minDate` | Minimum selectable date. | `Date` | `null` |
| `placeholder` | Placeholder text displayed when no date range is selected. | `string` | `'Select date range…'` |
| `presets` | Predefined date range selections available to users. | `KsPresetRange[]` | Built-in presets |
| `range` | Currently selected date range. Supports Angular two-way binding. | `KsDateRange` | `{ start: null, end: null }` |
| `showPresets` | Displays predefined date range presets. | `boolean` | `true` |

### KsDateRange

```ts
export interface KsDateRange {
  start: Date | null;
  end: Date | null;
}
```

### KsPresetRange

```ts
export interface KsPresetRange {
  label: string;
  range: () => KsDateRange;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksRangeChange` | Fired when the selected date range changes. | `KsDateRange` |

## Methods

### writeValue(val)

Programmatically updates the selected date range.

```ts
writeValue(val: KsDateRange | null): Promise<void>
```

# Usage

## React

```tsx
import { KsDaterange } from '@kraft.stitch/react';

function App() {
  return (
    <KsDaterange
      label="Date Range"
      range={{
        start: new Date(),
        end: new Date(),
      }}
    />
  );
}
```

## Angular

```ts
import { KsDaterangeComponent } from '@kraft.stitch/angular';
```

```html
<ks-daterange
  label="Date Range"
  [(range)]="range">
</ks-daterange>
```