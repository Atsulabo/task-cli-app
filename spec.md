# Task Cli App 仕様書

## 1. アプリ概要
- Python製のCLIアプリ
- 日常のタスクをターミナルから管理

## ２．目的
- GUIを立ち上げず、即時にタスク管理→素早くタスク管理
- ローカルファイルで完結するシンプルな構造
- コードの拡張性・学習用途としても有用

## ３．想定ユーザー
- 開発者やPCユーザー
- CLIを使い慣れているユーザー
- 簡単なタスクをサクッと記録したい人

## ４．機能一覧
| ID | 機能           | 内容                     |
|----|----------------|--------------------------|
| F1 | タスク追加     | 新しいタスクを登録する   |
| F2 | 一覧表示       | 登録されたタスクを表示   |
| F3 | タスク完了設定 | 指定したタスクを完了にする |
| F4 | タスク削除     | タスクを削除する         |
| F5 | JSON保存       | 永続的にローカルに保存   |

## ５．データ設計
### Task構造
- description: str
- done: bool
- created: datetime(ISO文字列)

## ６.モジュール構成
- 'task.py':CLIエントリーポイント
- 'task_manager.py':TaskManagerクラス
　（いわばタスク群を扱うメソッドを集めたもの）
- 'task_model.py':Taskクラス
　（いわばタスク１つを扱うもの。主にデータ）

## ７．使用例（コマンド）
```bash
python task.py add "レポート提出"
python task.py list
python task.py done 0
python task.py delete 1
```

## ８．データ構造（JSON）
```JSON
[
  {
    "description": "本を読む",
    "done": false,
    "created": "2025-06-17T20:00:00"
  }
]
```

## ９．今後の拡張予定
- 優先度、締切日、タグの追加
- GUI版（Tkinter,Streamlit）
- Github Actionsによる自動テスト

## 10．ライセンス
MIT License

