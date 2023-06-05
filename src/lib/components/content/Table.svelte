<script lang="ts">
    export let headers: any[]
    export let data: any[]
</script>

<table>
    <thead>
        <tr>
            {#each headers as header}
                <th>{header}</th>
            {/each}
        </tr>
    </thead>
    <tbody>
        {#each data as row}
            <tr>
                {#each row as cell}
                    <td>{cell}</td>
                {/each}
            </tr>
        {/each}
    </tbody>
</table>

<style>
    table {
        border-collapse: collapse;
        background: var(--color-background-alt);
    }

    tr {
        border-bottom: 1px solid var(--color-border);
    }

    th, td {
        text-align: left;
        padding: var(--space-inset-1);
    }
</style>