# github-issue-labels
- ๐ท๏ธ ์ต์ ์ ์ด์ ๋ผ๋ฒจ ์ธํธ๋ฅผ ์ฐพ๊ธฐ ์ํ ์ฌ์ 

---

## About labels
- issue, pull requests, discussions ๋ฅผ ๋ถ๋ฅํ๋ ์ฉ๋
- ๊ฐ repo ๋ง๋ค ์ค์ ํ  ์ ์๋ค.
- ๋ฐ๋๋ก ๋งํ๋ฉด ๊ฐ repo ๋ง๋ค ์ค์ ํด์ผ ํ๋ค.

## Default labels
![default labels](.%5B20210714%5D_github_labels_images/4461721f.png)

๋ผ๋ฒจ | ์ค๋ช | Close ๊ธฐ์ค (์ด๊ฑด ๋ด ๋ง์)
--- | --- | ---
bug | ๋ฒ๊ทธ ์์  | ๋ฒ๊ทธ ์์ 
documentation | ๋ฌธ์์ ๋ํ ๊ฐ์ , ์ถ๊ฐ | ๋ฌธ์ ์๋ฐ์ดํธ
duplicate | ์ค๋ณต | ์๋ณธ ๋งํฌ ๋จ๊น
enhancement | ์๋ก์ด ๊ธฐ๋ฅ ์์ฒญ | ๊ตฌํ
good first issue | ์ฒซ ๊ธฐ์ฌ์์๊ฒ ์ข์ ์ด์ | ํด๊ฒฐ
help wanted | ๊ด๋ฆฌ์๊ฐ ์ด์ ๋๋ PR์ ๋ํด ๋์ ์์ฒญ | ํด๊ฒฐ
invalid | ๋์ด์ ๊ด๋ จ ์์ | ์ด์  ๋จ๊น
question | ์ง๋ฌธ | ๋ต๋ณ, ํด๊ฒฐ
wontfix | ๋์ํ์ง ์์ ๊ฒ | ์ด์  ๋จ๊น
- ์ฐธ๊ณ  : [GitHub Docs - Managing labels](https://docs.github.com/en/issues/using-labels-and-milestones-to-track-work/managing-labels#about-labels)

## Custom labels
- Personal access token ํ์ํ๋ค.
    - [GitHub Docs - Creating a personal access token](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token#using-a-token-on-the-command-line)
    - token scopes - repo ๋ฃ์ด์ค์ผ ํ๋ค.

### labels.json
- ์ด๋ฆ์ด ๊ผญ labels ์ผ ํ์๋ ์๋ค.
- `name`, `color`, `description` ์ ์ํ  ์ ์๋ค.
```json
[
  {
    "name": "๋ผ๋ฒจ_์ด๋ฆ",
    "color": "Hex_code",
    "description": "๋ผ๋ฒจ_์ค๋ช"
  }
]
```

### ์ ์ฉํ๊ธฐ
```text
npx github-label-sync --access-token <token> --labels <json_ํ์ผ๋ช> <username>/<repo>
```
