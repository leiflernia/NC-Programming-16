<script>
  import Modal from "./Modal.svelte";

  const videoFileUrls = [
    "https://www.dreambroker.com/channel/pw9wz9ay/oqdbh2jb/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/a9wj3yn2/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/wfpxlfta/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/7fgf63i2/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/232ldz5w/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/tvhlfalw/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/t6sgbcpp/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/rduc0b4x/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/ztgng7b0/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/l30572fr/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/qtv9lw49/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/mbqh5pkq/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/bhvgecdq/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/vmfvifd9/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/h5b22htw/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/0o9ycmwc/get/normal.mp4",
    "https://www.dreambroker.com/channel/pw9wz9ay/hgrimkyh/get/normal.mp4",
  ];

  window.caches
    .open("video")
    .then((cache) =>
      Promise.all(
        videoFileUrls.map((videoFileUrl) => fetchAndCache(videoFileUrl, cache))
      )
    );

  function deleteVideo() {
    caches.delete("video");
  }

  function fetchAndCache(videoFileUrls, cache) {
    // Check first if video is in the cache.
    return cache.match(videoFileUrls).then((cacheResponse) => {
      // Let's return cached response if video is already in the cache.
      if (cacheResponse) {
        return cacheResponse;
      }
      // Otherwise, fetch the video from the network.
      return fetch(videoFileUrls).then((networkResponse) => {
        // Add the response to the cache and return network response in parallel.
        cache.put(videoFileUrls, networkResponse.clone());
        return networkResponse;
      });
    });
  }

  function make_uppercase() {
    this.value = this.value.toLocaleUpperCase();
  }

  let showModal1Wrong = false;
  let showModal1Tip = false;
  let tip1 = 1;

  let showModal2Wrong = false;
  let showModal2Tip = false;
  let tip2 = 1;

  let showModal3Wrong = false;
  let showModal3Tip = false;
  let tip3 = 1;

  let showModal4Wrong = false;
  let showModal4Tip = false;
  let tip4 = 1;

  let showModal5Wrong = false;
  let showModal5Tip = false;
  let tip5 = 1;

  let showModal6Wrong = false;
  let showModal6Tip = false;
  let tip6 = 1;

  let showModal7Wrong = false;
  let showModal7Tip = false;
  let tip7 = 1;

  let showModal8Wrong = false;
  let showModal8Tip = false;
  let tip8 = 1;

  let showModal9Wrong = false;
  let showModal9Tip = false;
  let tip9 = 1;

  let showModal10Wrong = false;
  let showModal10Tip = false;
  let tip10 = 1;

  let showModal11Wrong = false;
  let showModal11Tip = false;
  let tip11 = 1;

  let showModal12Wrong = false;
  let showModal12Tip = false;
  let tip12 = 1;

  let showModal13Wrong = false;
  let showModal13Tip = false;
  let tip13 = 1;

  let showModal14Wrong = false;
  let showModal14Tip = false;
  let tip14 = 1;

  let first = true;
  let startRotationValue = "";
  let second = false;
  let point1Value = "";
  let third = false;
  let point2Value = "";
  let fourth = false;
  let point3Value = "";
  let fift = false;
  let point4Value = "";
  let sixth = false;
  let point5Value = "";
  let seventh = false;
  let point6Value = "";
  let eight = false;
  let point7Value = "";
  let ninth = false;
  let point8Value = "";
  let tenth = false;
  let point9Value = "";
  let eleventh = false;
  let point10Value = "";
  let twelfth = false;
  let point11Value = "";
  let thirteenth = false;
  let point12Value = "";
  let fourteenth = false;
  let point13Value = "";
  let fifteenth = false;
  let point14Value = "";
  let sixteenth = false;
  let point15Value = "";
  let seventeenth = false;
  let point16Value = "";
  let eightteen = false;
  let point17Value = "";
  let nineteenth = false;
  let point18Value = "";
  let twenty = false;
  let point19Value = "";
  let twentyone = false;
  let point20Value = "";
  let twentytwo = false;
  let point21Value = "";
  let twentythree = false;
  let point22Value = "";
  let twentyfour = false;
  let point23Value = "";
  let twentyfive = "";
  let point24Value = "";
  let twentysix = "";
  let point25Value = "";
  let twentyseven = "";
  let endPoint = "";

  function startRotation() {
    if (
      startRotationValue.toLocaleUpperCase().replace(/\s/g, "") == "M3S2000" ||
      startRotationValue.toLocaleUpperCase().replace(/\s/g, "") == "M03S2000"
    ) {
      second = true;
      first = false;
    } else if (tip1 == 1) {
      showModal1Wrong = true;
      tip1 = 2;
    } else if (tip1 == 2) {
      showModal1Wrong = true;
      tip1 = 3;
    } else {
      showModal1Tip = true;
    }
  }

  function point1() {
    if (
      point1Value.toLocaleUpperCase().replace(/\s/g, "") == "G0X0Y-10" ||
      point1Value.toLocaleUpperCase().replace(/\s/g, "") == "G00X0Y-10"
    ) {
      second = false;
      third = true;
      setTimeout(function () {
        fourth = true;
        third = false;
      }, 2000);
    } else if (tip2 == 1) {
      showModal2Wrong = true;
      tip2 = 2;
    } else if (tip2 == 2) {
      showModal2Wrong = true;
      tip2 = 3;
    } else {
      showModal2Tip = true;
    }
  }

  function point2() {
    if (
      point2Value.toLocaleUpperCase().replace(/\s/g, "") == "G1X0Y-60" ||
      point2Value.toLocaleUpperCase().replace(/\s/g, "") == "G01X0Y-60"
    ) {
      fourth = false;
      fift = true;
      setTimeout(function () {
        sixth = true;
        fift = false;
      }, 2000);
    } else if (tip3 == 1) {
      showModal3Wrong = true;
      tip3 = 2;
    } else if (tip3 == 2) {
      showModal3Wrong = true;
      tip3 = 3;
    } else {
      showModal3Tip = true;
    }
  }

  function point3() {
    if (
      point3Value.toLocaleUpperCase().replace(/\s/g, "") == "G3X20Y-80I20J0" ||
      point3Value.toLocaleUpperCase().replace(/\s/g, "") == "G03X20Y-80I20J0"
    ) {
      sixth = false;
      seventh = true;
      setTimeout(function () {
        eight = true;
        seventh = false;
      }, 2000);
    } else if (tip4 == 1) {
      showModal3Wrong = true;
      tip4 = 2;
    } else if (tip4 == 2) {
      showModal3Wrong = true;
      tip4 = 3;
    } else {
      showModal3Tip = true;
    }
  }

  function point4() {
    if (
      point4Value.toLocaleUpperCase().replace(/\s/g, "") == "G1X85Y-80" ||
      point4Value.toLocaleUpperCase().replace(/\s/g, "") == "G01X85Y-80"
    ) {
      eight = false;
      ninth = true;
      setTimeout(function () {
        tenth = true;
        ninth = false;
      }, 2000);
    } else if (tip5 == 1) {
      showModal3Wrong = true;
      tip5 = 2;
    } else if (tip5 == 2) {
      showModal3Wrong = true;
      tip5 = 3;
    } else {
      showModal3Tip = true;
    }
  }

  function point5() {
    if (
      point5Value.toLocaleUpperCase().replace(/\s/g, "") == "G3X90Y-75I0J5" ||
      point5Value.toLocaleUpperCase().replace(/\s/g, "") == "G03X90Y-75I0J5"
    ) {
      tenth = false;
      eleventh = true;
      setTimeout(function () {
        twelfth = true;
        eleventh = false;
      }, 2000);
    } else if (tip6 == 1) {
      showModal3Wrong = true;
      tip6 = 2;
    } else if (tip6 == 2) {
      showModal3Wrong = true;
      tip6 = 3;
    } else {
      showModal3Tip = true;
    }
  }

  function point6() {
    if (
      point6Value.toLocaleUpperCase().replace(/\s/g, "") == "G1X90Y-65" ||
      point6Value.toLocaleUpperCase().replace(/\s/g, "") == "G01X90Y-65"
    ) {
      twelfth = false;
      thirteenth = true;
      setTimeout(function () {
        fourteenth = true;
        thirteenth = false;
      }, 2000);
    } else if (tip7 == 1) {
      showModal3Wrong = true;
      tip7 = 2;
    } else if (tip7 == 2) {
      showModal3Wrong = true;
      tip7 = 3;
    } else {
      showModal3Tip = true;
    }
  }
  function point7() {
    if (
      point7Value.toLocaleUpperCase().replace(/\s/g, "") == "G3X85Y-60I-5J0" ||
      point7Value.toLocaleUpperCase().replace(/\s/g, "") == "G03X85Y-60I-5J0"
    ) {
      fourteenth = false;
      fifteenth = true;
      setTimeout(function () {
        sixteenth = true;
        fifteenth = false;
      }, 2000);
    } else if (tip8 == 1) {
      showModal3Wrong = true;
      tip8 = 2;
    } else if (tip8 == 2) {
      showModal3Wrong = true;
      tip8 = 3;
    } else {
      showModal3Tip = true;
    }
  }

  function point8() {
    if (
      point8Value.toLocaleUpperCase().replace(/\s/g, "") == "G1X50Y-60" ||
      point8Value.toLocaleUpperCase().replace(/\s/g, "") == "G01X50Y-60"
    ) {
      sixteenth = false;
      seventeenth = true;
      setTimeout(function () {
        eightteen = true;
        seventeenth = false;
      }, 2000);
    } else if (tip9 == 1) {
      showModal3Wrong = true;
      tip9 = 2;
    } else if (tip9 == 2) {
      showModal3Wrong = true;
      tip9 = 3;
    } else {
      showModal3Tip = true;
    }
  }

  function point9() {
    if (
      point9Value.toLocaleUpperCase().replace(/\s/g, "") == "G1X50Y-30" ||
      point9Value.toLocaleUpperCase().replace(/\s/g, "") == "G01X50Y-30"
    ) {
      eightteen = false;
      nineteenth = true;
      setTimeout(function () {
        twenty = true;
        nineteenth = false;
      }, 2000);
    } else if (tip10 == 1) {
      showModal3Wrong = true;
      tip10 = 2;
    } else if (tip10 == 2) {
      showModal3Wrong = true;
      tip10 = 3;
    } else {
      showModal3Tip = true;
    }
  }

  function point10() {
    if (
      point10Value.toLocaleUpperCase().replace(/\s/g, "") == "G1X80Y-30" ||
      point10Value.toLocaleUpperCase().replace(/\s/g, "") == "G01X80Y-30"
    ) {
      twenty = false;
      twentyone = true;
      setTimeout(function () {
        twentytwo = true;
        twentyone = false;
      }, 2000);
    } else if (tip11 == 1) {
      showModal3Wrong = true;
      tip11 = 2;
    } else if (tip11 == 2) {
      showModal3Wrong = true;
      tip11 = 3;
    } else {
      showModal3Tip = true;
    }
  }

  function point11() {
    if (
      point11Value.toLocaleUpperCase().replace(/\s/g, "") == "G3X80Y-10I0J10" ||
      point11Value.toLocaleUpperCase().replace(/\s/g, "") == "G03X80Y-10I0J10"
    ) {
      twentytwo = false;
      twentythree = true;
      setTimeout(function () {
        twentyfour = true;
        twentythree = false;
      }, 2000);
    } else if (tip12 == 1) {
      showModal3Wrong = true;
      tip12 = 2;
    } else if (tip12 == 2) {
      showModal3Wrong = true;
      tip12 = 3;
    } else {
      showModal3Tip = true;
    }
  }

  function point12() {
    if (
      point12Value.toLocaleUpperCase().replace(/\s/g, "") == "G1X0Y-10" ||
      point12Value.toLocaleUpperCase().replace(/\s/g, "") == "G01X0Y-10"
    ) {
      twentyfour = false;
      twentyfive = true;
      setTimeout(function () {
        endPoint = true;
        twentyfive = false;
      }, 2000);
    } else if (tip13 == 1) {
      showModal3Wrong = true;
      tip13 = 2;
    } else if (tip13 == 2) {
      showModal3Wrong = true;
      tip13 = 3;
    } else {
      showModal3Tip = true;
    }
  }

  function end() {
    if (point13Value.toLocaleUpperCase().replace(/\s/g, "") == "M30") {
      endPoint = false;
    } else if (tip14 == 1) {
      showModal4Wrong = true;
      tip14 = 2;
    } else if (tip14 == 2) {
      showModal3Wrong = true;
      tip14 = 3;
    } else {
      showModal4Tip = true;
    }
  }
