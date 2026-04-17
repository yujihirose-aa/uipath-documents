# UiPath レコーダー技術詳細

> 作成日: 2026年4月17日

## 概要

UiPathのレコーダー技術は複数の認識エンジンを組み合わせて動作します。

## 1. Generative Recorder（生成AI レコーダー）

### 概要
- 自然言語の指示からオートメーションを生成
- GPT/LLMを活用したUI要素の意味的理解
- スクリーンショットベースの要素認識

### 特徴
- コーディング不要でのオートメーション作成
- 画面変更への高い耐性
- 多言語UI対応

## 2. Computer Vision（コンピュータビジョン）

### 概要
- AI/MLベースの画像認識
- 仮想環境・Citrix環境での動作
- ピクセルベースの要素識別

### 適用場面
- Citrix/RDP環境
- レガシーアプリケーション
- 標準的なセレクターが使えない場合

## 3. UIA（UI Automation）

### 概要
- Microsoft UI Automation フレームワーク
- Windowsネイティブアプリ対応
- アクセシビリティツリーを使用

### 特徴
- 高い信頼性・安定性
- WPF/WinForms/Win32対応
- プロパティベースの要素識別

## 4. MSAA（Microsoft Active Accessibility）

### 概要
- 旧来のWindowsアクセシビリティAPI
- レガシーアプリケーション対応
- UIAが使えない場合のフォールバック

## 5. Web レコーダー

### 対応ブラウザ
- Google Chrome（拡張機能）
- Microsoft Edge（拡張機能）
- Firefox（拡張機能）

### 認識方式
- CSSセレクター
- XPath
- アンカーベース（相対的位置）

## 6. SAP レコーダー

### 概要
- SAP GUI専用レコーダー
- SAP Scripting API活用
- 高い安定性・パフォーマンス

## 技術選択ガイドライン

| アプリケーション種別 | 推奨技術 |
|---------------------|---------|
| Webアプリ | Web Recorder（CSS/XPath） |
| Windowsネイティブ | UIA |
| レガシーWindows | MSAA |
| Citrix/仮想環境 | Computer Vision |
| SAP | SAP Recorder |
| 不明・複雑 | Generative Recorder |
