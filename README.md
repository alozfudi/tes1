# tes1

CloudStream extension, version 6.

Add this repository URL in CloudStream:

https://raw.githubusercontent.com/alozfudi/tes1/main/repository-v6.json

Confirm the extension shows v6. Older installations can update through their repository; use the fresh URL above if an old version remains cached.

Open the tes1 extension settings (gear). Complete the site verification, select **Gunakan sesi**, then refresh the tes1 home page.

If the site repeatedly refreshes after verification fails, use **Lihat diagnostik**. This native dialog shows Android/WebView versions, device time and the last 32 captured diagnostic events, without cookies, tokens or raw console output. The history remains available across page refreshes while the verification screen is open. It is discarded when that screen closes and is never sent automatically.

**Tes Cloudflare** opens Cloudflare's official compatibility checker in the same WebView. This button is outside the website and remains available during automatic page refreshes. Send a photo of its results and the diagnostic dialog if verification still fails. **Muat ulang** returns to the provider website and preserves the diagnostic history.

Page requests and the video interceptor continue to use one native CloudflareKiller instance. JavaScript, DOM storage and third-party cookie permissions remain enabled. The verification screen does not extract or copy cookies manually. Existing provider parsing and features are preserved.

This is a diagnostic update, not a guaranteed solution for verification failure. Built successfully using `:Hanime1Provider:make`; ZIP integrity, manifest version/name and classes.dex checksums verified. Android device verification and UI have not been tested here.
