# .github

`chktkd` が所有するリポジトリの既定 Issue / PR テンプレートを置くリポジトリ。

## 仕組み

自前のテンプレートを持たないリポジトリでは、GitHub がこのリポジトリの `.github/` 配下のテンプレートを使う。
リポジトリに同じ種類のファイルがあれば、そちらが優先される。
`.github/ISSUE_TEMPLATE/` は丸ごと置き換わるため、一部のテンプレートだけを継承することはできない。

公式ドキュメント: [Creating a default community health file](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)

## 構成

| ファイル | 用途 |
| :-- | :-- |
| `.github/PULL_REQUEST_TEMPLATE.md` | PR テンプレート |
| `.github/ISSUE_TEMPLATE/bug_report.yml` | バグ報告 |
| `.github/ISSUE_TEMPLATE/feature_request.yml` | 機能提案 |
| `.github/ISSUE_TEMPLATE/question.yml` | 質問 |
| `.github/ISSUE_TEMPLATE/config.yml` | 空 Issue を無効化 |

## 注意

- このリポジトリは public でなければ既定テンプレートとして使われない。機密情報を置かない。
- 既定テンプレートは各リポジトリの clone に含まれない。ローカルのファイルを読む AI ツールやスクリプトは、`gh api repos/chktkd/.github/contents/<path>` で取得する。
- `labels` に指定したラベルが存在しないリポジトリでは、そのラベルは付かない。
