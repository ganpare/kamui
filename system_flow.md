# 生成AI情報収集システムフロー

## 1. Input Layer (データ収集層)
```mermaid
graph TD
    A[中国AI情報収集] --> D[情報統合]
    B[日本AI情報収集] --> D
    C[米国AI情報収集] --> D
    
    subgraph "入力ソース"
        A
        B
        C
    end

    subgraph "データ収集仕様"
        E[".cn/.jp/.comドメイン"]
        F["500-700字/セクション"]
        G["信頼性の高い情報源指定"]
    end
```

## 2. Process Layer (処理層)
```mermaid
graph LR
    D[収集データ] --> H[横断的分析]
    D --> I[比較表作成]
    D --> J[動向総合分析]
    
    subgraph "処理パイプライン"
        H
        I
        J
    end

    subgraph "処理制御"
        K["dependency_wait制御"]
        L["最適AIモデル割当"]
        M["マルチリンガル処理"]
    end
```

## 3. Output Layer (出力層)
```mermaid
graph TD
    N[分析結果] --> O[Markdownレポート]
    N --> P[比較一覧表]
    N --> Q[Marpプレゼンテーション]
    
    subgraph "出力フォーマット"
        O
        P
        Q
    end

    subgraph "品質管理"
        R["文字数制限"]
        S["引用形式統一"]
        T["デザインテンプレート"]
    end
```

## 4. System Design (システム設計)
```mermaid
graph TB
    A[構造的設計層<br>structure.yaml] --> B1[エージェント層1]
    A --> B2[エージェント層2]
    A --> B3[エージェント層3]
    B1 --> C1[API層1]
    B2 --> C2[API層2]
    B3 --> C3[API層3]

    subgraph "第1層: 構造制御"
        A
        style A fill:#f9f,stroke:#333,stroke-width:4px
    end

    subgraph "第2層: エージェント"
        B1
        B2
        B3
    end

    subgraph "第3層: API実行"
        C1
        C2
        C3
    end
```

## システムの特徴

1. **データの一貫性**
   - 各国の情報を同一フォーマットで収集
   - 統一された文字数制限と構造
   - 標準化された引用形式

2. **処理の効率性**
   - 依存関係による処理順序の最適化
   - タスク特性に応じたAIモデルの選定
   - 並列処理可能な構造

3. **出力の品質管理**
   - 統一されたデザインテンプレート
   - マルチフォーマット（MD/表/スライド）
   - 段階的な情報の統合と可視化

