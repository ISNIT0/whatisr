<script>
  export let level;
</script>

<style>
  section {
    display: flex;
  }
  aside {
    width: 80px;
    flex: 0 0 auto;
  }
  .level {
    width: 80px;
    height: 80px;
    color: #fff;
    font-size: 60px;
    text-align: center;
    line-height: 80px;
    font-weight: bold;
  }
  .level.selected {
    box-shadow: inset 0 0 0 6px black;
  }
  .level-5 {
    background-color: #ea5043;
  }
  .level-4 {
    background-color: #f68922;
  }
  .level-3 {
    background-color: #ffc100;
  }
  .level-2 {
    background-color: #9dbb3b;
  }
  .level-1 {
    background-color: #39b272;
  }

  .content {
    margin-left: 20px;
    padding-left: 10px;
    border-left: 6px solid black;
    font-size: 1.5vw;
  }
  ul {
    padding-left: 4vw;
  }

  @media (max-width: 1000px) {
    aside {
      width: 40px;
    }
    .level {
      width: 40px;
      height: 40px;
      font-size: 30px;
      line-height: 40px;
    }
    .level.selected {
      box-shadow: inset 0 0 0 3px black;
    }
    .content {
      margin-left: 10px;
      padding-left: 5px;
      border-left: 3px solid black;
      font-size: 3vw;
    }
  }
</style>

<section>
  <aside>
    <div class="level level-5" class:selected={level === 5}>5</div>
    <div class="level level-4" class:selected={level === 4}>4</div>
    <div class="level level-3" class:selected={level === 3}>3</div>
    <div class="level level-2" class:selected={level === 2}>2</div>
    <div class="level level-1" class:selected={level === 1}>1</div>
  </aside>
  <div class="content">
    <ul>
      <li>Stay at home as much as possible</li>
      <li>Work from home if you can</li>
      <li>Go to work if you cannot work from home.</li>
      <li>Limit contact with other people</li>
      <li>Keep your distance if you go out (2 metres apart where possible)</li>
      <li>Wash your hands regularly</li>
      <li>Self-isolate if you or anyone in your household has symptoms.</li>
      <li>Keep following these rules even if you see others breaking them.</li>
    </ul>
  </div>
</section>
