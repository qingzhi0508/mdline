<section class="box">
  <ul id="first-list">
    {#each items as item,index}
  
    <li>
        <span></span>
        <h1 class="title">{item.title}</h1>
        <div class="info">{@html item.bodyHTML}</div>
        <div class="name"></div>
        <div class="time">
            <span>{item.beginDate}</span>
            <span>{#if item.endDate}{item.endDate}{/if}</span>
        </div>
    </li>
    {/each}
    
  </ul>
    
   
  
  </section>>
  
  <style>
  body{
      margin: 1;
      padding: 1;
      font-family: arial
  }
  
  .box{
      overflow: hidden;
      padding: 10px 0 40px 60px
  }
  
  .box ul{
      list-style-type: none;
      margin: 0;
      padding: 0;
      position: relative;
      transition: all 0.5s linear;
      top:0
  }
  
  .box ul:last-of-type{top:80px}
  
  .box ul:before {
      content: "";
      display: block;
      width: 0;
      height: 100%;
      border: 1px dashed #968b8b;
      position: absolute;
      top: 0;
      left:  -6.3%;
  }
  
  .box ul li{
      margin: 0 0 8%;
      position: relative;
      padding: 2% 1%;
      border-radius: 10px;
      border: 1px solid rgb(222, 222, 222);
     
      margin-left: 5%;
  }
  
  
  .box ul li > span{
      content: "";
      display: block;
      width: 0;
      height: 100%;
      border:1px solid #afa8a8;
      position: absolute;
      top:0;
      left:-12%;
  }
  
  .box ul li > span:before,.box ul li > span:after{
      content: "";
      display: block;
      width: 20px;
      height: 20px;
      border-radius: 50%;
      position: absolute;
  }
  
  .box ul li > span:before{top:-10px}
  .box ul li > span:after{top:95%}
  
  .box .title{
      color: #5ed3bf;
      font-size: 1.4em;
      margin: 0;
      padding: 0 0 0.5em 0;
      letter-spacing: 0.1em;
  }
  
  .box .info:first-letter{text-transform: capitalize;line-height: 1.7}
  
  .box .name{
      margin-top: 10px;
      text-transform: capitalize;
      font-style: italic;
      text-align: right;
      margin-right: 20px
  }
  
  .box .time span{
    position: absolute;
      left: -14%;
      font-size: 80%;
      font-weight: bold;
      display: block;
      clear: both;
      padding: 0.25em 0;
      border: 1px solid rgb(222, 222, 222);
      background-color: #80e6baba;
  }
  .box .time span:first-child{top:-16px}
  .box .time span:last-child{top:94%}
  
    </style>
  
  