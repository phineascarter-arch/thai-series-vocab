# 追泰劇學泰文 · thai-series-vocab

給完全初學者的泰劇學習 skill：從單集可核對的泰文字幕，整理繁體中文解釋、逐詞拆解、羅馬拼音、中文聲調與語氣說明，產出 HTML 學習手帳、Markdown 筆記與 Anki CSV。

## EP01 學習頁

- [開啟 EP01 學習網站](https://phineascarter-arch.github.io/thai-series-vocab/)
- [下載 Anki CSV](docs/anki-thai-girl-rules-EP01.csv)
- [閱讀 Markdown 筆記](docs/girl-rules-EP01-notes.md)

`docs/index.html` 是單一檔案，可下載後直接用瀏覽器開啟。包含《Girl Rules》EP01 四段共 47 個精選詞句，支援搜尋、分段、收藏、學會進度、中文自測、五題測驗及資料匯出。

GitHub Pages 完成部署後，網站連結會顯示於儲存庫的 Deployments 與 Actions 執行結果；尚未成功部署前，不要將預期網址當成已上線網址。

## 安裝 skill 到 Codex

本儲存庫根目錄就是 skill 目錄，包含 `SKILL.md`、`assets/`、`references/` 與 `agents/`。

在 Codex 對話中貼上本儲存庫網址並說：

```text
請使用 skill-installer，將這個 GitHub 儲存庫根目錄的 thai-series-vocab 安裝到我的個人 skills 目錄。
```

也可手動安裝。Windows PowerShell：

```powershell
git clone https://github.com/phineascarter-arch/thai-series-vocab.git "$env:USERPROFILE\.codex\skills\thai-series-vocab"
```

macOS／Linux：

```sh
git clone https://github.com/phineascarter-arch/thai-series-vocab.git ~/.codex/skills/thai-series-vocab
```

若目錄已存在，先確認是不是已安裝的版本，不要直接覆蓋本機修改。安裝後在下一則訊息明確呼叫 `$thai-series-vocab`；若客戶端尚未發現 skill，可開啟新對話。

## 使用

```text
使用 $thai-series-vocab，幫我整理《Girl Rules》EP02 四段，
合併成一份 HTML 學習頁、繁中筆記與 Anki CSV。
我是完全初學，請保留發音與聲調輔助。
```

可以附官方影片連結或提供泰文 `.srt`／`.vtt`／`.txt`。skill 先嘗試找可讀的泰文來源，取得失敗才請使用者補字幕。不把中英字幕回譯成泰文冒充原台詞，也不為湊數新增劇外例句。

## 語音與來源限制

之後新集數預設固定使用 **Microsoft Premwadee Neural 泰語女聲**（`th-TH-PremwadeeNeural`），以 MP3 內嵌播放，保留正常／慢速及 iPhone 點按播放流程。來源為 Microsoft 線上語音服務，既有產製工具為第三方 `edge-tts`；不會自行換回 Windows Pattara。

- EP01 頁面已內嵌 47 段 Microsoft Premwadee Neural 泰語女聲 MP3，支援正常與慢速播放；非演員原聲。
- 學習頁不需要伺服器，影片回看仍需要網路。
- 收藏與進度儲存在目前瀏覽器，未提供跨裝置同步；可匯出／匯入 JSON 備份。
- 範例使用官方影片的泰文自動字幕，可能有辨識誤差；羅馬拼音 是標準讀音輔助，未逐句核對演員音訊。
- 時間是字幕出現時觀察到的播放位置，非精確字幕起始時間。
- 僅保留精選學習短句，不提供整集字幕或影片。

## GitHub Pages 設定

網站檔案在 `docs/`，使用 GitHub Pages 的分支部署。

1. 在儲存庫 **Settings → Pages** 選擇 **Deploy from a branch**。
2. 分支選 **main**、資料夾選 **/docs**。
3. 後續將網站變更推送到 `main` 即自動更新。

GitHub Free 可用公開儲存庫部署 Pages；私人儲存庫是否可用取決於帳號方案。參考 [GitHub 官方部署說明](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)。

## 目錄

```text
SKILL.md                      技能主流程
agents/openai.yaml            Codex 顯示資訊
assets/learning-page.html     HTML 版型起點（需依劇集替換示範標籤）
references/html-learning-page.md  HTML 製作與驗證規則
docs/                         EP01 學習網站與可下載內容
```

原始英語工作流程參考 [pyang5166/gbro-series-vocab](https://github.com/pyang5166/gbro-series-vocab)。本 skill 獨立安裝，不會覆蓋英語版。影劇台詞與影片權利屬原權利人；網站與 skill 不代表製作公司或平台的官方產品。

