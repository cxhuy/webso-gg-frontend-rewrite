<script>
    import PlatformInfo from "../../components/platform/platform-info.svelte";
    import Heatmap from "../../components/platform/heatmap.svelte"
    import GenreTable from "../../components/platform/genreTable.svelte";
    import MonopolyTable from "../../components/platform/monopolyTable.svelte";
    import UploadPeriodTable from "../../components/platform/uploadPeriodTable.svelte";
    import PricingTable from "../../components/platform/pricingTable.svelte";
    import KeywordsTagsTable from "../../components/platform/keywordsTagsTable.svelte";

    import NovelpiaData from "../../jsondata/novelpia.json"
</script>

<PlatformInfo platformInfoData={NovelpiaData.platformInfoData}/>
<Heatmap heatmapData={NovelpiaData.heatmapData} platformGenres={NovelpiaData.platformInfoData.platformGenres}/>
<GenreTable genreData={NovelpiaData.genreData}/>
<MonopolyTable monopolyData={NovelpiaData.monopolyData}/>
<UploadPeriodTable weeklyUploadCountData={NovelpiaData.weeklyUploadCountData}/>
<PricingTable pricingData={NovelpiaData.pricingData}/>
<KeywordsTagsTable keywordsTagsData={NovelpiaData.keywordsTagsData}/>