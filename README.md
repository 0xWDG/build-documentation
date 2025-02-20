# Swift Package Documentation Generator

The Swift Package Documentation Generator GitHub Action generates documentation for a Swift package using docc.

```yaml
jobs:
  Build-documentation:
    runs-on: macos-latest
    steps:
      - name: Build documentation
        uses: 0xWDG/build-documentation@main
```

|Parameter|Description|Default value|
|---|---|---|
|product|Product name|\_\_AUTO\_\_|
|temppath|Temporary Directory to write to|tmpdocs|
|branch|Branch to write to|documentation|
|ios|Should we build for iOS?|false|


```yaml
# .github/workflows/build-documentation.yml
name: build-documentation

on:
  # Run on push to main branch
  push:
    branches:
      - main

  # Dispatch if triggered using Github (website)
  workflow_dispatch:

jobs:
  Build-documentation:
    runs-on: macos-latest
    steps:
      - name: Build documentation
        uses: 0xWDG/build-documentation@main
        with:
          product: Product-Name
          temppath: tmpdocs
          branch: documentation
          iOS: false # Build for iOS
```

## Contact

🦋 [@0xWDG](https://bsky.app/profile/0xWDG.bsky.social)
🐘 [mastodon.social/@0xWDG](https://mastodon.social/@0xWDG)
🐦 [@0xWDG](https://x.com/0xWDG)
🧵 [@0xWDG](https://www.threads.net/@0xWDG)
🌐 [wesleydegroot.nl](https://wesleydegroot.nl)
🤖 [Discord](https://discordapp.com/users/918438083861573692)

Interested learning more about Swift? [Check out my blog](https://wesleydegroot.nl/blog/).
