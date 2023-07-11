# ElectronJs_Send_Notification

---

# Resimler

![image](https://github.com/fastuptime/ElectronJs_Send_Notification/assets/63351166/73048ebc-ab97-4f5e-9e27-acb6b21d3b1a)
![image](https://github.com/fastuptime/ElectronJs_Send_Notification/assets/63351166/38d86a27-f00b-462a-bfa7-1028defc471e)
![image](https://github.com/fastuptime/ElectronJs_Send_Notification/assets/63351166/de345c80-7e48-47f5-8ca1-9c9093f68734)

# Kod

```
process.env.NODE_TLS_REJECT_UNAUTHORIZED = "0";
const electron = require("electron");
const { app, Notification } = electron;
const path = require("path");

function sendNotification(title, body) {
  const notification = {
    title: title,
    body: body,
    icon: path.join(__dirname, "./256x256.ico"),
  };
  new Notification(notification).show();
}

async function start() {
  if (process.platform === 'win32') {
      app.setAppUserModelId(app.name);
  }
  sendNotification(`Selam ${process.env.USERNAME}`, "Hoşgeldin!");
  sendNotification("Bilgilendirme", "Bu uygulama sadece test amaçlıdır.");
}

app.on("ready", start);
```

---
- ✨ [Destek İçin](https://fastuptime.com) <br>
- 💕 [Discord](https://fastuptime.com/discord)<br>
- 🎖️ [FasterHost Technology](https://fasterhost.tech/)<br>
- ✨ İletişim için [Tıkla!](mailto:fastuptime@gmail.com)<br>

# License
- Its protected by Creative Commons ([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/))

<a href="https://creativecommons.org/licenses/by-nc-sa/4.0/" title="BYNCSA40"><img src="https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png"></a>
