# ks-dialog

## Overview

The `ks-dialog` component provides a modal dialog interface for displaying content, user interactions, confirmations, forms, and workflows that require focused attention. It supports configurable sizes, custom footer content, persistent mode, controlled visibility, and optional close button behavior.

In Angular, the component supports two-way binding through the `open` input and `ksOpenChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `hideClose` | Hides the built-in close button. | `boolean` | `false` |
| `label` | Dialog title displayed in the header. | `string` | `''` |
| `open` | Controls whether the dialog is visible. Supports Angular two-way binding. | `boolean` | `false` |
| `persistent` | Prevents closing the dialog when clicking outside the panel. | `boolean` | `false` |
| `size` | Dialog size. | `"sm" \| "md" \| "lg" \| "xl" \| "full"` | `'md'` |
| `target` | Target element ID where the dialog should be rendered. Leave empty to render on the document body. | `string` | `''` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksOpenChange` | Fired when the dialog open state changes. | `boolean` |
| `closeDialog` | Fired when the dialog requests to be closed. | `void` |

## Slots

| Slot | Description |
| ---- | ----------- |
| Default | Main dialog content. |
| `footer` | Dialog footer content, typically used for action buttons. |

# Usage

## React

```tsx
import { KsDialog, KsButton } from '@kraft.stitch/react';

function App() {
  return (
    <KsDialog
      label="Delete Item"
      open={true}
      size="md"
    >
      <p>Are you sure you want to delete this item?</p>

      <div slot="footer">
        <KsButton
          name="Cancel"
          variant="neutral"
        />

        <KsButton
          name="Delete"
          variant="danger"
        />
      </div>
    </KsDialog>
  );
}
```

## Angular

```typescript
import { KsDialogComponent } from '@kraft.stitch/angular';
```

```html
<ks-dialog
  label="Delete Item"
  [(open)]="dialogOpen"
  size="md">

  <p>Are you sure you want to delete this item?</p>

  <div slot="footer">
    <ks-button
      name="Cancel"
      variant="neutral">
    </ks-button>

    <ks-button
      name="Delete"
      variant="danger">
    </ks-button>
  </div>

</ks-dialog>
```