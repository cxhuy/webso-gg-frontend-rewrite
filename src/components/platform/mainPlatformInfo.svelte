<script>
    export let platformInfo;
    export let platformPageName;
</script>

<a href="#/platforms/{platformPageName}">
    <div class="w-full mx-auto mt-3 p-3 font-light rounded-md text-gray-200 bg-white bg-opacity-5 text-center">
        <div class="text-2xl font-medium">{platformInfo.platformName}</div>
        <div class="mt-2 grid grid-cols-2">
            <div><span class="text-gray-400">총 조회수: </span>{platformInfo.totalViews.toLocaleString()}</div>
            <div class="ml-4"><span class="text-gray-400">총 작품수: </span>{platformInfo.totalNovels.toLocaleString()}</div>
        </div>
        <div class="mt-2 grid grid-cols-2">
            <div><span class="text-gray-400">평균 조회수: </span>{platformInfo.avgViews.toLocaleString()}</div>
            <div class="ml-4"><span class="text-gray-400">평균 연재수: </span>{platformInfo.avgChapters.toLocaleString()}</div>
        </div>
        <div class="mt-4 text-sm font-extralight text-gray-400">눌러서 더 많은 정보 보기</div>
    </div>
</a>