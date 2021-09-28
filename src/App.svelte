<script>
  import Calculator from "./components/Calculator.svelte";
  import TodoList from "./components/TodoList.svelte";
  import Select from "./components/Select.svelte";

  const options = [
    "",
    "Red",
    { label: "Green" },
    { label: "Blue", value: "b" },
  ];

  let selected;

  const handleSelect = (event) => (selected = event.detail);
</script>

<!-- <Calculator/> -->
<!-- <TodoList/> -->
<Select {options} on:select={handleSelect} />
{#if selected}
  <div>You selected {selected}.</div>
{/if}
