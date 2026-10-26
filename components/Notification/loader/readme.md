# ks-loader

## Overview

The `ks-loader` component provides a simple way to handle loading, empty, error, and success states within an application. It supports built-in visual states while allowing complete customization through slots for loading, empty, and error content.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `state` | Current loader state. | `LoaderStateEnum.Loading \| LoaderStateEnum.Success \| LoaderStateEnum.Empty \| LoaderStateEnum.Error` | `LoaderStateEnum.Loading` |

### LoaderStateEnum

```typescript
export enum LoaderStateEnum {
  Loading = 'loading',
  Success = 'success',
  Empty = 'empty',
  Error = 'error'
}
```

## Slots

| Slot | Description |
| ---- | ----------- |
| Default | Content displayed when the state is `Success`. |
| `loading` | Custom loading state content. |
| `empty` | Custom empty state content. |
| `empty-action` | Actions displayed within the empty state. |
| `error` | Custom error state content. |
| `error-action` | Actions displayed within the error state. |

# Usage

## React

```tsx
import { KsLoader } from '@kraft.stitch/react';

function App() {
  return (
    <KsLoader state="loading">
      <div>Loaded Content</div>
    </KsLoader>
  );
}
```

### Custom Empty State

```tsx
<KsLoader state="empty">
  <div slot="empty">
    No records found
  </div>

  <button slot="empty-action">
    Create Record
  </button>
</KsLoader>
```

### Custom Error State

```tsx
<KsLoader state="error">
  <div slot="error">
    Something went wrong
  </div>

  <button slot="error-action">
    Retry
  </button>
</KsLoader>
```

## Angular

```typescript
import { KsLoaderComponent } from '@kraft.stitch/angular';
```

```html
<ks-loader state="loading">
  <div>Loaded Content</div>
</ks-loader>
```

### Custom Empty State

```html
<ks-loader state="empty">

  <div slot="empty">
    No records found
  </div>

  <button slot="empty-action">
    Create Record
  </button>

</ks-loader>
```

### Custom Error State

```html
<ks-loader state="error">

  <div slot="error">
    Something went wrong
  </div>

  <button slot="error-action">
    Retry
  </button>

</ks-loader>
```