<section class="cards">
    {#each items as item,index}
    <div class="card">
        <header class="card__header">
          <div class="header__number">
            <span>{index+1}</span>
          </div>
          <h2 class="header__title">
            <span class="title__date"> 
                {#if item.endDate }
                <span class="cd-timeline__date">{item.beginDate} - {item.endDate}</span>
                {:else}
                <span class="cd-timeline__date">{item.beginDate}</span>
                {/if}
            </span>
            <span class="title__sub">{item.title}</span>
          </h2>
        </header>
        <article class="card__article">
            {@html item.bodyHTML}
        </article>
</div>
{/each}

</section>


<style>
   * {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  height: 100vh;
}

h1 {
  text-align: center;
  margin-bottom: 10px;
}

:root {
  --bg-color: #10aec2;
}

.card:nth-child(4n) {
  --bg-color: #10aec2;
}
.card:nth-child(4n+1) {
  --bg-color: #fbc82f;
}
.card:nth-child(4n+2) {
  --bg-color: #74759b;
}
.card:nth-child(4n+3) {
  --bg-color: #346c9c;
}

.cards {
  position: relative;
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
  padding: 10px 16px;
}
.cards::after {
  z-index: 9;
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  left: 50%;
  border-left: 1px solid rgba(200,200,200,0.5);
}

.card {
  position: relative;
  width: 45%;
  height: 200px;
  display: flex;
  flex-direction: column;
  box-shadow: 0px 3px 1px -2px rgba(0,0,0,0.2), 0px 2px 2px 0px rgba(0,0,0,0.14), 0px 1px 5px 0px rgba(0,0,0,0.12);
}
.card:nth-child(odd) {
  align-self: flex-start;
}
.card:nth-child(even ) {
  align-self: flex-end;
}


.card__header {
  display: flex;
  align-items: center;
  width: 100%;
  height: 35%;
  color: #fff;
  background-color: var(--bg-color);
}
.card:nth-child(odd) .card__header::after {
  position: absolute;
  left: 100%;
  content: "";
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 10px 0 10px 18px;
  border-color: transparent transparent transparent var(--bg-color);
}
.card:nth-child(even) .card__header::after {
  position: absolute;
  right: 100%;
  content: "";
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 10px 18px 10px 0;
  border-color: transparent var(--bg-color) transparent transparent;
}
.card:nth-child(odd) .card__header::before {
  z-index: 10;
  position: absolute;
  left: calc(111.11% - 2.5px);
  content: "";
  width: 10px;
  height: 10px;
  border-radius: 10px;
  background-color: #bdbdbd;
  box-shadow: 0 0 2px 6px #fff;
}
.card:nth-child(even) .card__header::before {
  z-index: 10;
  position: absolute;
  right: calc(111.11% - 5px);
  content: "";
  width: 10px;
  height: 10px;
  border-radius: 10px;
  background-color: #bdbdbd;
  box-shadow: 0 0 2px 6px #fff;
}


.header__number {
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 20px;
  padding: 6px 14px;
  font-size: 2rem;
  background-color: rgba(0,0,0,0.17);
}
.header__title {
  display: flex;
  margin-left: 10px;
  flex-direction: column;
  font-size: 0.6rem;
}
.title__sub {
  padding-top: 6px;
  font-size: 1.2rem;
}


.card__article {
  width: 100%;
  background-color: #fff;
  border: 1px solid rgba(200,200,200,0.5);
  border-top: none;
  padding: 10px;
}
</style>
