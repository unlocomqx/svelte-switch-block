<script>
  import { Meta, Story, Template } from "@storybook/addon-svelte-csf"
  import Switch from "./Switch.svelte"
  import Case from "./Case.svelte"
  import DefaultCase from "./DefaultCase.svelte"
</script>

<!-- More on default export: https://storybook.js.org/docs/react/writing-stories/introduction#default-export -->
<!-- More on argTypes: https://storybook.js.org/docs/svelte/api/argtypes -->
<Meta
  title="Components/Switch"
  component={Switch}
  argTypes={{}}
/>

<!-- More on component templates: https://storybook.js.org/docs/svelte/writing-stories/introduction#using-args -->
<Template let:args>
  <Switch {...args}>
    <Case value="A">
      ABC
    </Case>
    <Case value="B">
      DEF
    </Case>
    <Case value="C">
      GHI
    </Case>
    <DefaultCase>
      JKL
    </DefaultCase>
  </Switch>
</Template>

<!-- More on args: https://storybook.js.org/docs/svelte/writing-stories/args -->
<Story
  name="Default"
  args={{
    expression: "D"
  }}
/>
