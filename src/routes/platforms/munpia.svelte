<script>
    import PlatformInfo from "../../components/platform/platform-info.svelte";
    import Heatmap from "../../components/platform/heatmap.svelte"
    import GenreTable from "../../components/platform/genreTable.svelte";
    import MonopolyTable from "../../components/platform/monopolyTable.svelte";
    import UploadPeriodTable from "../../components/platform/uploadPeriodTable.svelte";
    import PricingTable from "../../components/platform/pricingTable.svelte";
    import KeywordsTagsTable from "../../components/platform/keywordsTagsTable.svelte";

    import MunpiaData from "../../../public/jsondata/munpia.json"
</script>

<PlatformInfo platformInfoData={MunpiaData.platformInfoData}/>
<Heatmap heatmapData={MunpiaData.heatmapData} platformGenres={MunpiaData.platformInfoData.platformGenres}/>
<GenreTable genreData={MunpiaData.genreData}/>
<MonopolyTable monopolyData={MunpiaData.monopolyData}/>
<UploadPeriodTable weeklyUploadCountData={MunpiaData.weeklyUploadCountData}/>
<PricingTable pricingData={MunpiaData.pricingData}/>
<KeywordsTagsTable keywordsTagsData={MunpiaData.keywordsTagsData}/>