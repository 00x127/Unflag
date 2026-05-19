## What this does

Some apps use `FLAG_SECURE` to block screenshots. This attempts to bypass it so screenshots and screen recording work again.

```bash
adb shell settings put global disable_screen_secure 1
```

**Revert:**

```bash
adb shell settings put global disable_screen_secure 0
```

**Check state:**

```bash
adb shell settings get global disable_screen_secure
```

## Requirements

* Any Android device (5.0+)
* USB cable
* [ADB](https://developer.android.com/tools/releases/platform-tools) installed on your computer
* USB debugging enabled on the phone
  * Go to Settings -> About phone -> Tap "Build number" 7 times
  * Go back to Settings -> Developer options -> Enable "USB debugging"

## Persistence

Resets on reboot. Re-run the command if needed.
