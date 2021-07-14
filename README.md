# github-issue-labels
- 🏷️ 최적의 이슈 라벨 세트를 찾기 위한 여정

---

## About labels
- issue, pull requests, discussions 를 분류하는 용도
- 각 repo 마다 설정할 수 있다.
- 반대로 말하면 각 repo 마다 설정해야 한다.

## Default labels
![default labels](.%5B20210714%5D_github_labels_images/4461721f.png)

라벨 | 설명 | Close 기준 (이건 내 마음)
--- | --- | ---
bug | 버그 수정 | 버그 수정
documentation | 문서에 대한 개선, 추가 | 문서 업데이트
duplicate | 중복 | 원본 링크 남김
enhancement | 새로운 기능 요청 | 구현
good first issue | 첫 기여자에게 좋은 이슈 | 해결
help wanted | 관리자가 이슈 또는 PR에 대해 도움 요청 | 해결
invalid | 더이상 관련 없음 | 이유 남김
question | 질문 | 답변, 해결
wontfix | 대응하지 않을 것 | 이유 남김
- 참고 : [GitHub Docs - Managing labels](https://docs.github.com/en/issues/using-labels-and-milestones-to-track-work/managing-labels#about-labels)

## Custom labels
- Personal access token 필요하다.
    - [GitHub Docs - Creating a personal access token](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token#using-a-token-on-the-command-line)
    - token scopes - repo 넣어줘야 한다.

### labels.json
- 이름이 꼭 labels 일 필요는 없다.
- `name`, `color`, `description` 정의할 수 있다.
```json
[
  {
    "name": "라벨_이름",
    "color": "Hex_code",
    "description": "라벨_설명"
  }
]
```

### 적용하기
```text
npx github-label-sync --access-token <token> --labels <json_파일명> <username>/<repo>
```
