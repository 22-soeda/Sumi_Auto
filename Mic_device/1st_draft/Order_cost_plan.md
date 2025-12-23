<style>
   /* カラーパレットの定義 */
  :root {
    --primary-line-color: #8fbbe0; /* 見出しの線の色 */
    --border-color: #bbb;       /* 表や横線の色 */
    --heading-text-color: #111;    /* 見出しの文字色 */
    --body-text-color: #333;       /* 本文の文字色 */
    --table-header-bg: #f8f9fa;    /* 表のヘッダー背景 */
    --table-row-even-bg: #fcfcfc;  /* 表の縞々（偶数行） */
  }

  /* Google Fontsから Inter と Noto Sans JP を読み込む */
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700&family=Noto+Sans+JP:wght@400;700&display=swap');

  /* 全体の基本設定 */
  .markdown-preview, body {
    font-family: 'Inter', 'Noto Sans JP', sans-serif;
    color: var(--body-text-color); /* 本文は読みやすい濃いグレー */
    line-height: 1.8;
    -webkit-font-smoothing: antialiased;
  }

  /* 1. 見出しのデザイン調整 */
  h1, h2, h3 {
    font-family: 'Inter', 'Noto Sans JP', sans-serif;
    color: var(--heading-text-color);
    font-weight: 700; /* 2. 見出しを太字に */
  }

  h1 {
    /* 1. 細さ: 1px や 2px など */
    /* 2. 濃さ: 色を指定。薄くしたい場合は #ddd や #eee */
    border-bottom: 1px solid var(--border-color);
    padding-bottom: 10px; /* 文字と線の間の距離 */
    margin-bottom: 30px; /* 線と次の行（作成者など）との距離 */
  }

  h2 {
    /* 1. ラインの色を薄い青 (#8fbbe0) に変更 */
    border-bottom: 1px solid var(--primary-line-color);
    padding-left: 12px;
    border-left: 6px solid var(--primary-line-color);
    margin-top: 2em;
    padding-bottom: 4px;
  }

  /* 3. 表（Table）のデザイン調整 */
  table {
    display: table;
    width: 100%;
    border-collapse: collapse;
    margin: 25px 0;
    font-size: 0.95em;
  }

  table th {
    background-color: var(--table-header-bg); /* ヘッダーをさらに薄く */
    color: var(--heading-text-color);               /* ヘッダー内の文字を濃く */
    font-weight: 700;
    border: 1px solid var(--border-color); /* 1. 表のラインも少し薄く */
    padding: 12px;
  }

  table td {
    border: 1px solid var(--border-color); /* 1. 表のラインも少し薄く */
    padding: 12px;
  }

  /* 1行おきに非常に薄いグレーをつけて可読性を上げる */
  table tr:nth-child(even) {
    background-color: var(--table-row-even-bg);
  }

  /* 横線（---）のデザイン調整 */
  hr {
    border: none;                /* 標準の太い枠線を消す */
    border-top: 1px solid var(--border-color);  /* 1pxの非常に薄いグレーの線にする */
    margin: 30px 0;              /* 上下の余白を広げてスッキリさせる */
  }

   /* ページ区切り */
  .page-break {
  page-break-before: always;
}
</style>

# 御見積書

**作成者：東京科学大学 添田悠介**
**作成日：2025年12月24日**

## ウェアラブル会話記録デバイス PoC開発業務

本プロジェクトにおける費用内訳をご提案いたします。
本プランは、技術的な録音検証に加え、実使用を想定した最低限の保護（バッテリーケース）とデバイス2台分の部材費を含めた構成となっております。

---

## 1. 開発プラン概要

本PoC（概念実証）では、デバイスの基本機能である音声取得と無線によるデータ送信の実現可能性を検証することに主眼を置いています。開発の範囲および提供形態は以下の通りです。

| 項目 | 内容 |
| :--- | :--- |
| **想定用途** | 技術検証、初期PoC、実機2台による動作確認 |
| **筐体(ケース)** | バッテリー保護ケースのみ（基板部分は露出または簡易絶縁処理） |
| **ファームウェア** | 基本的な録音機能の実装、データの書き込み制御 |
| **検証テスト** | 机上でのデバッグ、基本動作チェック |
| **納品物** | 実機プロトタイプ、ソースコード、報告ドキュメント |

---

<div class="page-break"></div>

## 2. 費用内訳（税抜）

本業務の遂行にあたり、設計から部材調達、実装、検証までに要する費用を以下の通り算出いたしました。各工程の役割と金額の詳細は下表をご参照ください。

| No. | 工程項目 | 金額(円) | 内容詳細 |
| :--- | :--- | ---: | :--- |
| 1 | **要件定義、設計費** | 50,000 | 必要最小限の構成検討、部品調達 |
| 2 | **材料費** | 30,000 | デバイス2台分の部材一式（マイコン、バッテリー等） |
| 3 | **筐体製作費** | 63,000 | バッテリーケースの設計および3Dプリントによる作製 |
| 4 | **ファームウェア開発費** | 237,000 | 基本録音機能の実装、ファイルシステム書き込み制御、エラー処理 |
| 5 | **検証・品質テスト費** | 45,000 | 机上でのデバッグ、動作チェック |
| 6 | **プロジェクト管理、報告費** | 75,000 | 進行管理、報告ドキュメント作製 |
| | **合計 (税抜)** | **¥500,000** | |

---

## 3. 備考・諸条件

円滑なプロジェクト進行のため、以下の納期および対応範囲についてご確認をお願いいたします。

1. **納期の目安**
   ご発注より 約1.0ヶ月 を予定しております。
2. **スコープ外事項**
   小型化に向けた筐体の設計・製作、長時間のフィールドテスト、高度な省電力アルゴリズムの実装は本プランに含まれません。