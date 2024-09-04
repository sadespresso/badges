# Storybook Addon - Badges

Annotate your stories with badges

## Usage

### Define presets

By default, there are few badges. See [defaults.ts](./src/defaults.ts)

```typescript
// preview.ts

const preview: Preview = {
  parameters: {
    badgePresets: {
      beta: {
        title: "Beta",
        description: "Not quite ready for prime time",
        style: {
          color: "#ffffff",
          backgroundColor: "#9c88ff",
        },
      },
      stable: {
        title: "Stable",
        description: "Ready for production",
        style: {
          color: "#ffffff",
          backgroundColor: "#44bd32",
        },
      },
    },
  },
};
```

### Specify in story params

#### For all stories of same component

```typescript
// MyComponent.stories.tsx

// 👇 This default export determines where your story goes in the story list
const meta: Meta<typeof MyComponent> = {
  component: MyComponent,
  parameters: {
    badges: [
      "beta", // Defined in `preview.ts`
      {
        title: "Sep 1",
        description: "Back to school special",
        style: {
          color: "#050505",
          backgroundColor: "#DBACFF",
        },
      },
    ]
  }
}
```

### Contributing

PRs are welcome

> 2024 Sep 4, totally worth to have it done even tho I was late to work few hours
