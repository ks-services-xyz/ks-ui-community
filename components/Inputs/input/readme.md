# ks-input

## Overview

The `ks-input` component provides a versatile text input field for collecting user input. It supports multiple input types, validation states, helper text, prefix and suffix icons, size variants, disabled states, and controlled value management.

In Angular, the component supports two-way binding through the `value` input and `ksValueChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `disabled` | Disables the input field. | `boolean` | `false` |
| `error` | Error message displayed below the input and activates the error state. | `string` | `''` |
| `hint` | Helper text displayed below the input. | `string` | `''` |
| `label` | Label displayed above the input. | `string` | `''` |
| `placeholder` | Placeholder text displayed when the input is empty. | `string` | `''` |
| `prefixIcon` | Leading icon displayed inside the input. | `string` | `''` |
| `size` | Input size variant. | `"sm" \| "md" \| "lg" \| "xl"` | `'md'` |
| `suffixIcon` | Trailing icon displayed inside the input. | `string` | `''` |
| `type` | HTML input type. | `"text" \| "email" \| "number" \| "password" \| "search" \| "tel" \| "url"` | `'text'` |
| `value` | Current input value. Supports Angular two-way binding. | `string` | `''` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksBlur` | Fired when the input loses focus. | `void` |
| `ksValueChange` | Fired when the input value changes. | `string` |

# Usage

## React

```tsx
import { KsInput } from '@kraft.stitch/react';

function App() {
  return (
    <KsInput
      label="Username"
      placeholder="Enter username"
      value=""
      prefixIcon="ks-icon-user"
    />
  );
}
```

## Angular

```typescript
import { KsInputComponent } from '@kraft.stitch/angular';
```

```html
<ks-input
  label="Username"
  placeholder="Enter username"
  prefixIcon="ks-icon-user"
  [(value)]="username">
</ks-input>
```