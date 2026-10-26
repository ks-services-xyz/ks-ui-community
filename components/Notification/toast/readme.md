# ks-toast-outlet

## Overview

The `ks-toast-outlet` component provides a centralized container for displaying toast notifications. It automatically renders and manages toast messages created through the toast store, allowing applications to display success, warning, error, and informational messages in a consistent location.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `position` | Position where toast notifications appear on the screen. | `"top-left" \| "top-center" \| "top-right" \| "bottom-left" \| "bottom-center" \| "bottom-right"` | `'top-right'` |

# Usage

## React

```tsx
import { KsToastOutlet } from '@kraft.stitch/react';
import { toastStore } from '@kraft.stitch/core';

function App() {
  const showToast = () => {
    toastStore.show({
      title: 'Success',
      message: 'Profile updated successfully.',
      variant: 'success'
    });
  };

  return (
    <>
      <button onClick={showToast}>
        Show Toast
      </button>

      <KsToastOutlet position="top-right" />
    </>
  );
}
```

## Angular

```typescript
import { KsToastOutletComponent } from '@kraft.stitch/angular';
```

```html
<button (click)="showToast()">
  Show Toast
</button>

<ks-toast-outlet
  position="top-right">
</ks-toast-outlet>
```

```typescript
showToast(): void {
  toastStore.show({
    title: 'Success',
    message: 'Profile updated successfully.',
    variant: 'success'
  });
}
```