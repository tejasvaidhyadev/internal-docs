# Nolano.AI Documentation Styling Guide

This guide outlines the consistent styling approach used throughout the Nolano.AI Mintlify documentation.

## Color Palette & Branding

### Primary Brand Colors
- **Primary**: `#935095` (Purple) - Main brand color
- **Light**: `#B47BB6` (Light Purple) - Secondary accents  
- **Dark**: `#6F3A71` (Dark Purple) - Emphasis and contrast
- **Gradient**: From `#935095` to `#B47BB6` for anchors

### Brand Assets
- **Logo System**: Dual-mode logos for light/dark themes
  - Light mode: `logos/logo_docs_light.png`
  - Dark mode: `logos/logo_docs_dark.png` 
- **Favicon**: `logos/favicon-light.png`

## Typography System

### Font Stack
- **Primary**: Inter, system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif
- **Code**: 'JetBrains Mono', 'Fira Code', 'Monaco', 'Cascadia Code', 'Roboto Mono', Consolas, 'Courier New', monospace

### Heading Hierarchy
- **H1**: Large, bold, tight line-height - Page titles
- **H2**: 2xl, semibold, tight - Major sections  
- **H3**: xl, semibold, normal - Subsections
- **H4**: lg, medium, normal - Component titles

## Visual Component Guidelines

### Card Layouts
Use consistent card patterns with purple color scheme:

```mdx
<CardGroup cols={2}>
  <Card 
    title="Feature Name" 
    icon="icon-name"
    color="#935095"
    href="/optional-link"
  >
    Brief description of the feature or benefit
  </Card>
</CardGroup>
```

**Color Rotation Pattern:**
- Primary cards: `#935095`
- Secondary cards: `#B47BB6`  
- Tertiary cards: `#6F3A71`
- Continue rotation for multiple cards

### Interactive Elements

**Steps Component:**
```mdx
<Steps>
  <Step title="Step Name">
    Content with code examples and explanations
  </Step>
</Steps>
```

**Tabs for Alternatives:**
```mdx
<Tabs>
  <Tab title="Option A">
    Content for first approach
  </Tab>
  <Tab title="Option B">
    Content for alternative approach
  </Tab>
</Tabs>
```

**Accordions for Details:**
```mdx
<AccordionGroup>
  <Accordion title="Advanced Topic">
    Detailed explanation that can be collapsed
  </Accordion>
</AccordionGroup>
```

### Code Documentation

**Multi-Language Examples:**
```mdx
<CodeGroup>

```python Python Example
# Python code here
```

```bash CLI Usage
# Command line examples
```

```javascript JavaScript
// JavaScript examples
```

</CodeGroup>
```

**API Parameter Documentation:**
```mdx
<ParamField path="parameter_name" type="str" required>
  Description of the parameter with usage details
</ParamField>

<ParamField path="optional_param" type="int" default="42">
  Optional parameter with default value
</ParamField>
```

### Callout Components

**Information Hierarchy:**
- `<Note>`: General information and tips
- `<Tip>`: Helpful suggestions and best practices  
- `<Warning>`: Important cautions and limitations
- `<Info>`: Additional context and explanations

### Image Standards

**Important: Always Use Absolute Paths**
- Use paths starting with `/` (e.g., `/logos/logo.png`) 
- This ensures images work correctly from any subdirectory
- Avoid relative paths like `logos/logo.png` or `../logos/logo.png`

**Framed Images:**
```mdx
<Frame>
  <img src="/logos/cube_exploded_hero.png" alt="Descriptive alt text" />
</Frame>
```

**Dual-Mode Images:**
```mdx
<img className="block dark:hidden" src="/logos/logo_docs_light.png" alt="Light mode" />
<img className="hidden dark:block" src="/logos/logo_docs_dark.png" alt="Dark mode" />
```

**Available Logo Assets:**
- Hero image: `/logos/cube_exploded_hero.png`
- Light mode logo: `/logos/logo_docs_light.png`
- Dark mode logo: `/logos/logo_docs_dark.png`
- Favicon: `/logos/favicon-light.png`
- Main logo: `/logos/logo.avif`

## Content Organization

### Navigation Structure
1. **Get Started** - Introduction and quickstart
2. **Core Concepts** - Fundamental topics
3. **Tutorials** - Step-by-step guides
4. **API Reference** - Technical documentation

### Page Structure Pattern
1. **Title and Description** (frontmatter)
2. **Hero Content** (overview/introduction)
3. **Main Content** (organized in logical sections)
4. **Interactive Examples** (code samples)
5. **Best Practices** (guidelines and tips)
6. **Next Steps** (navigation to related topics)

## Implementation Standards

### Consistency Rules
- All cards in a group should use the color rotation pattern
- Icons should be semantic and consistent across similar content
- Links should use purple theme colors for hover states
- Code examples should be complete and runnable

### Accessibility
- All images include descriptive alt text
- Color combinations meet WCAG contrast requirements  
- Interactive elements have proper focus states
- Content hierarchy uses semantic heading structure

### Mobile Responsiveness
- Card groups automatically stack on smaller screens
- Code blocks are horizontally scrollable
- Navigation collapses appropriately
- Text scales properly across devices

## Usage Examples

### Feature Showcase Page
```mdx
# Page Title

<Note>Brief overview or target audience</Note>

Main description with **bold key points**.

## Key Features

<CardGroup cols={2}>
  <Card title="Feature 1" icon="icon" color="#935095">
    Feature description
  </Card>
  <Card title="Feature 2" icon="icon" color="#B47BB6">
    Feature description  
  </Card>
</CardGroup>

## Examples

<CodeGroup>
```python Example 1
# Code here
```

```bash CLI
# Commands here
```
</CodeGroup>

<Tip>
  Helpful advice for users
</Tip>
```

### API Reference Page
```mdx
# ComponentName

<ParamField path="required_param" type="str" required>
  Description of required parameter
</ParamField>

<ParamField path="optional_param" type="int" default="42">
  Description with default value
</ParamField>

## Examples

<CodeGroup>
```python Basic Usage
# Example implementation
```
</CodeGroup>
```

This styling guide ensures consistent, professional, and accessible documentation across the entire Nolano.AI platform.
