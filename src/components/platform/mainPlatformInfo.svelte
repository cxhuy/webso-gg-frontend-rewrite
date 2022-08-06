<script>
    export let platformInfo;
    export let platformPageName;
</script>

<a href="/platforms/{platformPageName}">
    <div class="w-full lg:w-2/3 mx-auto mt-3 p-3 font-light rounded-md dark:text-gray-200 bg-black bg-opacity-5 dark:bg-white dark:bg-opacity-5">
        <div class="text-xl">{platformInfo.platformName}</div>
        <div class="mt-2 grid grid-cols-2">
            <div><span class="text-gray-600 dark:text-gray-400">총 조회수: </span>{platformInfo.totalViews.toLocaleString()}</div>
            <div class="ml-4"><span class="text-gray-600 dark:text-gray-400">총 작품수: </span>{platformInfo.totalNovels.toLocaleString()}</div>
        </div>
        <div class="mt-2 grid grid-cols-2">
            <div><span class="text-gray-600 dark:text-gray-400">평균 조회수: </span>{platformInfo.avgViews.toLocaleString()}</div>
            <div class="ml-4"><span class="text-gray-600 dark:text-gray-400">평균 연재수: </span>{platformInfo.avgChapters.toLocaleString()}</div>
        </div>
        <div class="mt-4 text-sm font-extralight text-gray-600 dark:text-gray-400">눌러서 더 많은 정보 보기</div>
    </div>
</a>