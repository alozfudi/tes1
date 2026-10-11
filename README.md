# tes1

CloudStream extension, version 5.

Add this repository URL in CloudStream:

https://raw.githubusercontent.com/alozfudi/tes1/main/repository-v5.json

Install tes1 and confirm that the extension shows v5. If a previous repository still shows v3/v4, remove the old installation and add the fresh URL above.

Open the tes1 extension settings (gear), complete the site verification, select **Gunakan sesi**, then refresh the tes1 home page. The verification screen enables JavaScript, DOM storage and third-party cookies and displays Android/WebView versions plus detected numeric errors. **Muat ulang** reloads only when selected by the user.

Page requests and the video interceptor use one native CloudflareKiller instance. The verification screen does not extract or copy cookies manually. Existing provider parsing and features are preserved.

Built with the repository Gradle task `:Hanime1Provider:make`. ZIP integrity, manifest version/name and classes.dex checksums verified. Verification on an Android device has not been tested here; Cloudflare may still reject a device or session. If verification fails, send a photo including the version/error line at the top of the verification screen.
