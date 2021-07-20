<script>
  import { calcTime, convertMoney } from '../helpers/helpers';
  export let time;
  export let budget;
  export let revenue;

</script>

<div class='wrapper'>
  <div class='content'>
    <div class='content-col'>
      <p>Running Time: {calcTime(time)}</p>
    </div>
    <div class='content-col'>
      <p>Budget: {convertMoney(budget)}</p>
    </div>
    <div class='content-col'>
      <p>Revenue: {convertMoney(revenue)}</p>
    </div>
  </div>
</div>

<style>
  .wrapper {
      display: flex;
      align-items: center;
      width: 100%;
      min-height: 100%;
      height: auto;
      background: #1c1c1c;
      padding: 20px;
      box-sizing: border-box;
      font-size: 20px;
  }

  .content {
      display: flex;
      align-items: flex-start;
      justify-content: center;
      width: 100%;
      max-width: 1280px;
  }

  .content-col {
      width: 30%;
      flex: 0 0 33%;
      background: #353535;
      color: #fff;
      padding: 0 20px;
      margin: 0 20px;
      border-radius: 40px;
      text-align: center;
  }
</style>