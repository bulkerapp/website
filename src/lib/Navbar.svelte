<script lang="ts">
    import Fa from "svelte-fa";
    import { faHouse, faCarrot, faBowlFood, faCalendarDays, faRightToBracket, faGear } from "@fortawesome/free-solid-svg-icons";
	import Tooltip from "./Tooltip.svelte";
</script>

<div class="nav">
    <div class="wrapper">
        <Tooltip text="Overview">
            <Fa icon={faHouse} fw size="1.5x"/>
        </Tooltip>
        <Tooltip text="Ingredients">
            <Fa icon={faCarrot} fw size="1.5x"/>
        </Tooltip>
        <Tooltip text="Meals">
            <Fa icon={faBowlFood} fw size="1.5x"/>
        </Tooltip>
        <Tooltip text="Calendar">
            <Fa icon={faCalendarDays} fw size="1.5x"/>
        </Tooltip>
    </div>
    <div class="wrapper bottom">
        <Tooltip text="Settings">
            <Fa icon={faGear} fw size="1.5x"/>
        </Tooltip>
        <Tooltip text="Logout">
            <Fa icon={faRightToBracket} fw size="1.5x"/>
        </Tooltip>
    </div>
</div>

<style>
    .nav {
        display: flex;
        flex-direction: column;
        align-items: center;
        float: left;
        height: 100%;
        border-right: 1px solid #292532;
        width: 4rem;
    }

    .wrapper {
        display: flex;
        flex-direction: column;
        gap: 2.5rem;
        margin: 20px 0;
    }

    .bottom {
        margin-top: auto;
    }
</style>
