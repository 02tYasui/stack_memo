# Poetry

## 事前作業
.tool-versionsの作成
```
python 3.11.6
poetry 1.7.0
```

## 新規プロジェクト立ち上げ

```shell
poetry new <project-name>
```

## 仮想環境を立ち上げ

```shell
poetry install
```

## パッケージ追加

```shell
poetry add <package-name>
```

## パッケージアップデート

```shell
poetry update --dry-run
poetry update
```

## 仮装環境実行

```shell
poetry run python <python-file>
```