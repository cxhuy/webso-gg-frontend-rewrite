<script>
    import MainPlatformInfo from "../components/platform/mainPlatformInfo.svelte";

    import MunpiaData from "../../public/jsondata/munpia.json"
    import NovelpiaData from "../../public/jsondata/novelpia.json"
    import KakaopageData from "../../public/jsondata/kakaopage.json"
    import KakaostageData from "../../public/jsondata/kakaostage.json"
    import NavernovelData from "../../public/jsondata/navernovel.json"
</script>

<svelte:head>
    <title>웹소지지</title>
</svelte:head>
<div class="container px-3 py-2.5 mt-6 flex flex-col">
    <div class="mx-auto dark:text-gray-200 text-6xl">웹소지지</div>
    <div class="mx-auto my-2 text-gray-600 dark:text-gray-400">웹소지지는 최근 1주일 내에 연재 기록이 있는 작품들을 기준으로 데이터를 제공합니다.</div>
    <MainPlatformInfo platformInfo={MunpiaData.platformInfoData} platformPageName="munpia"/>
    <MainPlatformInfo platformInfo={NovelpiaData.platformInfoData} platformPageName="novelpia"/>
    <MainPlatformInfo platformInfo={KakaopageData.platformInfoData} platformPageName="kakaopage"/>
    <MainPlatformInfo platformInfo={KakaostageData.platformInfoData} platformPageName="kakaostage"/>
    <MainPlatformInfo platformInfo={NavernovelData.platformInfoData} platformPageName="navernovel"/>
</div>