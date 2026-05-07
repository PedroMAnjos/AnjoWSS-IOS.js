# AnjoWSS-IOS.js


const AnjoWSS-IOS.js = "https://github.com/PedroMAnjos/AnjoWSS-IOS.js/blob/main/AnjoWSS-IOS.js"

let req = new Request(AnjoWSS-IOS.js)
let code = await req.loadString()

if (!code || code.startsWith("404")) {
  let a = new Alert()
  a.title = "Erro"
  a.message = "Nao foi possivel baixar o script."
  a.addAction("OK")
  await a.present()
} else {
  eval(code)
}
