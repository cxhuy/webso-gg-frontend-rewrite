<script>
    export let weeklyUploadCountData;
</script>

<div class="container px-3 py-2.5 mt-6">
    <div>
        <span class="text-3xl font-light dark:text-gray-200">연재 주기에 따른 통계</span>
    </div>
    <div class="hidden lg:block">
        <table class="mt-3 w-full table-auto font-light dark:text-gray-200">
            <thead class="bg-black bg-opacity-10 dark:bg-white dark:bg-opacity-10">
                <tr class="text-left">
                    <th class="p-3 font-normal">연재 주기</th>
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
                {#each Object.keys(weeklyUploadCountData) as weeklyUploadCount}
                    <tr class="bg-black bg-opacity-5 dark:bg-white dark:bg-opacity-5">
                        {#if weeklyUploadCount == "7"}
                            <td class="p-3">주 {weeklyUploadCount}회 이상</td>
                        {:else}
                            <td class="p-3">주 {weeklyUploadCount}회</td>
                        {/if}
                        {#each Object.values(weeklyUploadCountData[weeklyUploadCount]) as data}
                            <td class="p-3">{data.toLocaleString()}</td>
                        {/each}
                    </tr>
                {/each}
            </tbody>
        </table>
    </div>
    <div class="lg:hidden">
        {#each Object.keys(weeklyUploadCountData) as weeklyUploadCount}
            <div class="mt-3 p-3 font-light rounded-md dark:text-gray-200 bg-black bg-opacity-5 dark:bg-white dark:bg-opacity-5">
                {#if weeklyUploadCount == "7"}
                    <div class="text-xl">주 {weeklyUploadCount}회 이상</div>
                {:else}
                    <div class="text-xl">주 {weeklyUploadCount}회</div>
                {/if}
                <div class="mt-auto ml-auto">{weeklyUploadCountData[weeklyUploadCount]["novelCount"].toLocaleString()} 작품</div>
                <div class="mt-2 grid grid-cols-2">
                    <div><span class="text-gray-600 dark:text-gray-400">조회수: </span>{weeklyUploadCountData[weeklyUploadCount]["totalViews"].toLocaleString()}</div>
                    <div class="ml-4"><span class="text-gray-600 dark:text-gray-400">평균 조회수: </span>{weeklyUploadCountData[weeklyUploadCount]["avgViews"].toLocaleString()}</div>
                </div>
                <div class="grid grid-cols-2">
                    <div><span class="text-gray-600 dark:text-gray-400">좋아요 수: </span>{weeklyUploadCountData[weeklyUploadCount]["totalLikes"].toLocaleString()}</div>
                    <div class="ml-4"><span class="text-gray-600 dark:text-gray-400">평균 좋아요 수: </span>{weeklyUploadCountData[weeklyUploadCount]["avgLikes"].toLocaleString()}</div>
                </div>
                <div class="grid grid-cols-2">
                    <div><span class="text-gray-600 dark:text-gray-400">선작수: </span>{weeklyUploadCountData[weeklyUploadCount]["totalFavs"].toLocaleString()}</div>
                    <div class="ml-4"><span class="text-gray-600 dark:text-gray-400">평균 선작수: </span>{weeklyUploadCountData[weeklyUploadCount]["avgFavs"].toLocaleString()}</div>
                </div>
            </div>
        {/each}
    </div>
</div>
