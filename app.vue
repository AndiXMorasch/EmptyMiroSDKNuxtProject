<script setup lang="ts">

/*
<Initializer method for your application>
Please mind that this application must run
on localhost:3000. Otherwise, your application will
not be recognized by Miro!
 */
async function init() {

  if (miro === undefined) {
    console.log("Miro is undefined");
    return;
  }

  miro.board.ui.on('icon:click', async () => {
    console.log('Board connection established...');
    await miro.board.ui.openPanel({url: '/'});
    /*
    '/' pointing to the index.vue File in the 'pages' directory.
    From there you can start coding.
     */
  });
}

await init();

</script>

<template>
  <div>
    <NuxtPage/>
  </div>
</template>

<style>
/*
Do not delete this CSS attributes, otherwise you
may get problems with the width and height of the
content inside of your Miro Web SDK window!
*/

#__nuxt {
  height: 100%;
  width: 100%;
}

#__nuxt > div:first-child {
  height: 100%;
  width: 100%;
}
</style>
