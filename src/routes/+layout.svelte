<script lang="ts">
    import '../app.css';

    function toggleMenu(event: MouseEvent) {
        const target = event.target as HTMLElement;
        if (target.parentElement?.children[1].classList.contains('hidden')) {
            target.parentElement?.children[1].classList.remove('hidden');
        } else {
            target.parentElement?.children[1].classList.add('hidden');
        }
    }
</script>

<body class="bg-gray-100">
	<!-- 상단 -->
	<div class="bg-red-300 p-5">
		상단영역
	</div>
	<!-- //상단 -->

    <div class="flex min-h-screen">
		<!-- 메뉴 -->
		<div class="w-1/6 bg-white shadow-lg">
			<nav>
				<ul>
					<li>
						<span class="font-bold">
							<a href="/" class="block text-gray-800 hover:bg-gray-200">HOME</a>
						</span>
					</li>

					<li>
						<span class="font-bold">
							<a href="/board/list" class="block text-gray-800 hover:bg-gray-200" on:click={toggleMenu}>게시판</a>
							<ul class="w-1/6 absolute hidden">
								<li>
									<span class="font-bold">
										<a href="/board/list" class="block text-gray-800 hover:bg-gray-200">게시판 1</a>
									</span>
								</li>
								<li>
									<span class="font-bold">
										<a href="/board/list" class="block text-gray-800 hover:bg-gray-200">게시판 2</a>
									</span>
								</li>
							</ul>
						</span>
					</li>
				</ul>
			</nav>
		</div>
		<!-- //메뉴 -->
        
		<!-- 본문 -->
		<div class="p-10">
			<slot />
		</div>
		<!-- //본문 -->
    </div>

	<!-- 하단 -->
	<div class="bg-red-300 p-5">
		하단영역
	</div>
	<!-- //하단 -->
</body>