<script>
    import * as Foo from "$lib/foo";
    import Item from "$lib/foo/item.svelte";

    let error = $state(undefined);
</script>

<input
    oninput={(e) => {
        error = e.target.value === "e" ? "my error" : undefined;
    }}
/>

{#if error}
    <Foo.Item>Error</Foo.Item>
    <Item>Error</Item>
{:else}
    <Foo.Item>Message</Foo.Item>
    <Item>Message</Item>
{/if}
