# ks-otp-input

## Overview

The `ks-otp-input` component provides a dedicated interface for entering one-time passwords (OTP), verification codes, and PINs. It supports configurable lengths, numeric or text input modes, optional masking, validation states, disabled states, and controlled value management.

In Angular, the component supports two-way binding through the `value` input and `ksValueChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `disabled` | Disables the component. | `boolean` | `false` |
| `error` | Error message displayed below the component. | `string` | `''` |
| `inputType` | Input type for each OTP field. | `"number" \| "text"` | `'number'` |
| `label` | Label displayed above the component. | `string` | `''` |
| `length` | Number of OTP digits or characters. | `number` | `6` |
| `masked` | Masks the entered value similar to a password field. | `boolean` | `false` |
| `value` | Current OTP value. Supports Angular two-way binding. | `string` | `''` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `completed` | Fired when all OTP fields have been filled. | `string` |
| `ksValueChange` | Fired when the OTP value changes. | `string` |

## Methods

### writeValue(val)

Programmatically updates the OTP value.

```typescript
writeValue(val: string): Promise<void>
```

# Usage

## React

```tsx
import { KsOtpInput } from '@kraft.stitch/react';

function App() {
  return (
    <KsOtpInput
      label="Verification Code"
      length={6}
      value=""
    />
  );
}
```

## Angular

```typescript
import { KsOtpInputComponent } from '@kraft.stitch/angular';
```

```html
<ks-otp-input
  label="Verification Code"
  [length]="6"
  [(value)]="otp">
</ks-otp-input>
```