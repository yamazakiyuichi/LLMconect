# C:\GitHub\LLMconnect にデータを配置する手順

この実行環境（Linux コンテナ）から、あなたのローカル Windows パス `C:\GitHub\LLMconnect` へ直接ファイルを書き込むことはできません。

代わりに、以下を **Windows 側** で実行してください。

## PowerShell 手順

```powershell
New-Item -ItemType Directory -Force -Path C:\GitHub\LLMconnect | Out-Null
Set-Location C:\GitHub\LLMconnect

# 例: GitHub からデータを取得する場合
# git clone <データのURL> .

# 例: ZIP を落として展開する場合
# Invoke-WebRequest -Uri <ZIP_URL> -OutFile data.zip
# Expand-Archive -Path .\data.zip -DestinationPath . -Force
```

## このリポジトリを使う場合

このリポジトリの内容を配置したい場合は、以下を実行:

```powershell
git clone <このリポジトリURL> C:\GitHub\LLMconnect
```

