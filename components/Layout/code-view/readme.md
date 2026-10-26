# ks-code-view

## Overview

The `ks-code-view` component displays formatted source code with optional language labeling, syntax-aware presentation, copy functionality, and expandable/collapsible viewing. It is useful for documentation, code examples, tutorials, and developer-focused interfaces.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `actionButtonConfig` | Controls the visibility of action buttons such as expand and copy code. | `ActionButtonsConfig` | `{ expand: true, code: true }` |
| `code` | Source code content to display. | `string` | `''` |
| `collapsed` | Determines whether the code block is initially collapsed. | `boolean` | `false` |
| `label` | Optional title displayed in the header. | `string` | `''` |
| `language` | Language label displayed in the header. | `"html" \| "typescript" \| "javascript" \| "css" \| "json" \| "bash" \| "text"` | `'html'` |
| `maxHeight` | Maximum visible height before scrolling is enabled. | `string` | `'24rem'` |
| `showHeader` | Displays the header containing the title, language badge, and actions. | `boolean` | `true` |

### ActionButtonsConfig

```typescript
export interface ActionButtonsConfig {
  expand?: boolean;
  code?: boolean;
}
```

# Usage

## React

```tsx
import { KsCodeView } from '@kraft.stitch/react';

function App() {
  return (
    <KsCodeView
      label="Button Example"
      language="typescript"
      code={`const button = 'Hello World';`}
    />
  );
}
```

## Angular

```typescript
import { KsCodeViewComponent } from '@kraft.stitch/angular';
```

```html
<ks-code-view
  label="Button Example"
  language="typescript"
  [code]="sourceCode">
</ks-code-view>
```