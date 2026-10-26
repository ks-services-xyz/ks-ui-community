# ks-stepper

## Overview

The `ks-stepper` component provides a visual representation of progress through a multi-step process. It supports horizontal and vertical layouts, clickable navigation, completed step indicators, controlled active step management, and optional step descriptions and icons.

In Angular, the component supports two-way binding through the `activeStep` input and `ksStepChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `activeStep` | Currently active step index. Supports Angular two-way binding. | `number` | `0` |
| `clickable` | Allows users to click steps to navigate. | `boolean` | `false` |
| `completedSteps` | Collection of completed step indexes. | `number[]` | `[]` |
| `orientation` | Layout orientation of the stepper. | `"horizontal" \| "vertical"` | `'horizontal'` |
| `steps` | Collection of step definitions. | `KsStepItem[]` | `[]` |

### KsStepItem

```typescript
export interface KsStepItem {
  key: string;
  label: string;
  description?: string;
  icon?: string;
  optional?: boolean;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksStepChange` | Fired when the active step changes. Returns the new step index. | `number` |

# Usage

## React

```tsx
import { KsStepper } from '@kraft.stitch/react';

function App() {
  const steps = [
    {
      key: 'account',
      label: 'Account'
    },
    {
      key: 'profile',
      label: 'Profile'
    },
    {
      key: 'confirmation',
      label: 'Confirmation'
    }
  ];

  return (
    <KsStepper
      steps={steps}
      activeStep={1}
      completedSteps={[0]}
      clickable={true}
    />
  );
}
```

## Angular

```typescript
import { KsStepperComponent } from '@kraft.stitch/angular';
```

```html
<ks-stepper
  [steps]="steps"
  [(activeStep)]="activeStep"
  [completedSteps]="[0]"
  [clickable]="true">
</ks-stepper>
```