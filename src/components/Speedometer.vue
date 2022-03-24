<template>
  <svg
    width="200"
    height="200"
    viewBox="0 0 250 250"
    xmlns="http://www.w3.org/2000/svg"
    class="svg"
  >
    <defs>
      <linearGradient
        id="gradient"
        x1="20"
        y1="110"
        x2="125"
        y2="110"
        gradientUnits="userSpaceOnUse"
      >
        <stop offset="0%" stop-color="red" />
        <stop offset="100%" stop-color="#f75757" />
      </linearGradient>
      <linearGradient
        id="gradient-speedometer"
        x1="0%"
        y1="0%"
        x2="100%"
        y2="0%"
      >
        <stop offset="0%" stop-color="silver" />
        <stop offset="100%" stop-color="black" />
      </linearGradient>
    </defs>
    <!-- <path
      d="M5,145 
      C5,0 195,0 195,145"
      class="speedometer"
    /> -->
    <circle
      cx="50%"
      cy="50%"
      r="125"
      fill="url(#gradient-speedometer)"
    ></circle>
    <circle
      cx="50%"
      cy="50%"
      r="118"
      stroke="white"
      fill="#3b3838"
      stroke-width="1.5"
    ></circle>
    <circle cx="50%" cy="50%" r="115" stroke="silver" fill="#3b3838"></circle>
    <circle
      cx="50%"
      cy="50%"
      r="107"
      stroke="black"
      fill="#3b3838"
      style="filter: drop-shadow(0px 0px 6px black)"
    ></circle>
    <circle cx="50%" cy="50%" r="105" class="speedometer"></circle>

    <!-- <path
      fill="#ff3939"
      stroke-width="3"
      d="M25,110 
      Q25,110 97.5,100
      Q110,102.5 110,110
      Q110,117.5 97.5,120
      Q97.5,120 25,110
      "
      class="arrow"
    /> -->
    <line
      v-for="(item, index) in 17"
      :key="index"
      class="speed-lines"
      x1="50%"
      y1="115"
      x2="50%"
      y2="135"
      :style="{
        transform: 'rotate(' + (205 + item * 17) + 'deg) translateY(-460%)',
      }"
    />

    <line
      v-for="(item, index) in 16"
      :key="index"
      class="small-speed-lines"
      x1="50%"
      y1="120"
      x2="50%"
      y2="130"
      :style="{
        transform:
          'rotate(' + (205 + 1.7 * 1 + item * 17) + 'deg) translateY(-980%)',
      }"
    />
    <line
      v-for="(item, index) in 16"
      :key="index"
      class="small-speed-lines"
      x1="50%"
      y1="120"
      x2="50%"
      y2="130"
      :style="{
        transform:
          'rotate(' + (205 + 1.7 * 2 + item * 17) + 'deg) translateY(-980%)',
      }"
    />
    <line
      v-for="(item, index) in 16"
      :key="index"
      class="small-speed-lines"
      x1="50%"
      y1="120"
      x2="50%"
      y2="130"
      :style="{
        transform:
          'rotate(' + (205 + 1.7 * 3 + item * 17) + 'deg) translateY(-980%)',
      }"
    />
    <line
      v-for="(item, index) in 16"
      :key="index"
      class="small-speed-lines"
      x1="50%"
      y1="120"
      x2="50%"
      y2="130"
      :style="{
        transform:
          'rotate(' + (205 + 1.7 * 4 + item * 17) + 'deg) translateY(-980%)',
      }"
    />
    <line
      v-for="(item, index) in 16"
      :key="index"
      class="small-speed-lines"
      x1="50%"
      y1="120"
      x2="50%"
      y2="130"
      :style="{
        transform:
          'rotate(' + (205 + 1.7 * 5 + item * 17) + 'deg) translateY(-940%)',
        strokeWidth: 1,
      }"
    />
    <line
      v-for="(item, index) in 16"
      :key="index"
      class="small-speed-lines"
      x1="50%"
      y1="120"
      x2="50%"
      y2="130"
      :style="{
        transform:
          'rotate(' + (205 + 1.7 * 6 + item * 17) + 'deg) translateY(-980%)',
      }"
    />
    <line
      v-for="(item, index) in 16"
      :key="index"
      class="small-speed-lines"
      x1="50%"
      y1="120"
      x2="50%"
      y2="130"
      :style="{
        transform:
          'rotate(' + (205 + 1.7 * 7 + item * 17) + 'deg) translateY(-980%)',
      }"
    />

    <line
      v-for="(item, index) in 16"
      :key="index"
      class="small-speed-lines"
      x1="50%"
      y1="120"
      x2="50%"
      y2="130"
      :style="{
        transform:
          'rotate(' + (205 + 1.7 * 8 + item * 17) + 'deg) translateY(-980%)',
      }"
    />
    <line
      v-for="(item, index) in 16"
      :key="index"
      class="small-speed-lines"
      x1="50%"
      y1="120"
      x2="50%"
      y2="130"
      :style="{
        transform:
          'rotate(' + (205 + 1.7 * 9 + item * 17) + 'deg) translateY(-980%)',
      }"
    />

    <path
      class="arrow"
      d="M30,125
        L140,120 L140,130 L30,125
    "
    />
    <circle cx="50%" cy="50%" r="12" class="center-circle"></circle>

    <text
      v-for="(item, index) in 17"
      :key="index"
      x="50%"
      y="50%"
      fill="white"
      class="speed-values"
      :style="{
        transform:
          'translate(' +
          (Math.cos((245 + item * 13 - item * 30) * (Math.PI / 180)) * 70 - 9) +
          'px,' +
          (Math.sin((245 + item * 13 - item * 30) * (Math.PI / 180)) * 70 * -1 +
            4) +
          'px)',
      }"
    >
      {{ index * 20 }}
    </text>
  </svg>
</template>

<script>
export default {
  name: "Speedometer",
  data() {
    return {};
  },
};
</script>

<style lang="scss">
.arrow {
  transform: rotate(312deg);
  transform-origin: 50% 50%;
  fill: url("#gradient");
}

.speedometer {
  fill: #3b3838;
}

.center-circle {
  filter: drop-shadow(0px 0px 4px red) drop-shadow(0px 0px 1px white);
  stroke: red;
  fill: black;
}

.speed-lines {
  stroke: white;
  stroke-width: 2;
  transform-box: fill-box;
  transform-origin: 50% 50%;
}

.small-speed-lines {
  stroke: white;
  stroke-width: 0.5;
  transform-box: fill-box;
  transform-origin: 50% 50%;
}

.speed-values {
  font-size: 0.7rem;
  font-family: Raleway, Roboto, Segoe UI, sans-serif;
  font-weight: bold;
}
</style>
