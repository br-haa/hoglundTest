<template>
</template>

<script>
export default {
layout:'half'
}
</script>

<style lang="scss">
html {
  scroll-behavior: smooth;
  body {
    margin: 0;
  }
}
$textMargin: clamp(0.5rem, 1vw / 2.7, 1rem);
h1,
h2,
h3,
h4,
h5,
p,
li,
button,
label,
textarea,
a,
input {
  font-family: IBM Plex Sans, serif;
}

h1 {
  font-size: clamp(2rem, 10 * 1vw / 2, 6rem);
  font-weight: 1000;
  margin: $textMargin 0 $textMargin 0;
}
h2 {
  font-size: clamp(1.7rem, 10 * 1vw / 2.2, 4rem);
  font-weight: 900;
  margin: $textMargin 0 $textMargin 0;
}
h3 {
  font-size: clamp(1.3rem, 10 * 1vw / 2.4, 3rem);
  margin: $textMargin 0 $textMargin 0;
  font-weight: 800;
}
h4 {
  font-size: clamp(1.1rem, 10 * 1vw / 2.6, 2.3rem);
  margin: $textMargin 0 $textMargin 0;
  font-weight: 700;
}
h5 {
  font-size: clamp(0.8rem, 10 * 1vw / 2.8, 1.5rem);
  margin: $textMargin 0 $textMargin 0;
  font-weight: 600;
}
p,
li,
button,
{
  margin: $textMargin 0 $textMargin 0;
  font-size: clamp(0.8rem, 10 * 1vw / 2.8, 1.2rem);
  font-weight: 500;
}
em {
  font-family: IBM Plex Sans , sans-serif;
  font-style: italic;
}
</style>
