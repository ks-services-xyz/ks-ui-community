# ks-table

## Overview

The `ks-table` component provides a flexible way to display structured data in a tabular format. It supports customizable columns, column labels, row interactions, responsive scrolling, hover states, and multiple visual styles for presenting data efficiently.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `caption` | Title or caption displayed above the table. | `string` | `''` |
| `columnLabels` | Custom display labels for columns. | `Record<string, string>` | `{}` |
| `columns` | Explicit column order. If not specified, columns are derived from the first data row. | `string[]` | `[]` |
| `data` | Collection of records displayed as table rows. | `Record<string, any>[]` | `[]` |
| `hoverable` | Highlights table rows on hover. | `boolean` | `true` |
| `scrollable` | Enables horizontal scrolling when content overflows. | `boolean` | `true` |
| `size` | Table row size. | `"sm" \| "md" \| "lg"` | `'md'` |
| `variant` | Visual table style. | `"default" \| "striped" \| "bordered" \| "compact"` | `'default'` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `rowClick` | Fired when a table row is clicked. Returns the selected row data. | `any` |

# Usage

## React

```tsx
import { KsTable } from '@kraft.stitch/react';

function App() {
  const data = [
    { id: 1, name: 'John Doe', role: 'Developer' },
    { id: 2, name: 'Jane Smith', role: 'Designer' }
  ];

  return (
    <KsTable
      caption="Team Members"
      data={data}
      hoverable={true}
      variant="striped"
    />
  );
}
```

## Angular

```typescript
import { KsTableComponent } from '@kraft.stitch/angular';
```

```html
<ks-table
  caption="Team Members"
  [data]="data"
  [hoverable]="true"
  variant="striped">
</ks-table>
```