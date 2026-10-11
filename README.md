# tes1

CloudStream extension, version 9.

Add this repository URL in CloudStream:

https://raw.githubusercontent.com/alozfudi/tes1/main/repository-v9.json

Confirm the extension shows **v9**. Earlier repository indexes also advertise v9; use the fresh URL above if an older version remains cached.

Version 8 verification succeeded on the user's Android device, but the provider home page still reported that verification was required after selecting **Gunakan sesi**. Version 9 fixes an overly broad HTML challenge detector: Cloudflare's `/cdn-cgi/challenge-platform/` scripts may be injected into normal pages as passive JavaScript Detections. Their presence alone no longer causes a normal page to be rejected. Challenge detection now checks the official `cf-mitigated: challenge` header, HTTP 403/503, recognizable interstitial elements and challenge HTML. Normal provider listing/player content is accepted when no blocking status or header is present.

Open tes1 settings (gear), complete verification, select **Gunakan sesi**, then refresh the provider home page. The **Lihat diagnostik** dialog now includes the last page request status and challenge classification. Errors distinguish an unactivated session from a session that was activated but whose subsequent request remains blocked. Diagnostics exclude cookies, tokens, raw response bodies and full request URLs; they are never transmitted automatically.

The actual default Android WebView User-Agent is preserved. Page requests use that verified identity and one native CloudflareKiller instance, which also serves as the video interceptor. Provider parsing, categories, search, pagination, detail loading and video extraction are preserved. Hardware acceleration, JavaScript, DOM storage and third-party cookie permissions remain enabled. No WebGL, canvas or navigator spoofing is used.

Built successfully with `:Hanime1Provider:testDebugUnitTest :Hanime1Provider:make`. All nine challenge-classification regression tests passed. ZIP integrity, manifest version/name and classes.dex checksums were verified. The Android home-page runtime still requires testing on the user's device.
