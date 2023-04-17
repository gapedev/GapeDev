<script>
  import Tabs from "$lib/tabs.svelte";
  import ProjectsTab from "$lib/home/projectsTab.svelte";
  import portfolioTab from "$lib/home/portfolioTab.svelte";

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
