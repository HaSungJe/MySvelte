<script lang="ts">
    import { onMount } from 'svelte';
    import List from './List.svelte';

    let data: Array<object> = [
        { number: 1, name: '회원 1', random: 1 }, 
        { number: 2, name: '회원 2', random: 2 }, 
        { number: 3, name: '회원 3', random: 3 },
        { number: 4, name: '회원 4', random: 4 }, 
        { number: 5, name: '회원 5', random: 5 }, 
        { number: 6, name: '회원 6', random: 6 }, 
        { number: 7, name: '회원 7', random: 7 }, 
        { number: 8, name: '회원 8', random: 8 }, 
        { number: 9, name: '회원 9', random: 9 }, 
        { number: 10, name: '회원 10', random: 10 }
    ];

    async function list() {
        data = [];
        for (let i=0; i<10; i++) {
            data.push({
                number: i+1,
                name: `회원 ${i+1}`,
                random: Math.random() * 100
            });
        }
    }
</script>

<h3>목록</h3>
<button on:click={list}>검색</button>

<!-- 목록 -->
<List data={data}/>