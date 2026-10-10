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
| `.github/ISSUE_TEMPLATE/issue.yml` | 不具合・改善・作業を共通で扱う Issue テンプレート（背景・やること・完了条件） |
| `.github/ISSUE_TEMPLATE/config.yml` | テンプレートなしの Issue も作れるようにする |

Issue テンプレートを1種類にした理由: 2026-10 時点で所有リポジトリの Issue 197件のうち、種類別テンプレートから作られたものは約10件だった。手で書かれた Issue の大半は「背景 → やること → 完了条件」の構成だった。

## 注意

- このリポジトリは public でなければ既定テンプレートとして使われない。機密情報を置かない。
- 既定テンプレートは各リポジトリの clone に含まれない。ローカルのファイルを読む AI ツールやスクリプトは、`gh api repos/chktkd/.github/contents/<path>` で取得する。
