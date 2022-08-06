<script>
    export let monopolyData;
</script>

<div class="container px-3 py-2.5 mt-6">
    <div>
        <span class="text-3xl font-light dark:text-gray-200">독점 여부에 따른 통계</span>
    </div>
    <div class="hidden lg:block">
        <table class="mt-3 w-full table-auto font-light dark:text-gray-200">
            <thead class="bg-black bg-opacity-10 dark:bg-white dark:bg-opacity-10">
                <tr class="text-left">
                    <th class="p-3 font-normal">독점 여부</th>
                    <th class="p-3 font-normal">작품수</th>
                    <th class="p-3 font-normal">조회수</th>
                    <th class="p-3 font-normal">평균 조회수</th>
                    <th class="p-3 font-normal">좋아요 수</th>
                    <th class="p-3 font-normal">평균 좋아요 수</th>
                    <th class="p-3 font-normal">선작수</th>
                    <th class="p-3 font-normal">평균 선작수</th>
                </tr>
            </thead>
            <tbody>
                {#each Object.keys(monopolyData) as monopoly}
                    <tr class="bg-black bg-opacity-5 dark:bg-white dark:bg-opacity-5">
                        <td class="p-3">{monopoly}</td>
                        {#each Object.values(monopolyData[monopoly]) as data}
                            <td class="p-3">{data.toLocaleString()}</td>
                        {/each}
                    </tr>
                {/each}
            </tbody>
        </table>
    </div>
    <div class="lg:hidden">
        {#each Object.keys(monopolyData) as monopoly}
            <div class="mt-3 p-3 font-light rounded-md dark:text-gray-200 bg-black bg-opacity-5 dark:bg-white dark:bg-opacity-5">
                <div class="text-xl">{monopoly}</div>
                <div class="mt-auto ml-auto">{monopolyData[monopoly]["novelCount"].toLocaleString()} 작품</div>
                <div class="mt-2 grid grid-cols-2">
                    <div><span class="text-gray-600 dark:text-gray-400">조회수: </span>{monopolyData[monopoly]["totalViews"].toLocaleString()}</div>
                    <div class="ml-4"><span class="text-gray-600 dark:text-gray-400">평균 조회수: </span>{monopolyData[monopoly]["avgViews"].toLocaleString()}</div>
                </div>
                <div class="grid grid-cols-2">
                    <div><span class="text-gray-600 dark:text-gray-400">좋아요 수: </span>{monopolyData[monopoly]["totalLikes"].toLocaleString()}</div>
                    <div class="ml-4"><span class="text-gray-600 dark:text-gray-400">평균 좋아요 수: </span>{monopolyData[monopoly]["avgLikes"].toLocaleString()}</div>
                </div>
                <div class="grid grid-cols-2">
                    <div><span class="text-gray-600 dark:text-gray-400">선작수: </span>{monopolyData[monopoly]["totalFavs"].toLocaleString()}</div>
                    <div class="ml-4"><span class="text-gray-600 dark:text-gray-400">평균 선작수: </span>{monopolyData[monopoly]["avgFavs"].toLocaleString()}</div>
                </div>
            </div>
        {/each}
    </div>
</div>
