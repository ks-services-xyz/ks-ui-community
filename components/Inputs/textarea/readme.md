# ks-textarea

## Overview

The `ks-textarea` component provides a multi-line text input for collecting longer form content from users. It supports auto-resizing, validation states, helper text, character counting, configurable row sizes, disabled states, and controlled value management.

In Angular, the component supports two-way binding through the `value` input and `ksValueChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `autoResize` | Automatically resizes the textarea based on its content. | `boolean` | `false` |
| `disabled` | Disables the component. | `boolean` | `false` |
| `error` | Error message displayed below the textarea and activates the error state. | `string` | `''` |
| `hint` | Helper text displayed below the textarea. | `string` | `''` |
| `label` | Label displayed above the textarea. | `string` | `''` |
| `maxLength` | Maximum number of characters allowed. | `number` | `500` |
| `placeholder` | Placeholder text displayed when the textarea is empty. | `string` | `''` |
| `rows` | Number of visible text rows. | `number` | `3` |
| `showCounter` | Displays the current character count. | `boolean` | `false` |
| `value` | Current textarea value. Supports Angular two-way binding. | `string` | `''` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksBlur` | Fired when the textarea loses focus. | `void` |
| `ksValueChange` | Fired when the textarea value changes. | `string` |

# Usage

## React

```tsx
import { KsTextarea } from '@kraft.stitch/react';

function App() {
  return (
    <KsTextarea
      label="Description"
      placeholder="Enter description"
      rows={4}
      value=""
    />
  );
}
```

## Angular

```typescript
import { KsTextareaComponent } from '@kraft.stitch/angular';
```

```html
<ks-textarea
  label="Description"
  placeholder="Enter description"
  [rows]="4"
  [(value)]="description">
</ks-textarea>
```