<script>
  import portfolioTab from "$lib/portfolioTab.svelte";
  import Tabs from "$lib/tabs.svelte";
  import ProjectsTab from "$lib/projectsTab.svelte";

  export const items = [
    {
      label: "Portfolio",
      value: 1,
      component: portfolioTab,
    },
    {
      label: "Projects",
      value: 2,
      component: ProjectsTab,
    },
  ];
</script>

<Tabs {items} />
