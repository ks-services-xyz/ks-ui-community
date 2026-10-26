# Toast Store

## Overview

The `toastStore` provides a simple, framework-agnostic API for displaying toast notifications anywhere in your application. It can be used with React, Angular, or any framework supported by Kraft Stitch.

To render toast notifications, add a `<ks-toast-outlet>` component somewhere in your application layout.

## Methods

### show(message)

Displays a new toast notification.

```typescript
toastStore.show(message: string): void
```

#### Parameters

```typescript
message: string
```

The message text to display in the toast notification.

#### Example

```typescript
toastStore.show('Profile updated successfully.');
```

---

### dismiss(id)

Removes a specific toast notification.

```typescript
toastStore.dismiss(id: string): void
```

#### Parameters

```typescript
id: string
```

The unique identifier of the toast to dismiss.

#### Example

```typescript
toastStore.dismiss(toastId);
```

---

### clear()

Removes all active toast notifications.

```typescript
toastStore.clear(): void
```

#### Example

```typescript
toastStore.clear();
```

---

# Usage

## React

```tsx
import { toastStore } from '@kraft.stitch/react';

function App() {
  const showToast = () => {
    toastStore.show('Hi, how are you?');
  };

  return (
    <button onClick={showToast}>
      Show Toast
    </button>
  );
}
```

### Application Setup

```tsx
import { KsToastOutlet } from '@kraft.stitch/react';

function App() {
  return (
    <>
      <KsToastOutlet position="top-right" />
      {/* Application Content */}
    </>
  );
}
```

---

## Angular

```typescript
import { tostStore } from '@kraft.stitch/angular';

export class AppComponent {
  showToast(): void {
    toastStore.show('Hello from KS Toast!');
 }
}
```

```html
<button (click)="showToast()">
  Show Toast</button>
```

### Application Setup

```html
<ks-toast-outlet position="top-right"></ks-toast-outlet>
```

---
# ToastOutlet Positions

Supported positions:

```text*top-left
top-center
top-right
bottom-left
bottom-center
bottom-right
```

### Example

```html
<ks-toast-outlet position="bottom-center"></ks-toast-outlet>
```