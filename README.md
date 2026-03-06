# Portfolio
---

## 1. Web Applications (個人開発)

### 1.1. Calorie & Weight Tracker (高機能カロリー・体重管理アプリ)
🔗 **[> https://calorie-xi.vercel.app](#)** 
#### プロジェクトの背景と目的 (Motivation)
個人の健康管理において、「正確なカロリー収支の把握」と「継続的な記録」をサポートするためのアプリケーションです。
既存アプリの入力の手間や、トレーニング中のバックグラウンド操作における課題を解消するため、「PWAによるネイティブアプリに迫るUX」と「多言語対応の高度な食品データベース検索」を備えた実用性の高いツールとして開発しました。

#### 技術スタックと選定理由 (Architecture)
* **Frontend:** Next.js 16 (App Router), React 19, TypeScript
  * 選定理由: App Routerによる初期ロードの高速化と、TypeScriptによる型安全な開発を実現するため。
* **Backend:** Firebase (Firestore, Firebase Auth)
  * 選定理由: リアルタイムなデータ同期と、セキュアな認証基盤を迅速に構築するため。
* **UI/UX & Web APIs:** Tailwind CSS v4, Service Worker, Document PiP API, Web Audio API
  * 選定理由: PWA環境での最適化や、Web APIを活用したネイティブアプリと同等のバックグラウンド体験を提供するため。

#### 解決した技術的課題・アピールポイント (Value Proposition)
* **バックグラウンドでの確実な動作:** `Screen Wake Lock API` でスリープを防止し、`Document Picture-in-Picture API` や `Web Audio API` を駆使して、別タブ移動時や音楽再生中でもタイマーと通知が確実に機能するよう実装しました。
* **複数ソースの並列検索:** 独自DB、日本食品標準成分表、Open Food Facts、USDAの4つのデータベースをバックグラウンドで並列検索するアーキテクチャを構築し、高速かつ高精度な食品検索を実現しました。
* **PWAのiOS最適化:** iOS Safari特有のポップアップブロックやセーフエリアの表示崩れを検知・解消するロジックを独自に組み込みました。

---

### 1.2. Household Account Book (収支管理アプリ)
🔗 **[> https://household-account-book-swart.vercel.app](#)** 
#### プロジェクトの背景と目的 (Motivation)
単なる記録ツールではなく、「気づき」を与え資産形成をサポートする家計簿アプリケーションです。
クレジットカードの引き落とし日や銀行口座の必要額を自動計算して警告を出すなど、キャッシュフローの可視化による実践的な課題解決を図り、日々の家計管理を効率化します。

#### 技術スタックと選定理由 (Architecture)
* **Frontend:** Next.js 16 (App Router), React 19, TypeScript
  * 選定理由: 高速な初期表示とSEOフレンドリーな構成を実現し、堅牢なコードベースを維持するため。
* **Backend:** Firebase (Authentication, Firestore)
  * 選定理由: セキュアな認証とリアルタイムなデータ処理をサーバーレスで迅速に構築するため。
* **UI/UX & Tools:** Tailwind CSS v4, Recharts, date-fns
  * 選定理由: デバイスサイズに動的に最適化させつつ、スマートフォンでのスワイプナビゲーションなど優れた操作性と、高度なグラフ描画を提供するため。

#### 解決した技術的課題・アピールポイント (Value Proposition)
* **入力ストレスの最小化:** レシートのOCR自動解析（Next.js API Routes連携）、金額入力欄での電卓機能（例: `100+250`）、PC利用時のショートカットキーを実装し、あらゆるデバイスからのシームレスな入力を実現しました。
* **データ分析と予測機能:** 過去データからのAI支出予測機能や、現在のペースに基づく将来の資産推移シミュレーション機能を実装し、ユーザーの継続利用を促す付加価値を提供しています。
* **高度なUIコンポーネント:** Rechartsを用いた動的なグラフ描画や、大量データの効率的なレンダリングにより、パフォーマンスを維持しつつリッチな分析画面を構築しました。

---

## 2. Research / Academic Projects (研究活動)

### 2.1. グラフアルゴリズムの並列化と高速化研究 (Brandes Algorithm)
🔗 **[> https://github.com/m5291091/lab](#)**

#### プロジェクトの背景と目的 (Motivation)
ネットワーク分析において中心的な指標となる「媒介中心性 (Betweenness Centrality)」を算出するための Brandesアルゴリズム について、大規模グラフデータに対する計算コストの課題を解決するため、並列計算によるアプローチとパフォーマンスチューニングを行いました。

#### 技術スタックと選定理由 (Architecture)
* **Language:** C++
* **Parallel Computing:** CUDA (GPU), OpenMP (CPU)
  * 選定理由: ハードウェアの計算リソースを極限まで引き出し、計算集約型のアルゴリズムを最適化・高速化するため。
* **Build System:** CMake

#### アピールポイント (Value Proposition)
* **多様なアーキテクチャ向けの実装:** ベースとなる逐次処理 (`brandes_sequential`) に加え、OpenMPを用いたマルチコアCPUでのスレッド並列化 (`brandes_omp`)、およびCUDAを用いたGPUでの超並列化 (`brandes_gpu`) をそれぞれスクラッチから実装しました。
* **低レイヤー技術とコンピュータサイエンスの基礎力:** モダンなWeb開発の知識にとどまらず、メモリ管理やスレッド同期といった低レイヤーの制約を考慮しながら複雑なアルゴリズムを実装できる、エンジニアとしての確固たる基礎力を有しています。
