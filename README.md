const { Client, Intents } = require('discord.js-selfbot-v13');
const Discord = require('discord.js-selfbot-v13');
const readline = require('readline-sync');
const m = require("moment-duration-format");
const express = require('express')
const app = express();
const port = 8000

app.get('/', (req, res) => res.send('ทำงานเรียบร้อยแล้ว'))
app.listen(port, () =>
    console.log(`Your app is listening at http://localhost:${port}`)
);

const client = new Client({
  checkUpdate: false
});


client.on('ready', async () => {

        if (global.dataWeather && global.dataWeather.current_weather) {
          global.temp = global.dataWeather.current_weather.temperature;
          global.wind = global.dataWeather.current_weather.windspeed

        } else {
          global.temp = 25
          global.wind = 3.5
        }

 const num = parseFloat((Math.random() * 0.2 + 0.1 + Number.EPSILON).toFixed(1));
        const operator = Math.random() < 0.3 ? '+' : '-';

  setInterval(() => {
    const moment = require('moment');
    const created = moment().format('YYYY-MM-DD HH:mm:ss ');

  // <-----------------------------------------------------------------------------------> 


    const change = ['https://cdn.discordapp.com/attachments/1160471479092269148/1161145509130551296/6f40010dbf9ad18584707eb0fafe4a9b.gif?ex=65373c06&is=6524c706&hm=918b30c73788d77e5b4eb514ac85ac763d74993e80237a866e953f18250d37a5&','https://cdn.discordapp.com/attachments/1160471479092269148/1161145509516431480/86805ab550586369a6d2e9c6a8823c97.gif?ex=65373c06&is=6524c706&hm=a24e7f81e1a76197a539f2f864726d1ff0acfae567a0384ab827a090e2609336&','https://cdn.discordapp.com/attachments/1160471479092269148/1161145845555671100/236968b438117c04438e452c2ad5cad9.gif?ex=65373c56&is=6524c756&hm=f3d6c929315bcb15ee3a4f1859fe1ca1288d4e6a19284c4ca07340a5cbb43921&','https://cdn.discordapp.com/attachments/1160471479092269148/1161146119988989982/36bf01afc846e1510704c6d6e3f4c11b.gif?ex=65373c98&is=6524c798&hm=52373f02e8fb3de4f1bd9f9393a7047ddbe7d9933beec6b45614fced4946a53c&','https://cdn.discordapp.com/attachments/1160471479092269148/1161153886472654918/1a41580d44df6fc7b8a1ef0a6fd1bb52.gif?ex=653743d3&is=6524ced3&hm=ce5a20be3a9bca23520f3169b118c29437ebd1c3690666cedd01b20420836d68&','https://cdn.discordapp.com/attachments/1160471479092269148/1161154547218133063/271429a1b1cb41ff1403ed57bd9b1a7d.gif?ex=65374471&is=6524cf71&hm=5366b227a4ddbf3fb9cb205c8b0830fc8390a44d90e45e60123232422fe5cedb&','https://cdn.discordapp.com/attachments/1160471479092269148/1161155130171858944/c2ca6c6253bb062e191bc23078faeea3.gif?ex=653744fc&is=6524cffc&hm=d3adf6cdf7c7899ca4941a446e95bacdee638772e507ac6c2f0de3671d3a101e&','https://cdn.discordapp.com/attachments/1160471479092269148/1161156092605243392/00307934c44ef5838a9afdd820596011.gif?ex=653745e1&is=6524d0e1&hm=26068efe51b21833f69aa5c7fcfae83205c089e2d96ad56f98f04f364d51c974&','https://cdn.discordapp.com/attachments/1160471479092269148/1161156533405618256/1b46992047537f3a4b80c301db31c1da.gif?ex=6537464a&is=6524d14a&hm=16cf6e7cc0f1500c48735c89bfd518c8fc6ec696ff6c6e52e3193e560a6c67b7&','https://cdn.discordapp.com/attachments/1160471479092269148/1161158138507051028/1f5fbb3580b2211631d958457449f1ee.gif?ex=653747c9&is=6524d2c9&hm=d900fd0644fb7afea04705e30712b6e31cbdc4bdcac3d8556f87be60c406370a&&','https://cdn.discordapp.com/attachments/1160471479092269148/1161159065246904390/4debd6d94adcb8800c9308761b5fe724.gif?ex=653748a6&is=6524d3a6&hm=6c839f1007907746af59ae4d4ff46d2a5c2d66954bf79663f07b03b7669b91e1&','https://cdn.discordapp.com/attachments/1160471479092269148/1161159100525203486/38cf3635645a9797038cc571f71e1ed2.gif?ex=653748ae&is=6524d3ae&hm=c0a638ffe1f8d40c96ceea4de4e9a6857eb50a4fbf62107192837121994cc4c6&','https://cdn.discordapp.com/attachments/1160471479092269148/1161159278489514044/4a57f4256ddfb3e44068892e987222cd.gif?ex=653748d9&is=6524d3d9&hm=b45d11c4006d6dc247e326484ad3c22154a30bf3a3fff7a9980832d52e23216f&','https://cdn.discordapp.com/attachments/1160471479092269148/1161159496341659728/4f9087f13efb82ed77703b725ebba87e.gif?ex=6537490d&is=6524d40d&hm=f1b8e6c7e036d0bc0dc2451cab30d71079a7ced0f8a8bf2812d50a21ff0b19ed&','https://cdn.discordapp.com/attachments/1160471479092269148/1161159834964611174/96e9461f0f78ebc4a9344891444cd6a9.gif?ex=6537495d&is=6524d45d&hm=708a9be6f62cc3434ca471e12743423c9a2407ca9d8db7c8d520c41e05f96b25&']; //รูปใหญ่

    const poop = ['https://media.discordapp.net/attachments/1155965892853760030/1155966065277411328/1102270930023088280.gif?ex=652d9eca&is=651b29ca&hm=e90db3d12a3429e672e0a7bc937bc3a8c9f09649caca01876b0a4d23881c95f3&=']; // รูปเล็ก

   const change2 = ['Twitch','TikTok','YouTube','Netflix','Disney+','MONOMAX','Facebook','HBO GO','iQIYI','Viu','We TV','Amazon','Spotify','TrueID+',
   'AIS Play','BiliBili','YOUKU','Pornhub','Steam','FiveM','RedM','LDPlayer','Noxplayer','BlueStacks','Nitro Boost 1 Year','Twitter','Roblox','Microsoft Store','Google Chrome','Mozilla Firefox','Brave','Microsoft Edge','Opera GX','Epic Games Store','Open Broadcaster Software']; // ข้อความตรง กำลังเล่น

    const change3 = ['Twitch','Facebook Gaming','YouTube']; // ชื่อ ด้านบนสุด

    const iooi = ['🐰TikTok🐰','🦄TikTok🦄','🦉TikTok🦉','🐳TikTok🐳','🐑TikTok🐑','🦝TikTok🦝']; // ชื่อ ปุ่ม 1

    const iiio = ['https://www.tiktok.com']; // ลิ้ง ปุ่ม 1

   const yyyt = ['🍰Twitch🍰','🍜Twitch🍜','🍫Twitch🍫','🍹Twitch🍹','🍳Twitch🍳','🍭Twitch🍭']; // ชื่อ ปุ่ม 2

   const ddds = ['https://www.twitch.tv']; // ลิ้ง ปุ่ม 2



  // <----------------------------------------------------------------------------------->  



   const tyyy = yyyt[Math.floor(Math.random()*yyyt.length)];
   const sddd = ddds[Math.floor(Math.random()*ddds.length)]; 
   const oooi = 
iiio[Math.floor(Math.random()*iiio.length)]; 
   const ioii =
iooi[Math.floor(Math.random()*iooi.length)];
    const popp =
poop[Math.floor(Math.random()*poop.length)];
    const ssss = 
change[Math.floor(Math.random()*change.length)];
    const dwada = change2[Math.floor(Math.random()*change2.length)];
    const ap =
change3[Math.floor(Math.random()*change3.length)];;      
    const r = new Discord.RichPresence()
      .setApplicationId('1121867777867788309')
      .setType('STREAMING')
      .setURL('https://www.youtube.com/watch?v=uKM6TWZRz44')
      .setState(`${dwada}`)
      .setName(`Twitch`)
      .setDetails(`${ap}🍭${getTime()} ${moment().format ('DD/MM/YYYY')}`)
      .setAssetsSmallImage(`${popp}`) 
.setAssetsLargeImage(`${ssss}`)
.setAssetsLargeText(`🔥${operator === '+' ? (global.temp + num).toFixed(1) : (global.temp - num).toFixed(1)} °C🔥    🌠${operator === '+' ? (global.wind + num).toFixed(1) : (global.wind - num).toFixed(1)} m/s🌠`)
.setAssetsSmallText(`ping : ${Math.round(client.ws.ping)}`)
.addButton(`${ioii}`,`${oooi}`)  

      .addButton(`${tyyy}`,`${sddd}`)
.setStartTimestamp(Date.now())
.setEndTimestamp(Date.now())
    client.user.setActivity(r);
  },  2 * 1000 );
  console.log(`${client.user.username} Is Ready!`)
});


client.login(process.env.token)



   let endTime = new Date().setHours(24 + 6, 0, 0, 0), 
  today = new Date().setHours(0, 0, 0, 0),
  dayCount = Math.floor( 
    (today - new Date(2023, 0).getTime()) / (24 * 60 * 60 * 1000) 
  )

var date = new Date().getDate() + "/"+ (new Date().getMonth()+1)  + "/" + new Date().getFullYear();
    var time = new Date().getHours() + ":"+ new Date().getMinutes();

let options = {
    timeZone: 'Asia/Bangkok',
    year: 'numeric',
    month: 'numeric',
    day: 'numeric',
    hour: 'numeric',
    minute: 'numeric',
    hour12: false
  };

  function getDate() {
    return (new Date()).toLocaleString([], options).split(" ")[0].replaceAll(",", "");
  }
  function getTime() {
    return (new Date()).toLocaleString([], options).split(" ")[1].replaceAll(",", "");
          }

