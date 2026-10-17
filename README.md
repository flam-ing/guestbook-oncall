# 방명록 운영 연습 (guestbook-oncall)

DB Inc AI 교육 2일차 2교시에서 쓰는 연습 저장소예요. 방명록 서비스를 막 열었고, 사용자의 버그 신고는 이 저장소의 **Issues**로 들어와요. 처음에는 이슈가 하나도 없어요.

이름, 글, 데이터는 모두 수업을 위해 만든 것이에요. 실제 서비스가 아니에요.

## 내 PC에서 켜기

```bash
git clone https://github.com/flam-ing/guestbook-oncall.git
cd guestbook-oncall
python3 app.py          # http://127.0.0.1:8000
python3 -m unittest     # 테스트
```

설치할 패키지는 없어요. Windows는 `python3` 대신 `python`을 써요. git이 없으면 위의 초록색 **Code** 단추에서 **Download ZIP**으로 받아도 돼요.

## 버그 신고하기

**Issues → New issue → 버그 신고**를 골라 재현 순서, 기대, 실제를 채워요.

## 자동 처리(온콜)

저장소 관리자가 이슈에 `autofix` 라벨을 붙이면 GitHub Actions가 Claude Code를 깨워요. Claude는 GitHub 서버에서 이슈를 재현하고, 원인 줄을 고치고, 회귀 테스트를 더한 뒤 결과를 이슈에 남겨요. 머지는 사람이 해요.

라벨은 쓰기 권한이 있는 사람만 붙일 수 있어요. 그래서 누구나 이슈를 쓸 수 있어도, 아무나 Claude를 깨울 수는 없어요.

일하는 규칙은 [CLAUDE.md](CLAUDE.md)에, 자동 처리 설정은 [.github/workflows/claude.yml](.github/workflows/claude.yml)에 있어요.
