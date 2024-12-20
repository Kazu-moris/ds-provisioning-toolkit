# ds-provisioning-toolkit

データサイエンスやデータエンジニアリングのローカル開発環境を素早く構築するためのテンプレートツールキットです。

## 概要

本質的にやりたいことは、データのロジックの部分に集中できる状態をローカルに実現すること。

そしてそれは、すぐにクラウドへのデプロイやCICDへの移行ができることを前提に考えられるべき。

このツールキットは、以下のような作業を行う際の環境構築を支援します：

- データ分析のプロトタイピング
- 機械学習モデルの開発と検証
- データパイプラインの構築
- ビジュアライゼーションの作成
- dbtを使用したデータモデリングとトランスフォーメーション

## 主な機能

- Jupyter Notebook/Lab環境の提供
- 一般的なデータサイエンスライブラリ（pandas, numpy, scikit-learn等）の事前設定
- データベース接続用のツール
- 環境の再現性を保証するための設定ファイル
- dbt Core環境の自動セットアップ
- dbtプロジェクトテンプレートの提供
- データモデリング用のサンプルマクロとテスト
- コード品質を維持するための各種Linter/Formatter
  - Python: black, isort, flake8, mypy
  - SQL: sqlfluff
  - Jupyter Notebook: nbformat
  - YAML: yamllint
  - シェルスクリプト: shellcheck

## コンテナ環境について

本プロジェクトではDockerを使用して開発環境を構築します。以下の特徴があります：

- VS Code Dev Containersとの互換性
- docker-composeによる複数サービスの管理
- 環境の再現性と移植性の確保

### 代替コンテナランタイム

本プロジェクトはPodmanへの移行も考慮して設計されています：

- Dockerfileとdocker-compose.ymlは Podman互換
- 必要に応じてPodmanへの移行が可能
- チーム開発においてはコンテナランタイムの選択を統一することを推奨

## 必要要件

### 必須
- Python 3.8以上
- Docker Engine 24.0以上
  - または Podman 4.0以上（Dockerの代替として使用可能）
- dbt Core 1.5以上
- 対応データウェアハウス（BigQuery, Snowflake, Redshift等）へのアクセス権限
- Git
- pre-commit（コード品質チェック自動化用）

### 推奨
- VS Code + Dev Containers拡張機能
- Docker Desktop（Windows/Mac環境の場合）

## 使い方

[ここに具体的な使用方法や環境構築手順を記載]

## ライセンス

[ここにライセンス情報を記載]