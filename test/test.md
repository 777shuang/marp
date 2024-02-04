---
marp: true
paginate: true
math: katex
theme: academic
---

# 動作概念図

@startuml
    Keydriver ->> POI: Excelファイル読み込み
    POI ->> Excel: 読み込み
    Excel ->> POI: ワークシート
    POI ->> Keydriver: ワークシート
    Keydriver ->> WebDriver: ブラウザ操作
    WebDriver ->> ブラウザ: ブラウザ操作
    ブラウザ ->> WebDriver: ブラウズ結果
    WebDriver ->> Keydriver: ブラウズ結果
    Keydriver ->> Keydriver: 結果検証
    Keydriver ->> POI: テスト結果出力
    POI ->> Excel: テスト結果出力
@enduml
