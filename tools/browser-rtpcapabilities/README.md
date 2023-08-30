# browser-RtpCapabilities

This tool generates default SDP Offer/Answer messages from the web browser you use to run it, and uses that to generate an equivalent mediasoup `RtpCapabilities` object.

Run it like this:

```sh
npm install
npm run start
```

Now, open a web browser at http://127.0.0.1:8080, and click on *Run*.

The resulting text is source code of a JavaScript object, which that you can copy-paste into the file [mediasoup-sdp-bridge/src/BrowserRtpCapabilities.ts](../../src/BrowserRtpCapabilities.ts).
