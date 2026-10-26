# ks-timepicker

## Overview

The `ks-timepicker` component provides an intuitive interface for selecting time values. It supports 12-hour and 24-hour formats, optional seconds selection, validation feedback, disabled states, placeholders, and programmatic value updates.

In Angular, the component supports two-way binding through the `value` input and `ksValueChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `disabled` | Disables the component. | `boolean` | `false` |
| `error` | Error message displayed below the field. | `string` | `''` |
| `label` | Label displayed above the field. | `string` | `''` |
| `placeholder` | Placeholder text displayed when no time is selected. | `string` | `'Select time…'` |
| `showSeconds` | Displays seconds selection. | `boolean` | `false` |
| `use12Hour` | Enables 12-hour (AM/PM) format. | `boolean` | `false` |
| `value` | Currently selected time. Supports Angular two-way binding. | `KsTimeValue` | `null` |

### KsTimeValue

```ts
export interface KsTimeValue {
  hours: number;
  minutes: number;
  seconds?: number;
  period?: 'AM' | 'PM';
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksValueChange` | Fired when the selected time changes. | `KsTimeValue` |

## Methods

### writeValue(val)

Programmatically updates the selected time.

```ts
writeValue(val: KsTimeValue | null): Promise<void>
```

# Usage

## React

```tsx
import { KsTimepicker } from '@kraft.stitch/react';

function App() {
  return (
    <KsTimepicker
      label="Start Time"
      value={{
        hours: 9,
        minutes: 30,
      }}
    />
  );
}
```

## Angular

```ts
import { KsTimepickerComponent } from '@kraft.stitch/angular';
```

```html
<ks-timepicker
  label="Start Time"
  [(value)]="time">
</ks-timepicker>
```