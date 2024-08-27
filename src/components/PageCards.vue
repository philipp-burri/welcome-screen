<script setup>
import { onMounted } from 'vue';
import  { ref } from 'vue';

const data = ref([])
const googleApi = import.meta.env.VITE_GOOGLE_API_KEY
const googleSheetId = "1wIFXqrkCjqjseb5cQ-bgUfNHN1_0_fKsYF83joG9TyE";

async function fetchData() {
  try {
    const response = await fetch(`https://sheets.googleapis.com/v4/spreadsheets/${googleSheetId}/values:batchGet?ranges=A1%3AE100&valueRenderOption=FORMATTED_VALUE&key=${googleApi}`);
    const jsonData = await response.json();
    console.log(jsonData);
    data.value = jsonData.valueRanges[0].values.slice(1).map (row => ({
      time: row[0],
      title: row[1],
      location: row[2]
    }))
  } catch (error) {
    console.error('Error fetching data:', error);
  }
}
function startDataFetching() {
  fetchData(); 
  setInterval(fetchData, 3 * 60 * 60 * 1000); 
}

onMounted(() => {
  startDataFetching();
  
});
</script>

<template>
    <div class="info">
        <div v-for="(event, index) in data" :key="index" class="info-card">
        <ul>
            <li><div class="info-time">{{ event.time }}</div></li>
            <li><div class="info-title">{{ event.title }}</div></li>
            <li><div class="info-location">{{ event.location }}</div></li>
        </ul>
        </div>
    </div>
</template>

<style scoped>
ul{
  list-style: none;
}
.info{
  display: flex;
  flex-direction: column;
  gap: 40px;
  margin-top: 36px;
}
.info-card{
  background-color: #0F05A0 ;
  border-radius: 4px;
  padding-top: 35px;
  padding-bottom: 40px;
  padding-left: 35px;
  gap: 10px;
  min-width: 960px;
}
.info-time{
  color: #EB5E00;
  font-size: 28px;
  font-weight: 900;
}
.info-title{
  color: #FFBFAB;
  font-weight: 900;
  font-size: 28px;
}
.info-location{
  color: #FFBFAB;
  font-size: 28px;
}
</style>