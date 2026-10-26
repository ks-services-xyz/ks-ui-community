# ks-tooltip

## Overview

The `ks-tooltip` component displays contextual information when users interact with an element. It can be shown on hover, focus, or programmatically, and supports multiple placement options to ensure the tooltip appears in an appropriate location relative to its target.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `position` | Preferred tooltip placement. | `"top" \| "right" \| "bottom" \| "left"` | `'top'` |
| `text` | Content displayed inside the tooltip. | `string` | `''` |
| `visible` | Controls whether the tooltip is always visible. When `false`, normal hover behavior is used. | `boolean` | `false` |

## Slots

| Slot | Description |
| ---- | ----------- |
| Default | Element that triggers the tooltip. |

# Usage

## React

```tsx
import { KsTooltip, KsButton } from '@kraft.stitch/react';

function App() {
  return (
    <KsTooltip
      text="Save changes"
      position="top"
    >
      <KsButton name="Save" />
    </KsTooltip>
  );
}
```

## Angular

```typescript
import { KsTooltipComponent } from '@kraft.stitch/angular';
```

```html
<ks-tooltip
  text="Save changes"
  position="top">
  <ks-button name="Save"></ks-button>
</ks-tooltip>
```