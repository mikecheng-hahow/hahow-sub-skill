# Hahow SUB Skill

字幕製作規範，設計給 [Claude Code](https://claude.com/claude-code) 或其他支援自訂 skill／system prompt 的 LLM agent 使用，用來把 `.srt` 字幕檔依固定規則修正（行長、標點、空格、用字一致性、口說優先原則等 11 條規則）。

來源：Hahow 字幕製作規範 20Q3。

## 使用方式

**Claude Code**：把 `SKILL.md` 放進專案的 `.claude/skills/` 或全域 `~/.claude/skills/` 目錄下，即可用 `/sub`（或依你設定的觸發詞）呼叫。

**其他 agent／LLM**：把 `SKILL.md` 的內容整份貼進 system prompt 或當作規則文件餵給模型，指示它依此規則逐條檢查、修正字幕檔即可。

## 核心原則

1. 行長限制（全形 15 字／半形 30 字）
2. 字幕不用標點，改用半形空格斷句；引號／書名號需成對且不可跨條
3. 程式碼符號全形化（避免字幕系統誤判標籤）
4. 中英文、數字之間補空格
5. 專有名詞大小寫與拼法一致
6. **口說優先**：字幕依老師／講者實際講出來的話製作，不是定稿文字；僅允許口誤修正與贅字刪修兩種例外
7. 斷句依語氣自然斷開，不拆完整語塊
8. 不確定內容標示、交件命名規則等

完整規則見 [`SKILL.md`](./SKILL.md)。

## License

MIT，見 [`LICENSE`](./LICENSE)。
