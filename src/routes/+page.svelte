<script lang="ts">
    import type { PageData } from './$types'
    import LogIn from '$lib/auth/LogIn.svelte'
    import ReminderList from '$lib/reminders/ReminderList.svelte'

    export let data: PageData
    let loggedIn = true
</script>

<svelte:head>
    <title>Reminders - MyPlanner</title>
    <meta name="description" content="A simple planner for keeping reminders">
</svelte:head>
{#if loggedIn}
    <ReminderList reminders={data.reminders} />
{:else}
    <LogIn />
{/if}
