# tes1

CloudStream extension, version 7.

Add this repository URL in CloudStream:

https://raw.githubusercontent.com/alozfudi/tes1/main/repository-v7.json

Confirm the extension shows v7. Older installations can update through their repository; use the fresh URL above if an old version remains cached.

Version 7 explicitly requests Android hardware acceleration for the verification dialog before attaching its window. The diagnostic screen reports whether the WebView is actually hardware accelerated. On the official Cloudflare test page it also reads the real WebGL vendor and renderer. It never patches WebGL, canvas or navigator, or substitutes graphics values. A hardware-acceleration request cannot repair a device driver or guarantee challenge acceptance.

Open tes1 extension settings (gear), select **Tes Cloudflare**, then inspect its result. Select **Lihat diagnostik** and send a photo including the hardware acceleration, WebGL vendor and renderer lines if verification still fails. **Muat ulang** returns to the provider site. Complete verification there, select **Gunakan sesi**, then refresh the provider home page.

Diagnostic history stays available during page refreshes while the verification screen remains open. It is discarded when that screen closes and is never sent automatically. It excludes cookies, tokens and raw console output.

Page requests and the video interceptor continue to use one native CloudflareKiller instance. JavaScript, DOM storage and third-party cookie permissions remain enabled. The verification screen does not extract or copy cookies manually. Provider parsing and features are preserved.

Built successfully using `:Hanime1Provider:make`; ZIP integrity, manifest version/name and classes.dex checksums verified. Android device verification and UI have not been tested here. This update is a targeted rendering change, not a guaranteed solution for verification failure.
