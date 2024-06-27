<script lang="ts">
    function clickMenu(event: MouseEvent) {
        const target = event.target as HTMLElement;
        if (target.classList.contains('close')) {
            target.classList.remove('close');
            target.classList.add('open');
            target.parentElement?.children[1]?.setAttribute('style', 'display: block');
        } else {
            target.classList.remove('open');
            target.classList.add('close');
            target.parentElement?.children[1]?.setAttribute('style', 'display: none;');
        }
    }
</script>

<h1>헤더영역</h1>
<ul>
    <li><button class="close" on:click={clickMenu}>메뉴 1</button>
        <ul style="display: none;">
            <li>메뉴 1-1</li>
            <li>메뉴 1-2</li>
            <li>메뉴 1-3</li>
        </ul>
    </li>
    <li><button class="close" on:click={clickMenu}>메뉴 2</button>
        <ul style="display: none;">
            <li>메뉴 2-1</li>
            <li>메뉴 2-2</li>
            <li>메뉴 2-3</li>
        </ul>
    </li>
    <li><button class="close" on:click={clickMenu}>메뉴 3</button>
        <ul style="display: none;">
            <li>메뉴 3-1</li>
            <li>메뉴 3-2</li>
            <li>메뉴 3-3</li>
        </ul> 
    </li>
</ul>