# ks-datepicker

## Overview

The `ks-datepicker` component provides an intuitive date selection interface for forms and user input scenarios. It supports date selection, minimum and maximum date constraints, placeholders, disabled states, labels, and programmatic value updates.

In Angular, the component supports two-way binding through the `selectedDate` input and `ksSelectedDateChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `disabled` | Disables the component. | `boolean` | `false` |
| `label` | Label displayed above the field. | `string` | `''` |
| `maxDate` | Maximum selectable date. | `Date` | `null` |
| `minDate` | Minimum selectable date. | `Date` | `null` |
| `placeholder` | Placeholder text displayed when no date is selected. | `string` | `'Select date'` |
| `selectedDate` | Currently selected date. Supports Angular two-way binding. | `Date \| null` | `null` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksSelectedDateChange` | Fired when the selected date changes. | `Date \| null` |

## Methods

### writeValue(val)

Programmatically updates the selected date.

```ts
writeValue(val: Date | null): Promise<void>
```

# Usage

## React

```tsx
import { KsDatepicker } from '@kraft.stitch/react';

function App() {
  return (
    <KsDatepicker
      label="Start Date"
      placeholder="Select date"
      selectedDate={new Date()}
    />
  );
}
```

## Angular

```ts
import { KsDatepickerComponent } from '@kraft.stitch/angular';
```

```html
<ks-datepicker
  label="Start Date"
  placeholder="Select date"
  [(selectedDate)]="selectedDate">
</ks-datepicker>
```