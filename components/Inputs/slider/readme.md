# ks-slider

## Overview

The `ks-slider` component allows users to select a numeric value within a defined range by dragging a slider thumb. It supports configurable minimum and maximum values, step intervals, value tooltips, labels, disabled states, and controlled value management.

In Angular, the component supports two-way binding through the `value` input and `ksValueChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `disabled` | Disables the component. | `boolean` | `false` |
| `label` | Label displayed above the slider. | `string` | `''` |
| `max` | Maximum allowed value. | `number` | `100` |
| `min` | Minimum allowed value. | `number` | `0` |
| `showLabels` | Displays minimum and maximum value labels. | `boolean` | `false` |
| `showTooltip` | Displays the current value in a tooltip while interacting. | `boolean` | `true` |
| `step` | Increment step value. | `number` | `1` |
| `value` | Current slider value. Supports Angular two-way binding. | `number` | `0` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksBlur` | Fired when the slider loses focus. | `void` |
| `ksValueChange` | Fired when the slider value changes. | `number` |

## Methods

### writeValue(val)

Programmatically updates the slider value.

```typescript
writeValue(val: number): Promise<void>
```

# Usage

## React

```tsx
import { KsSlider } from '@kraft.stitch/react';

function App() {
  return (
    <KsSlider
      label="Volume"
      min={0}
      max={100}
      step={1}
      value={50}
    />
  );
}
```

## Angular

```typescript
import { KsSliderComponent } from '@kraft.stitch/angular';
```

```html
<ks-slider
  label="Volume"
  [min]="0"
  [max]="100"
  [step]="1"
  [(value)]="volume">
</ks-slider>
```