</script>

{#if first}
  <div>
    <img class="canvas" src="start.jpg" alt="Bild 1" />
  </div>
  <div>
    <p>
      Ange koden för start av medurs rotation med TVÅ tusen varv per minut.(M03
      eller M04)
    </p>
  </div>
  <div>
    <form>
      <!-- svelte-ignore a11y-autofocus -->
      <input
        autofocus
        style="text-transform: uppercase"
        type="text"
        on:input={make_uppercase}
        bind:value={startRotationValue}
      />
      <button type="submit" on:click|preventDefault={startRotation}>
        Kör
      </button>
    </form>
  </div>
  {#if showModal1Wrong}
    <Modal on:close={() => (showModal1Wrong = false)}>
      <p>
        Tyvärr så var det inte rätt, försök igen och tänk på ordningsföljden.
      </p>
    </Modal>
  {:else if showModal1Tip}
    <Modal on:close={() => (showModal1Tip = false)}>
      <p>Skriv in M3S2000 tryck på Kör</p>
    </Modal>
  {/if}
{:else if second}
  <video autoplay loop class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/oqdbh2jb/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <div>
      <p>
        Programmera dig från punkt till punkt. Observera att både X & Y måste
        anges för varje block. Grönt streck = G1, G2 eller G3. Rött streck = G0
        Använd snabbmatning (G0) vid körning till konturen. Följ den blå punkten
        runt konturen. Avsluta med kod för programslut. Varje ruta motsvarar
        10mm.
      </p>
    </div>
    <form>
      <!-- svelte-ignore a11y-autofocus -->
      <input
        autofocus
        style="text-transform: uppercase"
        type="text"
        on:input={make_uppercase}
        bind:value={point1Value}
      />
      <button type="submit" on:click|preventDefault={point1}>Kör</button>
    </form>
  </div>
  {#if showModal2Wrong}
    <Modal on:close={() => (showModal2Wrong = false)}>
      <p>
        Tyvärr så var det inte rätt, försök igen och tänk på ordningsföljden.
      </p>
    </Modal>
  {:else if showModal2Tip}
    <Modal on:close={() => (showModal2Tip = false)}>
      <p>G0X0Y-10</p>
    </Modal>
  {/if}
{:else if third}
  <video autoplay class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/a9wj3yn2/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>
      Programmera dig från punkt till punkt. Observera att både X & Y måste
      anges för varje block. Grönt streck = G1, G2 eller G3. Rött streck = G0
      Använd snabbmatning (G0) vid körning till konturen. Följ den blå punkten
      runt konturen. Avsluta med kod för programslut. Varje ruta motsvarar 10mm.
    </p>
  </div>
{:else if fourth}
  <div class="canvas">
    <video autoplay loop class="canvas">
      <source
        src="https://www.dreambroker.com/channel/pw9wz9ay/wfpxlfta/get/normal.mp4"
        type="video/mp4"
      />
      Du måste använda en annan webbläsare för att kunna spela upp video.
    </video>
    <div>
      <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
    </div>
    <div>
      <form>
        <!-- svelte-ignore a11y-autofocus -->
        <input
          autofocus
          style="text-transform: uppercase"
          type="text"
          on:input={make_uppercase}
          bind:value={point2Value}
        />
        <button type="submit" on:click|preventDefault={point2}>Kör</button>
      </form>
    </div>
    {#if showModal3Wrong}
      <Modal on:close={() => (showModal3Wrong = false)}>
        <p>
          Tyvärr så var det inte rätt, försök igen och tänk på ordningsföljden.
        </p>
      </Modal>
    {:else if showModal3Tip}
      <Modal on:close={() => (showModal3Tip = false)}>
        <p>G1X0Y-60</p>
      </Modal>
    {/if}
    <div />
  </div>
{:else if fift}
  <video autoplay class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/7fgf63i2/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div />
{:else if sixth}
  <video autoplay loop class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/232ldz5w/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <div>
      <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
    </div>
    <div>
      <form>
        <!-- svelte-ignore a11y-autofocus -->
        <input
          autofocus
          style="text-transform: uppercase"
          type="text"
          on:input={make_uppercase}
          bind:value={point3Value}
        />
        <button type="submit" on:click|preventDefault={point3}>Kör</button>
      </form>
    </div>
    {#if showModal3Wrong}
      <Modal on:close={() => (showModal3Wrong = false)}>
        <!-- <h2 slot="header">
        </h2> -->
        <p>
          Tyvärr så var det inte rätt, försök igen och tänk på ordningsföljden.
        </p>
      </Modal>
    {:else if showModal3Tip}
      <Modal on:close={() => (showModal3Tip = false)}>
        <p>G3X20Y-80I20J0</p>
      </Modal>
    {/if}
  </div>
  <div />
{:else if seventh}
  <video autoplay class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/tvhlfalw/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div />
{:else if eight}
  <video autoplay loop class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/t6sgbcpp/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <div>
      <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
    </div>
    <div>
      <form>
        <!-- svelte-ignore a11y-autofocus -->
        <input
          autofocus
          style="text-transform: uppercase"
          type="text"
          on:input={make_uppercase}
          bind:value={point4Value}
        />
        <button type="submit" on:click|preventDefault={point4}>Kör</button>
      </form>
    </div>
    {#if showModal3Wrong}
      <Modal on:close={() => (showModal3Wrong = false)}>
        <!-- <h2 slot="header">
        </h2> -->
        <p>
          Tyvärr så var det inte rätt, försök igen och tänk på ordningsföljden.
        </p>
      </Modal>
    {:else if showModal3Tip}
      <Modal on:close={() => (showModal3Tip = false)}>
        <p>G1X85Y-80</p>
      </Modal>
    {/if}
  </div>
  <div />
{:else if ninth}
  <video autoplay class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/rduc0b4x/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div />
{:else if tenth}
  <video autoplay loop class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/ztgng7b0/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div>
    <form>
      <!-- svelte-ignore a11y-autofocus -->
      <input
        autofocus
        style="text-transform: uppercase"
        type="text"
        on:input={make_uppercase}
        bind:value={point5Value}
      />
      <button type="submit" on:click|preventDefault={point5}>Kör</button>
    </form>
  </div>
  {#if showModal3Wrong}
    <Modal on:close={() => (showModal3Wrong = false)}>
      <!-- <h2 slot="header">
        </h2> -->
      <p>
        Tyvärr så var det inte rätt, försök igen och tänk på ordningsföljden.
      </p>
    </Modal>
  {:else if showModal3Tip}
    <Modal on:close={() => (showModal3Tip = false)}>
      <p>G3X90Y-75I0J5</p>
    </Modal>
  {/if}
  <div />
{:else if eleventh}
  <video autoplay loop class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/l30572fr/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div />
{:else if twelfth}
  <video autoplay loop class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/qtv9lw49/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div>
    <form>
      <!-- svelte-ignore a11y-autofocus -->
      <input
        autofocus
        style="text-transform: uppercase"
        type="text"
        on:input={make_uppercase}
        bind:value={point6Value}
      />
      <button type="submit" on:click|preventDefault={point6}>Kör</button>
    </form>
    {#if showModal3Wrong}
      <Modal on:close={() => (showModal3Wrong = false)}>
        <p>
          Tyvärr så var det inte rätt, försök igen och tänk på ordningsföljden.
        </p>
      </Modal>
    {:else if showModal3Tip}
      <Modal on:close={() => (showModal3Tip = false)}>
        <p>G1X90Y-65</p>
      </Modal>
    {/if}
  </div>
  <div />
{:else if thirteenth}
  <div class="canvas">
    <video autoplay loop class="canvas">
      <source
        src="https://www.dreambroker.com/channel/pw9wz9ay/mbqh5pkq/get/normal.mp4"
        type="video/mp4"
      />
      Du måste använda en annan webbläsare för att kunna spela upp video.
    </video>
    <div>
      <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
    </div>
    <div />
  </div>
{:else if fourteenth}
  <video autoplay loop class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/bhvgecdq/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div>
    <form>
      <!-- svelte-ignore a11y-autofocus -->
      <input
        autofocus
        style="text-transform: uppercase"
        type="text"
        on:input={make_uppercase}
        bind:value={point7Value}
      />
      <button type="submit" on:click|preventDefault={point7}>Kör</button>
    </form>
    {#if showModal3Wrong}
      <Modal on:close={() => (showModal3Wrong = false)}>
        <p>
          Tyvärr så var det inte rätt, försök igen och tänk på ordningsföljden.
        </p>
      </Modal>
    {:else if showModal3Tip}
      <Modal on:close={() => (showModal3Tip = false)}>
        <p>G3X85Y-60I-5J0</p>
      </Modal>
    {/if}
  </div>
  <div />
{:else if fifteenth}
  <video autoplay loop class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/vmfvifd9/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div />
{:else if sixteenth}
  <video autoplay loop class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/h5b22htw/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div>
    <form>
      <!-- svelte-ignore a11y-autofocus -->
      <input
        autofocus
        style="text-transform: uppercase"
        type="text"
        on:input={make_uppercase}
        bind:value={point8Value}
      />
      <button type="submit" on:click|preventDefault={point8}>Kör</button>
    </form>
    {#if showModal3Wrong}
      <Modal on:close={() => (showModal3Wrong = false)}>
        <p>
          Tyvärr så var det inte rätt, försök igen och tänk på ordningsföljden.
        </p>
      </Modal>
    {:else if showModal3Tip}
      <Modal on:close={() => (showModal3Tip = false)}>
        <p>G1X50Y-60</p>
      </Modal>
    {/if}
  </div>
  <div />
{:else if seventeenth}
  <video autoplay loop class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/0o9ycmwc/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div />
{:else if eightteen}
  <video autoplay loop class="canvas">
    <source
      src="https://www.dreambroker.com/channel/pw9wz9ay/hgrimkyh/get/normal.mp4"
      type="video/mp4"
    />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div>
    <form>
      <!-- svelte-ignore a11y-autofocus -->
      <input
        autofocus
        style="text-transform: uppercase"
        type="text"
        on:input={make_uppercase}
        bind:value={point9Value}
      />
      <button type="submit" on:click|preventDefault={point9}>Kör</button>
    </form>
    {#if showModal3Wrong}
      <Modal on:close={() => (showModal3Wrong = false)}>
        <p>
          Tyvärr så var det inte rätt, försök igen och tänk på ordningsföljden.
        </p>
      </Modal>
    {:else if showModal3Tip}
      <Modal on:close={() => (showModal3Tip = false)}>
        <p>G1X50Y-30</p>
        <!-- <img width="510px" src="G2-Hint-Mill.png" alt="Tips 3" /> -->
      </Modal>
    {/if}
  </div>
  <div />
{:else if nineteenth}
  <video autoplay loop class="canvas">
    <source src="clip-18.mp4" type="video/mp4" />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div />

  <!-- point 10 -->
{:else if twenty}
  <video autoplay loop class="canvas">
    <source src="clip-19.mp4" type="video/mp4" />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div>
    <form>
      <!-- svelte-ignore a11y-autofocus -->
      <input
        autofocus
        style="text-transform: uppercase"
        type="text"
        on:input={make_uppercase}
        bind:value={point10Value}
      />
      <button type="submit" on:click|preventDefault={point10}>Kör</button>
    </form>
    {#if showModal3Wrong}
      <Modal on:close={() => (showModal3Wrong = false)}>
        <p>
          Tyvärr så var det inte rätt, försök igen och tänk på ordningsföljden.
        </p>
      </Modal>
    {:else if showModal3Tip}
      <Modal on:close={() => (showModal3Tip = false)}>
        <p>G1X80Y-30</p>
        <!-- <img width="510px" src="G2-Hint-Mill.png" alt="Tips 3" /> -->
      </Modal>
    {/if}
  </div>
  <div />
{:else if twentyone}
  <video autoplay loop class="canvas">
    <source src="clip-20.mp4" type="video/mp4" />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div />

  <!-- Point 10 -->
{:else if twentytwo}
  <video autoplay loop class="canvas">
    <source src="clip-21.mp4" type="video/mp4" />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div>
    <form>
      <!-- svelte-ignore a11y-autofocus -->
      <input
        autofocus
        style="text-transform: uppercase"
        type="text"
        on:input={make_uppercase}
        bind:value={point11Value}
      />
      <button type="submit" on:click|preventDefault={point11}>Kör</button>
    </form>
    {#if showModal3Wrong}
      <Modal on:close={() => (showModal3Wrong = false)}>
        <p>
          Tyvärr så var det inte rätt, försök igen och tänk på ordningsföljden.
        </p>
      </Modal>
    {:else if showModal3Tip}
      <Modal on:close={() => (showModal3Tip = false)}>
        <p>G3X80Y-10I0J10</p>
      </Modal>
    {/if}
  </div>
  <div />
{:else if twentythree}
  <video autoplay loop class="canvas">
    <source src="clip-22.mp4" type="video/mp4" />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div />

  <!-- Point 11 -->
{:else if twentyfour}
  <video autoplay loop class="canvas">
    <source src="clip-23.mp4" type="video/mp4" />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde.</p>
  </div>
  <div>
    <form>
      <!-- svelte-ignore a11y-autofocus -->
      <input
        autofocus
        style="text-transform: uppercase"
        type="text"
        on:input={make_uppercase}
        bind:value={point12Value}
      />
      <button type="submit" on:click|preventDefault={point12}>Kör</button>
    </form>
    {#if showModal3Wrong}
      <Modal on:close={() => (showModal3Wrong = false)}>
        <p>
          Tyvärr så var det inte rätt, försök igen och tänk på ordningsföljden.
        </p>
      </Modal>
    {:else if showModal3Tip}
      <Modal on:close={() => (showModal3Tip = false)}>
        <p>G1X0Y-10</p>
      </Modal>
    {/if}
  </div>
  <div />
{:else if twentyfive}
  <video autoplay loop class="canvas">
    <source src="clip-24.mp4" type="video/mp4" />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Följ den blå punkten runt konturen ange G-värde X-värde Y-värde. Hej</p>
  </div>
  <div />

  <!-- end -->
{:else if endPoint}
  <video autoplay loop class="canvas">
    <source src="clip-25.mp4" type="video/mp4" />
    Du måste använda en annan webbläsare för att kunna spela upp video.
  </video>
  <div>
    <p>Avsluta programmet</p>
  </div>
  <div>
    <form>
      <!-- svelte-ignore a11y-autofocus -->
      <input
        autofocus
        style="text-transform: uppercase"
        type="text"
        on:input={make_uppercase}
        bind:value={point13Value}
      />
      <button
        type="submit"
        on:click|preventDefault={end}
        on:focus={deleteVideo}
      >
        Kör
      </button>
    </form>
    {#if showModal4Wrong}
      <Modal on:close={() => (showModal4Wrong = false)}>
        <p>M30 avslutar programmet</p>
      </Modal>
    {:else if showModal4Tip}
      <Modal on:close={() => (showModal4Tip = false)}>
        <p>M30 avslutar programmet</p>
      </Modal>
    {/if}
  </div>
  <div />
{:else}
  <img class="canvas" src="stop.jpg" alt="Stop" />

  <div>
    <h1>Det är allt!</h1>
    <p>Du är nu klar med övningen. Bra jobbat!</p>
  </div>
{/if}

<style>
  .canvas {
    left: 0;
    width: 700px;
  }
</style>
