# webxr
The run/debug locally:
1. Setup the Meta Quest 3 in developer mode (by pairing with the Meta cellphone app, must create a meta account and pair with headset)
2. Connect the headset to computer with USB-C
3. Make sure you can connect with adb `adb devices` (sometimes `adb kill-server` helps)
4. Start a local webserver (e.g., `python -m http.server 8080`)
5. Port-forward to the headset: `adb reverse tcp:8080 tcp:8080`
6. Open the web browser on the meta quest and navigate to `http://localhost:8080/`, then select the desired webpage (e.g. `demo0.html`)
7. On the computer, in chrome, you can navigate to `chrome://inspect/#devices` to inspect the running webapp on the Meta Quest3 browser. This is very useful for debugging.
