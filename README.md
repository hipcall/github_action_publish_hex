# Hipcall Github Action for Publish a Hex Package

* Create a key on your hex.pm dashboard.
* Add the key to your GitHub repository’s secrets. Call it HEX_API_KEY.
* Use this GitHub Action in your workflow:

```yaml
on:
  push:
    tags:
      - '*'

jobs:
  publish:
    runs-on: ubuntu-latest
    steps:
      - name: Check out
        uses: actions/checkout@v3

      - name: Publish package to hex.pm
        uses: hipcall/github_action_publish_hex@v1
        env:
          HEX_API_KEY: ${{ secrets.HEX_API_KEY }}
```

## Hipcall

All [Hipcall](https://www.hipcall.com/en-gb/) libraries:

- [HipcallDisposableEmail](https://github.com/hipcall/hipcall_disposable_email) - Simple library checking the email's domain is disposable or not.
- [HipcallDeepgram](https://github.com/hipcall/hipcall_deepgram) - Unofficial Deepgram API Wrapper written in Elixir.
- [HipcallOpenai](https://github.com/hipcall/hipcall_openai) - Unofficial OpenAI API Wrapper written in Elixir.
- [HipcallWhichtech](https://github.com/hipcall/hipcall_whichtech) - Find out what the website is built with.
- [HipcallSdk](https://github.com/hipcall/elixir_sdk/) - Official Hipcall API Wrapper written in Elixir.
- [Github Action for Hex](https://github.com/hipcall/github_action_publish_hex)