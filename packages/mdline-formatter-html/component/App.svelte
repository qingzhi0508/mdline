
<section class="box">

    {#each items.reverse() as item,index}
    
    <div class="listItem" data-index="{index}">
    
     <div class="listItemContent">
        <div class="listItemContent-date"> <span>{item.beginDate}</span>
            <span>{#if item.endDate}{item.endDate}{/if}</span>
        </div>
        <h3  class="title">{item.title}</h3>
        <div class="listItemContent-content">{@html item.bodyHTML}</div>
     </div>
    </div>
    {/each}
    </section>
    
    
    
    <style>
    * {
        margin: 0;
        padding: 0;
    }
    body {
        font-size: 14px;
        -webkit-user-select: none;
        -webkit-touch-callout: none;
        -webkit-tap-highlight-color:rgba(0, 0, 0, 0);
        -webkit-font-smoothing: antialiased;
        -webkit-text-size-adjust: 100%;
        font-family:"Helvetica Neue", Helvetica, Arial, sans-serif;
        word-wrap: break-word;
    
        padding-bottom: 20px;
    }
    img {
        width: 100%;
        display: block;
    }
    
    
    #list {
        margin: 0 4px 0;
        overflow-x: hidden;
        overflow-y: auto;
    }
    
    
    .title {
        color: #5ed3bf;
        font-size: 1.4em;
    }
    .listItem {
        position: relative;
        padding-left: 40px;
        padding-top: 4px;
    }
    .listItem:before {
        content: "";
        display: inline-block;
        position: absolute;
        top: 0;
        left: 0;
        width: 1px;
        height: 100%;
        border-right: 1px solid rgb(168, 163, 163);
        left: 19px;
        z-index: 1;
    }
    .listItem-first:before {
        height: 50%;
        top: 50%;
    }
    .listItem-last:before {
        height: 50%;
    }
    .listItem:after {
        content: "";
        display: inline-block;
        position: absolute;
        width: 8px;
        height: 8px;
        background-color: #5ed3bf;
        border-radius: 4px;
        left: 16px;
        top: 50%;
        margin-top: -2px;
        z-index: 1;
    }
    .listItem.highlight:after {
        -webkit-box-sizing: border-box;
        -moz-box-sizing: border-box;
        box-sizing: border-box;
        width: 16px;
        height: 16px;
        background-color: #3d93fd;
        border: 4px solid #88bdfe;
        border-radius: 8px;
        left: 12px;
        -webkit-box-shadow: 0 0 0 3px #d8e9ff;
        box-shadow: 0 0 0 3px #d8e9ff;
        z-index: 2;
    }
    .listItem.highlight > .listItemContent {
        background-color: #3d93fd;
        color: #fff;
    }
    .listItem.highlight .listItemContent-date{
        color: rgb(24, 22, 22);
    }
    
    .listItemContent {
        padding: 5px;
        border: 1px solid rgb(172, 169, 169);
        border-radius: 4px;
    }
    .listItemContent-date {
        color: #161515;
    }
      </style>
    
    