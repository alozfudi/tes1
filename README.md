# tes1

CloudStream extension, version 8.

Add this repository URL in CloudStream:

https://raw.githubusercontent.com/alozfudi/tes1/main/repository-v8.json

Confirm the extension shows v8. Earlier repository lists also advertise v8; use the fresh URL above if an old version remains cached. After updating, force-stop and reopen CloudStream before retrying verification.

Version 8 fixes an incorrect User-Agent assignment in the verification screen. CloudflareKiller.getCookieHeaders() can return CloudStream's desktop HTTP fallback before its native WebView User-Agent has been initialized. Earlier verification screens copied that fallback, causing an Android WebView to advertise a Windows browser. The screen now keeps its actual default Android WebView User-Agent. Once the user selects **Gunakan sesi**, initial page requests also use that same User-Agent. CloudflareKiller continues to handle cookies and subsequent requests natively.

Open tes1 extension settings (gear), select **Tes Cloudflare**, and inspect its result. The **Lihat diagnostik** dialog includes the WebView User-Agent, hardware acceleration status and actual WebGL renderer. The test page's Browser section should reflect the real WebView, rather than an injected desktop HTTP fallback. **Muat ulang** returns to the provider site. Complete verification there, select **Gunakan sesi**, then refresh the provider home page.

Diagnostic history stays available during page refreshes while the verification screen remains open. It is discarded when that screen closes and is never sent automatically. It excludes cookies, tokens and raw console output. WebGL, canvas and navigator are not patched; GPU information is not fabricated.

Page requests and the video interceptor use one native CloudflareKiller instance. Provider parsing and features are preserved. JavaScript, DOM storage, third-party cookie permissions and the hardware-accelerated verification dialog remain enabled.

Built successfully with `:Hanime1Provider:make`; ZIP integrity, manifest version/name and classes.dex checksums verified. Android device verification and UI have not been tested here. The User-Agent bug is fixed in source; successful Cloudflare verification still needs confirmation on the device.
