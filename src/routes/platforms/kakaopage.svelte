<script>
    import Noticebar from "../../components/noticebar.svelte";
    import PlatformInfo from "../../components/platform/platformInfo.svelte";
    import Heatmap from "../../components/platform/heatmap.svelte"
    import GenreTable from "../../components/platform/genreTable.svelte";
    import MonopolyTable from "../../components/platform/monopolyTable.svelte";
    import UploadPeriodTable from "../../components/platform/uploadPeriodTable.svelte";
    import KeywordsTagsTable from "../../components/platform/keywordsTagsTable.svelte";

    import KakaopageData from "../../../public/jsondata/kakaopage.json"
</script>

<Noticebar noticeMsg="판드, BL 장르는 제외한 정보입니다."/>
<PlatformInfo platformInfoData={KakaopageData.platformInfoData}/>
<Heatmap heatmapData={KakaopageData.heatmapData} platformGenres={KakaopageData.platformInfoData.platformGenres}/>
<GenreTable genreData={KakaopageData.genreData}/>
<MonopolyTable monopolyData={KakaopageData.monopolyData}/>
<UploadPeriodTable weeklyUploadCountData={KakaopageData.weeklyUploadCountData}/>
<KeywordsTagsTable keywordsTagsData={KakaopageData.keywordsTagsData}/>