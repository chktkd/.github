# .github

`chktkd` が所有するリポジトリの既定 Issue / PR テンプレートを置く、owner 共通の `.github` リポジトリ。

## Communication

- Respond in Japanese

## Commands

- 開発・テスト・lint: N/A（コードも lint 設定もなく、テンプレートと文書のみ）

## Critical Rules

- このリポジトリの `.github/` 配下は、自前のテンプレートを持たない全リポジトリの既定として使われる。変更は所有リポジトリ全体に影響するため、PR テンプレートや Issue テンプレートの項目を変えるときは理由を PR に書く。
- `.github/ISSUE_TEMPLATE/` はリポジトリ単位で丸ごと置き換わり、一部だけ継承できない。ファイルを追加する前に、この性質を前提に設計する。
- ここに置いたファイルは各リポジトリの clone に含まれない。他リポジトリの作業中に参照するときは `gh api repos/chktkd/.github/contents/<path>` で取得する。

## Production Impact

- デプロイ対象なし。main にマージした時点で、既定テンプレートとして GitHub が各リポジトリへ反映する。
- public リポジトリでなければ既定テンプレートとして使われない。機密情報を置かない。secrets なし。

## Project-Specific Notes

- Issue テンプレートは `issue.yml` の1種類に絞っている。種類別テンプレートは意図的に作らない。理由は README.md を参照する。
- 構成と仕組みの詳細は README.md を参照する。
