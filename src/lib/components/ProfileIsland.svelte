<script lang="ts">
  import { handleCameraMovement, mesh } from "$lib/stores";
  import { T } from "@threlte/core";
  import { HTML } from "@threlte/extras";
  import Chest from "./models/Chest.svelte";
  import DingusTheCat from "./models/DingusTheCat.svelte";
  import Lute from "./models/Lute.svelte";
  import MediumIsland from "./models/MediumIsland.svelte";
  import PalmTree from "./models/PalmTree.svelte";
  import PalmTree1 from "./models/PalmTree1.svelte";
  import Sawmill from "./models/Sawmill.svelte";
  import SmallShip from "./models/SmallShip.svelte";
  import WoodenSign2 from "./models/WoodenSign2.svelte";
  import FishBucket from "./models/FishBucket.svelte";
  import Barrel from "./models/Barrel.svelte";
  import Skull from "./models/Skull.svelte";
  import Grass1 from "./models/Grass1.svelte";
</script>

<MediumIsland position.x={0.8} position.z={-3} />

<Chest
  scale={0.15}
  position.x={0.4}
  position.y={1.5}
  position.z={-3}
  rotation.y={0.4}
/>

<Barrel
  scale={0.15}
  position.x={0.8}
  position.y={1.5}
  position.z={-3}
  rotation.y={0.4}
/>

<Skull
  scale={0.15}
  position.x={0.8}
  position.y={1.6}
  position.z={-3}
  rotation.y={0.4}
/>

<FishBucket
  scale={0.15}
  position.x={0.4}
  position.y={1.5}
  position.z={-2.75}
  rotation.y={0.4}
/>

<PalmTree
  scale={0.2}
  position.x={0.4}
  position.y={1.5}
  position.z={-3.3}
  rotation.y={0.4}
/>

<Grass1
  scale={0.4}
  position.x={0.45}
  position.y={1.5}
  position.z={-3.3}
  rotation.y={0.4}
/>

<PalmTree1
  scale={0.2}
  position.x={1.15}
  position.y={1.5}
  position.z={-3.3}
  rotation.y={0.4}
/>

<Grass1
  scale={0.4}
  position.x={1.15}
  position.y={1.5}
  position.z={-3.3}
  rotation.y={0.4}
/>

<Sawmill
  scale={0.2}
  position.x={1.15}
  position.y={1.5}
  position.z={-3.1}
  rotation.y={-2}
/>

<SmallShip
  scale={0.14}
  position.x={0.8}
  position.y={1.5}
  position.z={-3.4}
  rotation.y={-3}
/>

<Lute
  scale={0.2}
  position.x={0.65}
  position.y={1.685}
  position.z={-3.15}
  rotation.x={-0.2}
  rotation.y={-0.5}
  rotation.z={3}
/>

<DingusTheCat
  scale={0.03}
  position.x={0.5}
  position.y={1.5}
  position.z={-3.5}
  rotation.y={4}
/>

<T.Mesh
  position.y={1.5}
  on:create={({ ref }) => {
    $mesh = ref;
  }}
>
  <WoodenSign2 scale={0.16} position.x={0.7} position.z={-2.9} />

  <HTML transform position.x={0.807} position.z={-2.9} position.y={0.36}>
    <button
      on:click={$handleCameraMovement(1, 2.5, -2, 4, 1.5, -1.4)}
      class="text-white"
      style="font-size: 1px;">Next</button
    >
  </HTML>
</T.Mesh>
