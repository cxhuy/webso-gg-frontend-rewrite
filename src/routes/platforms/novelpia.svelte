<script>
    import Noticebar from "../../components/noticebar.svelte";
    import PlatformInfo from "../../components/platform/platformInfo.svelte";
    import Heatmap from "../../components/platform/heatmap.svelte"
    import GenreTable from "../../components/platform/genreTable.svelte";
    import MonopolyTable from "../../components/platform/monopolyTable.svelte";
    import UploadPeriodTable from "../../components/platform/uploadPeriodTable.svelte";
    import PricingTable from "../../components/platform/pricingTable.svelte";
    import KeywordsTagsTable from "../../components/platform/keywordsTagsTable.svelte";

    import NovelpiaData from "../../../public/jsondata/novelpia.json"
</script>

<Noticebar noticeMsg="19금 작품은 제외한 정보입니다."/>
<PlatformInfo platformInfoData={NovelpiaData.platformInfoData}/>
<Heatmap heatmapData={NovelpiaData.heatmapData} platformGenres={NovelpiaData.platformInfoData.platformGenres}/>
<GenreTable genreData={NovelpiaData.genreData}/>
<MonopolyTable monopolyData={NovelpiaData.monopolyData}/>
<UploadPeriodTable weeklyUploadCountData={NovelpiaData.weeklyUploadCountData}/>
<PricingTable pricingData={NovelpiaData.pricingData}/>
<KeywordsTagsTable keywordsTagsData={NovelpiaData.keywordsTagsData}/>