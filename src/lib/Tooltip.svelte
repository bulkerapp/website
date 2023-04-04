<script lang="ts">
    export let text: string;
    let isHovered = false;

    function mouseOver(event: MouseEvent) {
        isHovered = true;
    }

    function mouseLeave() {
        isHovered = false;
    }

    $: iconColor = isHovered ? "#d5d3d9" : "#726d7e";
</script>

<div class="wrapper" on:mouseover={mouseOver} on:mouseleave={mouseLeave} style="--icon-color: {iconColor}">
    <slot/>
    {#if isHovered}
        <div class="tooltip">{text}</div>
    {/if}
</div>

<style>
    .wrapper {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0.5em;
        color: var(--icon-color);
        aspect-ratio: 1 / 1;
    }

    .wrapper:hover {
        cursor: pointer;
        background-color: #292532;
        border-radius: 6px;
    }

    .tooltip {
        background-color: #292532;
        border-radius: 6px;

        padding: 7px 15px;
        position: absolute;
        left: 140%;
        top: 50%;
        transform-origin: left;
        transform: translateY(-50%);
        white-space: nowrap;
    }
</style>
