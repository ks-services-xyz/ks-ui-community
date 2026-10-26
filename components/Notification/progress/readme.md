# ks-progress

## Overview

The `ks-progress` component visually communicates the progress of a task, process, or operation. It supports determinate and indeterminate states, configurable sizes, labels, color variants, and percentage display options.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `indeterminate` | Displays an animated loading state when progress is unknown. | `boolean` | `false` |
| `label` | Optional text displayed alongside the progress indicator. | `string` | `''` |
| `max` | Maximum progress value. | `number` | `100` |
| `showLabel` | Displays the current progress percentage. | `boolean` | `false` |
| `size` | Progress indicator size. | `"sm" \| "md" \| "lg"` | `'md'` |
| `value` | Current progress value. | `number` | `0` |
| `variant` | Visual style variant. | `"brand" \| "danger" \| "info" \| "neutral" \| "success" \| "warning"` | `'brand'` |

# Usage

## React

```tsx
import { KsProgress } from '@kraft.stitch/react';

function App() {
  return (
    <KsProgress
      label="Upload Progress"
      value={65}
      max={100}
      showLabel={true}
      variant="success"
    />
  );
}
```

### Indeterminate Progress

```tsx
<KsProgress
  label="Loading..."
  indeterminate={true}
/>
```

## Angular

```typescript
import { KsProgressComponent } from '@kraft.stitch/angular';
```

```html
<ks-progress
  label="Upload Progress"
  [value]="65"
  [max]="100"
  [showLabel]="true"
  variant="success">
</ks-progress>
```

### Indeterminate Progress

```html
<ks-progress
  label="Loading..."
  [indeterminate]="true">
</ks-progress>
```