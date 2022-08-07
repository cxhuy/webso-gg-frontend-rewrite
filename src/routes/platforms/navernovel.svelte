<script>
    // import Noticebar from "../../components/noticebar.svelte";
    import PlatformInfo from "../../components/platform/platformInfo.svelte";
    import Heatmap from "../../components/platform/heatmap.svelte"
    import GenreTable from "../../components/platform/genreTable.svelte";
    import UploadPeriodTable from "../../components/platform/uploadPeriodTable.svelte";

    import NavernovelData from "../../../public/jsondata/navernovel.json"
</script>

<!-- <Noticebar noticeMsg="네이버 웹소설은 최신화 조회수만 제공되고 있습니다."/> -->
<PlatformInfo platformInfoData={NavernovelData.platformInfoData}/>
<Heatmap heatmapData={NavernovelData.heatmapData} platformGenres={NavernovelData.platformInfoData.platformGenres}/>
<GenreTable genreData={NavernovelData.genreData}/>
<UploadPeriodTable weeklyUploadCountData={NavernovelData.weeklyUploadCountData}/>
