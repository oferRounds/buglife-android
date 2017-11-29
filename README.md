<p align="center">
	<img src="https://ds9bjnn93rsnp.cloudfront.net/assets/logo/logotype_black_on_transparent_782x256-7256a7ab03e9652908f43be94681bc4ebeff6d729c36c946c346a80a4f8ca245.png" width=300 />
</p>

[![Documentation](https://img.shields.io/badge/documentation-latest-blue.svg)](http://www.buglife.com/docs/android)
[![Twitter](https://img.shields.io/badge/twitter-@BuglifeApp-blue.svg)](https://twitter.com/buglifeapp)

Buglife is an awesome bug reporting SDK & web platform for iOS apps. Here's how it works:

1. User takes a screenshot, or stops screen recording
2. User annotates their screenshot & writes feedback
3. Bug reports are pushed to your team's email/Jira/Slack/Asana/wherever you track bugs.

You can also find Buglife for iOS [here](https://github.com/buglife/buglife-ios).

<p align="center" style="margin-top: 20px; margin-bottom: 20px;">
	<img src="https://i.imgur.com/73pDl6Q.png" />
</p>

---

|   | Main Features |
|---|---------------|
| 👤 | Free + no account required |
| 📖 | Open source |
| 🏃🏽‍♀️ | Fast & lightweight |
| 🎨 | Themeable |
| 📩 | Automatic caching & retry |
| 📜 | Custom form fields, with pickers & multiline text fields  |
| ℹ️ | Advanced logging, with debug / info / warning levels |
| 📎 | Custom attachments, including JSON & SQLite support |

## Installation

1. Add `buglife-android` as a dependency to your app's `build.gradle`.

	```groovy
	dependencies {
		compile 'com.buglife.sdk:buglife-android:1.0.0'
	}
	```

2. Create an `Application` subclass in your project if you don't already have one. (And don't forget to add it to your app's `AndroidManifest.xml`.)

3. Add the following lines to the end of the `onCreate()` method in your app's `Application` subclass:

	```java
	Buglife.initWithEmail(this, "you@yourdomain.com");
	Buglife.setInvocationMethod(InvocationMethod.SCREENSHOT);
	```
	Be sure to replace `you@yourdomain.com` with your own email address; this is where bug reports will be sent to.
	
	##### Got an account?
	
	If you have a Buglife account already, you should initialize Buglife with your team's API key instead of your email:
	
	```java
	Buglife.initWithApiKey(this, "YOUR_API_KEY");
	Buglife.setInvocationMethod(InvocationMethod.SCREENSHOT);
	```

4. Build & run on a device; take a screenshot to report a bug!

5. Submit a bug report from your device, then check your email for a link to the Buglife web dashboard!

## Usage

Check out the [Buglife Android guide](http://www.buglife.com/docs/android) for configuration & customization options.

## License

```
Copyright (C) 2017 Buglife, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0
    
Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

