# 監査と認定

## MASVS 認定と認証マークに対する OWASP の見解

OWASP はベンダー中立の非営利組織であり、ベンダー、検証者、ソフトウェアの認定は行っていません。

そのような保証の表明、認証マーク、認定はいずれも OWASP によって公式に検査、登録、認定されたものではありません。組織は ASVS 認定を主張する第三者や認証マークについて、その信頼性を慎重に検討する必要があります。

ただし、OWASP の公式な認定であると主張しない限り、組織がこのような保証サービスを提供することを妨げるものではありません。

## モバイルアプリの認定に関するガイダンス

モバイルアプリの MASVS への準拠を検証するために推奨される方法は「オープンブック」レビューを実行することです。つまり、アプリの設計者や開発者、プロジェクト文書、ソースコード、役割ごとに少なくともひとつのユーザーアカウントへのアクセスを含むエンドポイントへの認証されたアクセスといった、主要リソースへのアクセス権限をテスト技術者に割り当てることです。

MASVS は（クライアント側の）モバイルアプリと、アプリとそのリモートエンドポイント間のネットワーク通信のセキュリティを対象とすることに注意することが重要です。また、ユーザー認証とセッション管理に関連するいくつかの基本的かつ一般的な要件も対象とします。アプリに関連付けられた（Webサービスなどの）リモートサービスに対して特定の要件は含まれていません。認証およびセッション管理に関連する限られた一般的要件に対して安全です。ただし、MASVS V1 ではリモートサービスを全体的な脅威モデルでカバーし、OWASP ASVS などの適切な標準に沿って検証する必要があることを明記しています。

認定機関は、（特に重要な構成要素が範囲外である場合）検証の範囲、合格したテストと不合格のテストを含む検証結果の要約、不合格のテストへの解決法の明確な指示をレポートに含める必要があります。詳細な調書、スクリーンショットやムービー、問題を確実かつ繰り返し利用するためのスクリプト、傍受したプロキシログなどのテストの電子記録、クリーンアップリストなどの関連メモを保持することは標準的な業界の慣行と考えられます。ツールを実行して不合格を報告するだけでは不十分です。認定レベルのすべての問題がテストされ、余すところなくテストされている十分な証跡を提供していません。係争の場合には、すべての検証要件が実際にテストされたことを実証するのに十分な証跡が必要となります。

### OWASP モバイルセキュリティテストガイド (MSTG) を使用する

OWASP MSTG はモバイルアプリのセキュリティをテストするためのマニュアルです。MASVS に記載されている要件を検証するための技術的プロセスを記述しています。MSTG には MASVS のそれぞれの要件に対応するテストケースのリストが含まれています。MASVS の要件は高レベルで汎用的ですが、MSTG はモバイル OS ごとに詳細な推奨案とテスト手順を提供しています。

### 自動セキュリティテストツールの役割

可能な限り効率を上げるためにソースコードスキャナやブラックボックステストツールの使用が奨励されています。ただし、自動ツールのみを使用して MASVS 検証を完了することはできません。モバイルアプリはさまざまであり、全体的なアーキテクチャ、ビジネスロジック、使用されている特定のテクノロジーやフレームワークの技術的な落とし穴を理解することはアプリのセキュリティを検証するために必須の要件であるためです。

## その他の用途

### 詳細なセキュリティアーキテクチャガイダンスとして

モバイルアプリケーションセキュリティ検証標準のより一般的な用途のひとつはセキュリティアーキテクトのためのリソースとするものです。二つの主要なセキュリティアーキテクチャフレームワーク SABSA と TOGAF にはモバイルアプリケーションセキュリティアーキテクチャのレビューを完了するために必要な多くの情報がありません。MASVS を使用すると、セキュリティアーキテクトがモバイルアプリに共通する問題のコントロールを強化できるようになり、ギャップを埋めることができます。

### 既製のセキュアコーディングチェックリストの代替として

多くの組織は MASVS を採用することにより利益を得ることができます。2つのレベルのいずれかを選択するか、MASVS をフォークし、それぞれのアプリケーションのリスクレベルに必要なものをドメイン固有の方法に変更します。このタイプのフォークはトレーサビリティが維持されている限りにおいて奨励されています。したがって、アプリが要件 4.1 を満たしていれば、標準の派生としてフォークされたコピーにおいても同様であることを意味します。

### セキュリティテスト手法の基礎として

優れたモバイルアプリのセキュリティテスト手法は MASVS に記載されているすべての要件をカバーする必要があります。OWASP モバイルセキュリティテストガイド (MSTG) では検証要件ごとにブラックボックスとホワイトボックスのテストケースについて説明しています。

### 自動単体テストと自動統合テストのガイドとして

MASVS はアーキテクチャ上の要件を除いて高度にテスト可能であるよう設計されています。MASVS の要件に基づいて自動化された単体、統合、受け入れテストは継続的な開発ライフサイクルに統合することができます。これにより開発者のセキュリティ意識が向上するだけでなく、結果としてアプリの全体的な品質が向上し、プレリリースのフェーズでのセキュリティテストの検証量が減少します。

### セキュア開発トレーニング用に

MASVS はセキュアなモバイルアプリの特性を定義するためにも使用できます。多くの「セキュアコーディング」コースは単にコーディングのヒントを少し示すだけの倫理的ハッキングコースにすぎません。これは開発者の助けにはなりません。代わりとして、セキュア開発コースは MASVS を使用できます。トップ 10 コードセキュリティ問題などよりも、MASVS に記載されているプロアクティブなコントロールに強く焦点を当てます。