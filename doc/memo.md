# Memo

## Links

- [VSCode API](https://code.visualstudio.com/api/references/vscode-api)
- 参考
  - https://qiita.com/HelloRusk/items/073b58c1605de224e67e

## 逆引き

- ステータスバーにボタン追加

```typescript
const button = vscode.window.createStatusBarItem(
  vscode.StatusBarAlignment.Right,
  0
);
button.command = 'vscode-omikuji.omikuji';
button.text = 'おみくじを引く';
context.subscriptions.push(button);
button.show();
```

- 文字列を入力する

```typescript
vscode.commands.registerCommand('vscode.hello', async () => {
  const name = await vscode.window.showInputBox({
    title: 'あなたの名前は？',
  });
  if (name !== undefined) {
    vscode.window.showInformationMessage(`${name}です！`);
  }
});
```

- プレビューする

```typescript
const panel = vscode.window.createWebviewPanel();
```

## Commands

```sh
# パッケージ化
npx vsce package
```
