<template>
  <VApp class="bg">
    <VContainer>
      <VCard flat max-width="1000px" rounded="xl" class="ma-auto pa-6 ma-5 mt-10 shandow">
        <Header />
        <Actions />
        <Table />
      </VCard>
    </VContainer>
  </VApp>
</template>
<style>
* {
  font-family: "Open Sans", sans-serif;
  font-optical-sizing: auto;
  font-style: normal;
  font-variation-settings: "wdth" 100;
  line-height: 1;
}
.bg {
  background-color: #f7f8fa !important;
}
.shandow {
  -webkit-box-shadow: 0px 3px 33px -7px rgba(45, 45, 45, 0.5);
  -moz-box-shadow: 0px 3px 33px -7px rgba(45, 45, 45, 0.5);
  box-shadow: 0px 3px 33px -7px rgba(45, 45, 45, 0.5);
}
</style>
