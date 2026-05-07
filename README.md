# AnjoWSS-IOS.js


const KELLERSS_IOS = "https://raw.githubusercontent.com/kellerzz/KellerSS-iOS/refs/heads/main/KellerSS-iOS.js"

let req = new Request(KELLERSS_IOS)
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
