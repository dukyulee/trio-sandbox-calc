# trio-sandbox-calc

[ai-trio-relay](https://github.com/dukyulee/ai-trio-relay)를 실제 Claude Code 웹 · Codex 웹 · Antigravity로 시험하는 **실험용 저장소**다. 코드 자체에는 쓸모가 없다.

> ⚠️ 공개 저장소다. 실험 중에 생기는 `trio/*` 브랜치(조각 · 전달함 · integration)와 그 안의 편지도 모두 공개된다. 비밀값을 넣지 않는다.

작은 계산기다. 계약 파일 `src/types.js`(+ 그 시험)만 있고, 나머지 세 파일은 조각이 만든다.

| 조각 | 담당 | 고쳐도 되는 파일 |
|---|---|---|
| add | claude | `src/add.js` · `test/add.test.js` |
| mul | codex | `src/mul.js` · `test/mul.test.js` |
| format | antigravity | `src/format.js` · `test/format.test.js` (add · mul에 의존) |

- 계획: [plan.json](plan.json) → `trio plan --file plan.json` → `trio approve` → `trio run`
- 전체 시험: `node --test "test/*.test.js"`
