# UiPath vs Automation Anywhere 比較資料

> 作成日: 2026年4月17日
> 観点: AI Agent / Agentic Process Automation 中心

## 🎯 概要比較

| 項目 | UiPath | Automation Anywhere |
|------|--------|---------------------|
| **AI Agent基盤** | Maestro / Goal Based Agents | Autopilot / AARI |
| **LLM統合** | AI Trust Layer | AI + RPA Platform |
| **オーケストレーション** | Orchestrator + Maestro | Control Room + CoE Manager |
| **ドキュメント処理** | Document Understanding | IQ Bot / Document Automation |
| **コーディングスタイル** | ビジュアル + コード（VB.NET/C#） | ビジュアル + Python |
| **クラウド対応** | Automation Cloud | Automation 360 Cloud |
| **価格モデル** | ライセンス + 従量課金 | サブスクリプション |

## 🤖 AI Agent / Agentic Process Automation

### UiPath
- **Maestro**: マルチエージェントオーケストレーション
- **Goal Based Agents**: 目標ベースの自律エージェント
- **AI Activities**: LLM呼び出し・プロンプト管理
- **Context Grounding**: RAG統合

### Automation Anywhere
- **Autopilot**: 自然言語でのプロセス自動化
- **AI Agent Studio**: カスタムエージェント構築
- **Enterprise Knowledge AI**: RAG/ナレッジベース統合
- **Co-Pilot**: チャットインターフェース型自動化

## 🔄 レコーダー技術比較

| 技術 | UiPath | Automation Anywhere |
|------|--------|---------------------|
| **AI/Gen AI Recorder** | Generative Recorder | Generative Recorder |
| **コンピュータビジョン** | Computer Vision | AISense |
| **UIオートメーション** | UIA / MSAA / COM | UIA / MSAA |
| **Web** | Chrome/Edge拡張 | Chrome/Edge拡張 + Anchor |
| **仮想環境** | Remote Runtime | VMWare対応 |

## 📊 移行考慮点（UiPath → Automation Anywhere）

### 互換性が高い領域
- ✅ Webオートメーション（基本操作）
- ✅ Excel/Office操作
- ✅ APIコール・REST連携
- ✅ データベース操作

### 要注意領域
- ⚠️ レコーダー技術の差異（AISense vs Computer Vision）
- ⚠️ VB.NET コードの Python への変換
- ⚠️ Orchestrator ↔ Control Room の設定差異
- ⚠️ 例外処理・リトライロジックの再設計

## 🚀 推奨移行アプローチ

1. **現状分析**: 既存UiPathボットのインベントリ作成
2. **複雑度評価**: シンプル/中程度/複雑に分類
3. **パイロット移行**: シンプルなボットから開始
4. **AI Agent化**: 移行と同時にAgentic Process Automationへ昇華
5. **段階的展開**: CoE主導でのロールアウト
