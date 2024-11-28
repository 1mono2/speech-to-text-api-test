# リアルタイム音声認識アプリケーション

このプロジェクトは、Google Cloud Speech-to-Text APIを使用して、マイクからの音声入力をリアルタイムでテキストに変換するPythonアプリケーションです。

## 機能

- リアルタイムの音声認識
- マイク入力のストリーミング処理
- テキストへの変換結果の即時表示

## 必要要件

- Python 3.10以上
- Google Cloud アカウントとプロジェクト
- Google Cloud Speech-to-Text APIの有効化
- 認証用のサービスアカウントキー

## インストール方法

1. リポジトリをクローン
```bash
git clone [repository-url]
cd speech-to-text-api-test
```

2. 仮想環境を作成し、依存パッケージをインストール
```bash
python -m venv .venv
source .venv/bin/activate  # Windowsの場合: .venv\Scripts\activate
pip install -r requirements.txt
```

3. Google Cloud の認証情報を設定
- Google Cloud Console からサービスアカウントキーをダウンロード
- 環境変数を設定
```bash
export GOOGLE_APPLICATION_CREDENTIALS="path/to/your/service-account-key.json"
```

## 使用方法

1. アプリケーションを起動
```bash
python test.py
```

2. マイクに向かって話しかけると、リアルタイムで音声認識が行われ、テキストとして表示されます。

## 設定

- サンプリングレート: 8000Hz
- チャンクサイズ: 800 (100ms)
- 音声チャンネル: モノラル（1チャンネル）

## ライセンス

このプロジェクトはMITライセンスの下で公開されています。

## 注意事項

- Google Cloud Speech-to-Text APIの使用には料金が発生する場合があります。
- 音声認識の精度は、マイクの品質や環境ノイズの影響を受ける場合があります。
