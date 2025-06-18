# Task Cli App 仕様書

## 1. アプリ概要
- Python製のCLIアプリ
- 日常のタスクをターミナルから管理

## ２．目的
- GUIを立ち上げず、即時にタスク管理
- ローカルファイルで完結するシンプルな構造
- コードの拡張性・学習用途としても有用

## ３．想定ユーザー
- 開発者やPCユーザー
- CLIを使い慣れているユーザー
- 簡単なタスクをサクッと記録したい人

## ４．主要機能
| 機能       | 説明                                         |
|------------|----------------------------------------------|
| タスク追加 | `python task.py add "本を読む"`             |
| 一覧表示   | `python task.py list`                       |
| 完了設定   | `python task.py done 0`                     |
| 削除       | `python task.py delete 0`                   |
| 保存形式   | JSON形式でローカルファイルに永続保存       |

## ５．データ構造（JSON）
```JSON
[
  {
    "description": "本を読む",
    "done": false,
    "created": "2025-06-17T20:00:00"
  }
]
```

## ６．今後の拡張予定
- 優先度、締切日、タグの追加
- GUI版（Tkinter,Streamlit）
- Github Actionsによる自動テスト

## ７．ライセンス
MIT License

