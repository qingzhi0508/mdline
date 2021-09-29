<section class="box">
  <ul id="first-list">
    {#each items as item,index}
  
    <li>
        <span></span>
        <div class="title">{item.title}</div>
        <div class="info">{@html item.bodyHTML}</div>
        <div class="name"></div>
        <div class="time">
            <span>{item.beginDate}</span>
            <span>{#if item.endDate}{item.endDate}{/if}</span>
        </div>
    </li>
    {/each}
    
    <div class="arrow" id="btn1">
  
    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="Capa_1" x="0px" y="0px" width="512px" height="512px" viewBox="0 0 284.929 284.929" style="enable-background:new 0 0 284.929 284.929;" xml:space="preserve">
        <g>
            <g>
                <path d="M135.899,167.877c1.902,1.902,4.093,2.851,6.567,2.851s4.661-0.948,6.562-2.851L282.082,34.829    c1.902-1.903,2.847-4.093,2.847-6.567s-0.951-4.665-2.847-6.567L267.808,7.417c-1.902-1.903-4.093-2.853-6.57-2.853    c-2.471,0-4.661,0.95-6.563,2.853L142.466,119.622L30.262,7.417c-1.903-1.903-4.093-2.853-6.567-2.853    c-2.475,0-4.665,0.95-6.567,2.853L2.856,21.695C0.95,23.597,0,25.784,0,28.262c0,2.478,0.953,4.665,2.856,6.567L135.899,167.877z" fill="#FFFFFF"/>
                <path d="M267.808,117.053c-1.902-1.903-4.093-2.853-6.57-2.853c-2.471,0-4.661,0.95-6.563,2.853L142.466,229.257L30.262,117.05    c-1.903-1.903-4.093-2.853-6.567-2.853c-2.475,0-4.665,0.95-6.567,2.853L2.856,131.327C0.95,133.23,0,135.42,0,137.893    c0,2.474,0.953,4.665,2.856,6.57l133.043,133.046c1.902,1.903,4.093,2.854,6.567,2.854s4.661-0.951,6.562-2.854l133.054-133.046    c1.902-1.903,2.847-4.093,2.847-6.565c0-2.474-0.951-4.661-2.847-6.567L267.808,117.053z" fill="#FFFFFF"/>
            </g>
        </g>
        <g>
        </g>
        <g>
        </g>
        <g>
        </g>
        <g>
        </g>
        <g>
        </g>
        <g>
        </g>
        <g>
        </g>
        <g>
        </g>
        <g>
        </g>
        <g>
        </g>
        <g>
        </g>
        <g>
        </g>
        <g>
        </g>
        <g>
        </g>
        <g>
        </g>
    </svg>
    
  </div> 
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
  
  
  .arrow{
      position: absolute;
      top: 105%;
      left: 22%;
      cursor: pointer;
    height:20px;
    width:20px
  }
  
  .arrow:hover{
      -webkit-animation: arrow 1s linear infinite;
         -moz-animation: arrow 1s linear infinite;
           -o-animation: arrow 1s linear infinite;
              animation: arrow 1s linear infinite;
  }
  
  .box ul:last-of-type .arrow{
      position: absolute;
      top: 105%;
      left: 22%;
      transform: rotateX(180deg);
      cursor: pointer;
  }
  
  svg{
      width: 20px;
      height: 20px
  }
  
  @keyframes arrow{
      0%,100%{
          top:105%
      }
      50%{
          top:106%
      }
  }
  
  @-webkit-keyframes arrow{
      0%,100%{
          top:105%
      }
      50%{
          top:106%
      }
  }
  
  @-moz-keyframes arrow{
      0%,100%{
          top:105%
      }
      50%{
          top:106%
      }
  }
  
  @-o-keyframes arrow{
      0%,100%{
          top:105%
      }
      50%{
          top:106%
      }
  }
  
    </style>
  
  