# Evidence Template Project

Welcome to Evidence. Use this project template to get started.

[Share your feedback with the Evidence team](https://du3tapwtcbi.typeform.com/to/GZNZe1GY)

## Getting Started

Check out the docs for [alternative install methods](https://docs.evidence.dev/getting-started/install-evidence) including Docker, Github Codespaces, and alongside dbt.

```shell
npx degit evidence-dev/template my-project
cd my-project 
npm install 
npm run dev 
```

Once you've launched Evidence, this project includes a short tutorial to help you get started.

Don't clone this repo, just download the code using the steps above.

## Codespaces

If you are using this template in Codespaces, use the following commands to get started:

```shell
npm install
npm run dev -- --host 0.0.0.0
```

See [the CLI docs](https://docs.evidence.dev/cli/) for more command information.

**Note:** Codespaces is much faster on the Desktop app. After the Codespace has booted, select the hamburger menu → Open in VS Code Desktop.

## Learning More

- [Docs](https://docs.evidence.dev/)
- [Github](https://github.com/evidence-dev/evidence)
- [Slack Community](https://join.slack.com/t/evidencedev/shared_invite/zt-uda6wp6a-hP6Qyz0LUOddwpXW5qG03Q)
- [Evidence Home Page](https://www.evidence.dev)

# e-Stat

https://www.e-stat.go.jp/

## 学校保健統計調査 平成２７年度以降 都道府県表

```
curl -sLo tmp.csv \
  "http://api.e-stat.go.jp/rest/3.0/app/getSimpleStatsData?appId=${appId}&lang=J&statsDataId=0003146482&metaGetFlg=Y&cntGetFlg=N&explanationGetFlg=Y&annotationGetFlg=Y&sectionHeaderFlg=1&replaceSpChars=0"
awk '/^"tab_code"/,0' tmp.csv > sources/height-and-weight.csv
```
