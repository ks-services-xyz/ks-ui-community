# ks-pagination

## Overview

The `ks-pagination` component helps users navigate through large datasets by splitting content into multiple pages. It supports page navigation, page size selection, quick page jumping, configurable page button counts, and controlled pagination state management.

In Angular, the component supports two-way binding through the `currentPage` input and `ksPageChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `currentPage` | Current active page. Supports Angular two-way binding. | `number` | `1` |
| `maxPageButtons` | Maximum number of page buttons displayed. | `number` | `7` |
| `pageSize` | Number of items displayed per page. | `number` | `10` |
| `pageSizeOptions` | Available page size options. | `number[]` | `[10, 20, 50, 100]` |
| `showPageSize` | Displays the page size selector. | `boolean` | `false` |
| `showQuickJumper` | Displays a quick page navigation input. | `boolean` | `false` |
| `total` | Total number of items. | `number` | `0` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksPageChange` | Fired when the current page changes. | `number` |
| `ksPageSizeChange` | Fired when the page size changes. | `number` |

# Usage

## React

```tsx
import { KsPagination } from '@kraft.stitch/react';

function App() {
  return (
    <KsPagination
      total={250}
      currentPage={1}
      pageSize={10}
      showPageSize={true}
      showQuickJumper={true}
    />
  );
}
```

## Angular

```typescript
import { KsPaginationComponent } from '@kraft.stitch/angular';
```

```html
<ks-pagination
  [total]="250"
  [(currentPage)]="currentPage"
  [pageSize]="10"
  [showPageSize]="true"
  [showQuickJumper]="true">
</ks-pagination>
```