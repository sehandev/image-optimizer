<script lang="ts">
  import { invoke } from "@tauri-apps/api/tauri"

  let info = ""

  async function convertTest() {
    info = await invoke("convert", {
      imagePath: "/Users/sehan/Downloads/test.png",
    })
  }
</script>

<div>
  <div class="row">
    <button on:click={convertTest}> Test </button>
  </div>
  <p>{info}</p>
</div>
