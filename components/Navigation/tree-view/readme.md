# ks-tree-view

## Overview

The `ks-tree-view` component displays hierarchical data in a tree structure, allowing users to expand, collapse, and select nodes. It supports single and multi-selection modes, configurable expanded nodes, nested hierarchies, and node-level customization through icons and disabled states.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `expandedKeys` | Keys of nodes that should be expanded initially. | `string[]` | `[]` |
| `multi` | Allows selecting multiple nodes. | `boolean` | `false` |
| `nodes` | Collection of tree nodes. | `KsTreeNode[]` | `[]` |

### KsTreeNode

```typescript
export interface KsTreeNode {
  key: string;
  label: string;
  icon?: string;
  disabled?: boolean;
  children?: KsTreeNode[];
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `expandChange` | Fired when a node is expanded or collapsed. | `{ key: string; expanded: boolean }` |
| `selectionChanged` | Fired when the node selection changes. | `string \| string[]` |

# Usage

## React

```tsx
import { KsTreeView } from '@kraft.stitch/react';

function App() {
  const nodes = [
    {
      key: 'documents',
      label: 'Documents',
      children: [
        {
          key: 'reports',
          label: 'Reports'
        },
        {
          key: 'invoices',
          label: 'Invoices'
        }
      ]
    },
    {
      key: 'settings',
      label: 'Settings'
    }
  ];

  return (
    <KsTreeView
      nodes={nodes}
      expandedKeys={['documents']}
      multi={true}
    />
  );
}
```

## Angular

```typescript
import { KsTreeViewComponent } from '@kraft.stitch/angular';
```

```html
<ks-tree-view
  [nodes]="nodes"
  [expandedKeys]="['documents']"
  [multi]="true">
</ks-tree-view>
```