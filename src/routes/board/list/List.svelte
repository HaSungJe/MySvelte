<script>
    export let data;
</script>

<table>
    <colgroup>
        <col />
        <col />
        <col />
    </colgroup>
    <thead>
        <tr>
            <th>번호</th>
            <th>이름</th>
            <th>랜덤숫자</th>
        </tr>
    </thead>
    <tbody>
        {#each data as item}
            <tr>
                <td>{item.number}</td>
                <td>{item.name}</td>
                <td>{item.random}</td>
            </tr>
        {/each}
    </tbody>
</table>