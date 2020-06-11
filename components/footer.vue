<template>
  <div class="footer">
    <div class="block"></div>
    <div class="text">
      Lunch 11:30-14:00 Dinner 18:00-23:00&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      〒101-0062 東京都千代田区神田駿河台4-6-B4F&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      Tel 03-1234-5678
      <br />Copyright (C) FANTASTICO540 co.,ltd ※このお店は実在しません
    </div>
  </div>
</template>

<style lang="scss" scoped>
.footer {
  min-height: 80px;
  background-color: #e88c4d;
  position: relative;
  bottom: 0;
  top: 0;
  width: 100%;
}

.block {
  --width: 16px;
  height: calc(var(--width) / 2);
  width: 100vw;
  background: repeating-linear-gradient(
    to right,
    #fff,
    #fff var(--width),
    #009245 var(--width),
    #009245 calc(var(--width) * 2),
    #c1272d calc(var(--width) * 2),
    #c1272d calc(var(--width) * 3)
  );
}

.text {
  margin: 10px;
  line-height: 25px;
  font-size: 1.1rem;
  text-align: center;
}
</style>