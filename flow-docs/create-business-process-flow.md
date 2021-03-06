---
title: PowerApps で業務プロセス フローを作成する | MicrosoftDocs
description: 業務プロセス フローを作成する方法について説明します
ms.custom: ''
ms.date: 08/17/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 (online)
- Dynamics 365 Version 9.x
- powerapps
ms.assetid: efe86ab3-430f-485a-b924-6ed82cfbb449
caps.latest.revision: 39
author: Mattp123
ms.author: matp
manager: kvivek
search.app:
- Flow
search.audienceType:
- flowmaker
- enduser
ms.openlocfilehash: 1e765d4c7c11354e382c3ff74ac66103345ff39f
ms.sourcegitcommit: a20fbed9941f0cd8b69dc579277a30da9c8bb31b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2018
ms.locfileid: "44691036"
---
# <a name="tutorial-create-a-business-process-flow-to-standardize-processes"></a>チュートリアル: プロセスを標準化する業務プロセス フローを作成する

このチュートリアルでは、PowerApps を使って業務プロセス フローを作成する方法を示します。 業務プロセス フローを使用する理由の詳細については、「[Business process flows overview](business-process-flows-overview.md)」 (業務プロセス フローの概要) を参照してください。 モバイル タスク フローの作成については、「[モバイル タスク フローを作成する](https://docs.microsoft.com/dynamics365/customer-engagement/customize/create-mobile-task-flow)」を参照してください。  
  
 ユーザーが業務プロセス フローを開始すると、フォーム上部にあるプロセス バーにプロセスのステージとステップが表示されます。  
  
 ![ステージを含む業務プロセス](media/business-process-stages.png "ステージを含む業務プロセス")  
  
 > [!TIP]
 >  業務プロセス フローの定義を作成したら、業務プロセス フローのインスタンスを作成、読み取り、更新、削除できるユーザーを制御できるようになります。 たとえば、サービス関連のプロセスの場合、顧客サービス担当者には、業務プロセス フローのインスタンスを変更するためのフルアクセスを提供できます。一方、営業担当者には、顧客の販売後活動を監視できるようにインスタンスへの読み取り専用アクセスを提供することができます。 作成する業務プロセス フローの定義に対してセキュリティを設定するには、操作バーの **[セキュリティ ロールの有効化]** を選択します。  
  
<a name="BKMK_Createbusinessprocessflows"></a>   
## <a name="create-a-business-process-flow"></a>業務プロセス フローを作成する  
  
1. [ソリューション エクスプローラー](/powerapps/maker/model-driven-apps/advanced-navigation#solution-explorer)を開きます。
  
2. 左のナビゲーション ウィンドウで、**[プロセス]** を選択します。 
  
3.  **[アクション]** ツールバーで、**[新規]** を選択します。  
  
4.  **[プロセスの作成]** ダイアログ ボックスで、必須フィールドに入力します。  
  
    -   プロセス名を入力します。 プロセスの名前は一意である必要はありませんが、プロセスを選択する必要があるユーザーにわかりやすいものにしてください。 これは後で変更できます。  
  
    -   **[カテゴリ]** リストで、**[業務プロセス フロー]** を選択します。  
  
         プロセスを作成した後でカテゴリを変更することはできません。  
  
    -   **[エンティティ]** リストで、プロセスのベースとなるエンティティを選択します。  
  
         選択したエンティティは、プロセス フローの最初のステージに追加できるステップで使用可能なフィールドに影響します。 目的のエンティティが見つからない場合は、エンティティのエンティティ定義に業務プロセス フロー (フィールドが作成される) オプション セットが存在することを確認します。 プロセスを保存した後でこれを変更することはできません。  
  
5. **[OK]** を選択します。  
  
     新しいプロセスが作成され、業務プロセス フロー デザイナーが開き、既に作成されている単一のステージが示されます。  
  
 ![主要な要素を示す業務プロセス フロー ウィンドウ](media/business-process-flow-window-showing-main-elements.png "主要な要素を示す業務プロセス フロー ウィンドウ")  
  
6. **ステージを追加します。** ユーザーがプロセス内のある業務ステージから別の業務ステージに進む場合は、次のようにします。  
  
    1.  **[コンポーネント]** タブから **[ステージ]** コンポーネントをドラッグし、デザイナーの [+] 記号にドロップします。  
  
        ![業務プロセス ステージをドラッグする](media/drag-business-process-stage.png "業務プロセス ステージをドラッグする")  
  
    2.  ステージに対してプロパティを設定するには、ステージを選択してから、画面の右側にある **[プロパティ]** タブでプロパティを設定します。  
  
        -   表示名を入力します。  
  
        -   必要に応じて、ステージのカテゴリを選択します。  プロセス バーに、シェブロンとしてカテゴリ (**[見込みありと評価]** や **[提案作成]** など) が表示されます。  
  
            ![業務プロセス バーのシェブロン](media/business-process-bar-chevron.png "業務プロセス バーのシェブロン")  
  
        -   プロパティの変更が完了したら、**[適用]** ボタンを選択します。  
  
7. **ステージにステップを追加します。** ステージのステップを表示するには、ステージの右上隅にある **[詳細]** を選択します。 ステップをさらに追加するには、次のようにします。  
  
    1.  **[コンポーネント]** タブからステージに **[ステップ]** コンポーネントをドラッグします。  
  
        ![業務プロセス内のステージにステップを追加する](media/add-step-stage-business-process.png "業務プロセス内のステージにステップを追加する")  
  
    2.  ステップを選択してから、**[プロパティ]** タブでプロパティを設定します。  
  
        1.  ステップの表示名を入力します。  
  
        2.  ユーザーがステップを完了するためにデータを入力するようにする場合は、ドロップダウン リストから適切なフィールドを選択します。  
  
        3.  ユーザーがプロセスの次のステージに移動する前にフィールドに入力してステップを完了する必要がある場合は、**[必須]** を選択します。  
  
        4.  完了したら、**[適用]** を選択します。  
  
8. **プロセスに分岐 (条件) を追加します。** 分岐条件を追加するには、次のようにします。  
  
    1.  **[コンポーネント]** タブから **[条件]** コンポーネントを、2 つのステージの間にある [+] 記号にドラッグします。  
  
        ![業務プロセス フローに条件を追加する](media/add-condition-business-process-flow.png "業務プロセス フローに条件を追加する")  
  
    2.  条件を選択し、**[プロパティ]** タブでプロパティを設定します。分岐プロパティの詳細については、[分岐を使用する業務プロセス フローの強化](enhance-business-process-flows-branching.md)に関するページを参照してください。 条件に対するプロパティの設定が完了したら、**[適用]**  を選択します。  
  
9. **ワークフローを追加します。** ワークフローを呼び出すには、次のようにします。  
  
    1.  **[コンポーネント]** タブから **[ワークフロー]** コンポーネントをステージ、またはデザイナーの**グローバル ワークフロー** アイテムにドラッグします。   どちらに追加するかは、以下の条件に応じて異なります。  
  
       - ステージの開始時または終了時にワークフローをトリガーする場合は、**ステージにドラッグします**。 ワークフロー コンポーネントは、ステージと同じ主エンティティに基づいている必要があります。  
  
       - プロセスがアクティブ化されたとき、またはアーカイブされたとき (状態が **[完了]** または **[破棄済み]** に変わったとき) にワークフローをトリガーする場合は、**グローバル ワークフロー アイテムにドラッグします**。 ワークフロー コンポーネントは、プロセスと同じ主エンティティに基づいている必要があります。  
  
    2.  ワークフローを選択し、**[プロパティ]** タブでプロパティを設定します。  
  
       1.  表示名を入力します。  
  
       2.  ワークフローがトリガーされるタイミングを選択します。  
  
       3.  ステージ エンティティと一致する既存のオンデマンド アクティブ ワークフローを検索するか、**[新規]** を選択して新しいワークフローを作成します。  
  
       4.  完了したら、**[適用]** を選択します。  
  
       ワークフローの詳細については、[ワークフロー プロセス](../common-data-service/workflow-processes.md)に関するページを参照してください。  
  
10. 業務プロセス フローを検証するには、操作バーの **[検証]** を選択します  
  
11. 作業を続けながら、下書きとしてプロセスを保存するには、操作バーの **[保存]** を選択します。  
  
    > [!IMPORTANT]
    >  プロセスが下書きである限り、ユーザーは使用できません。  
  
12. プロセスをアクティブ化して、所属チームで使用できるようにするには、操作バーの **[アクティブ化]** を選択します。  

13. 業務プロセス フローのインスタンスを作成、読み取り、更新、または削除できるユーザーを制御できるようにするには、デザイナーのコマンド バーで **[セキュリティ ロールの編集]** を選択します。 たとえば、サービス関連のプロセスの場合、顧客サービス担当者には、業務プロセス フローのインスタンスを変更するためのフルアクセスを提供できます。一方、営業担当者には、顧客の販売後活動を監視できるようにインスタンスへの読み取り専用アクセスを提供することができます。

  **[セキュリティ ロール]** 画面で、ロールの名前を選択してセキュリティ ロールの情報ページを開きます。 [業務プロセス フロー] タブを選択し、セキュリティ ロールの業務プロセス フローに適切な特権を割り当てます。

  > [!NOTE]
  > システム管理者とシステム カスタマイザーのセキュリティ ロールでは、既定で新しい業務プロセス フローにアクセスできます。

   ![業務プロセス フローに特権を割り当てる](media/bpf-assign-privileges.png)

  適切なラジオ ボタンを選択して特権を指定し、[保存] をクリックします。 特権の詳細については、[業務プロセス フローの特権](business-process-flows-overview.md#BKMK_MultipleBPF)に関する記述を参照してください。

  その後、必ず、所属組織内の適切なユーザーにセキュリティ ロールを割り当ててください。

> [!TIP] 
>  デザイナー ウィンドウでタスク フローを操作するときに覚えておくと役に立つヒントをいくつか以下に示します。  
>   
> - 業務プロセス フロー ウィンドウにあるすべてのスナップショットを作成するには、操作バーの **[スナップショット]** を選択します。 これは、チーム メンバーからのプロセスに関するコメントを共有して取得する場合などに便利です。  
> - プロセスのさまざまな部分にすばやく移動するには、ミニマップを使用します。 これは、画面に収まりきらない複雑なプロセスがある場合に便利です。  
> - 業務プロセスの説明を追加するには、業務プロセス フロー ウィンドウの左隅のプロセス名の下にある **[詳細]** を選択します。 最大 2,000 文字を使用することができます。  
  
<a name="BKMK_Editbusinessprocessflows"></a>   
## <a name="edit-a-business-process-flow"></a>業務プロセス フローを編集する  
 業務プロセス フローを編集するには、ソリューション エクスプローラーを開き、**[プロセス]** を選択します。次に、編集するプロセスのリストから **[業務プロセス フロー]** を選択します。  
  
 プロセスのリストから編集する業務プロセス フローの名前を選択すると、それがデザイナーで開きます。そこで必要なすべての更新を行うことができます。 プロセスの名前の下にある **[詳細]** を展開し、その名前を変更するか、説明を追加して、追加情報を表示します。  
  
 ![業務プロセス フローの展開された [詳細] セクション](media/business-process-flow-details.png "業務プロセス フローの展開された [詳細] セクション")  
  
  
## <a name="other-things-to-know-about-business-process-flows"></a>業務プロセス フローについて知っておく必要があるその他の内容
 **ステージの編集**  
業務プロセス フローには最大 30 個のステージを含めることができます。    
  
ステージの次のプロパティを追加または変更できます。  
  
- **ステージ名**  
  
- **エンティティ** 最初の 1 つを除くすべてのステージのエンティティを変更できます。  
  
- **ステージ カテゴリ** カテゴリを使用して、ステージをアクションの種類でグループ化することができます。 これは、所属するステージごとにレコードをグループ化するレポートの場合に便利です。 ステージ カテゴリのオプションは、[ステージ カテゴリ] グローバル オプション セットから取得されます。 このグローバル オプション セットにさらにオプションを追加し、必要に応じて、既存のオプションのラベルを変更することができます。 必要に応じて、それらのオプションを削除することもできますが、既存のオプションはそのままにしておくことをお勧めします。 オプションを削除した場合、それとまったく同じものを追加して戻すことはできません。 それらを使用しないようにする場合は、ラベルを "使用しない" に変更します。  
  
- **関連付け**。 プロセスの前のステージが異なるエンティティに基づいている場合は、関連付けを入力します。 現在定義されているステージについては、**[関連付けの選択]** を選び、2 つのステージ間を移動するときに使用する関連付けを特定します。 次の利点を得るため、関連付けを選択することをお勧めします。  
  
    -   関連付けには、多くの場合、レコード間でデータを自動的に引き継ぎ、データ入力を最小限にする属性マップが定義されています。  
  
    -   レコードのプロセスのバーで **[次のステージ]** を選択すると、関連付けを使用するすべてのレコードがプロセス フローにリストされます。これにより、プロセス内のレコードの再利用が促されます。 さらに、ワークフローを使用してレコードの作成を自動化できます。これにより、ユーザーはレコードを作成するのではなく、選択するだけでプロセスをさらに簡素化できます。  
  
**ステップの編集**  
 各ステージには最大 30 個のステップを含めることができます。    
  
**分岐の追加**  
ステージへの分岐の追加については、[分岐を使用する業務プロセス フローの強化](enhance-business-process-flows-branching.md)に関するページを参照してください。  
  
ユーザーが業務プロセス フローを使用できるようにするには、プロセス フローを並べ替え、セキュリティ ロールを有効にして、アクティブ化する必要があります。  
  
**プロセス フロー順序の設定**  
 あるエンティティ (レコードの種類) に対して業務プロセス フローが複数ある場合は、新しいレコードに自動的に割り当てられるプロセスを設定する必要があります。 コマンド バーで、**[プロセス フローの順序]** を選択します。 新しいレコード、またはプロセス フローがまだ関連付けられていないレコードの場合、ユーザーがアクセスできる最初の業務プロセス フローが使用されます。  
  
**セキュリティ ロールの有効化**  
ユーザーは、自分に割り当てられているセキュリティ ロールの業務プロセス フローで定義されている特権に応じて、業務プロセス フローへのアクセスが許可されます。 

既定では、**システム管理者**と**システム カスタマイザー**のセキュリティ ロールでのみ、新しい業務プロセス フローを表示できます。 

業務プロセス フローに特権を指定するには、編集する業務プロセス フローを開き、業務プロセス フロー デザイナーのコマンド バーで **[セキュリティ ロールの編集]** を選択します。 このトピックの前半でリストされている「[業務プロセス フローを作成する](#create-a-business-process-flow)」の手順 13 を参照してください。
  
**アクティブ化**  
すべてのユーザーが業務プロセス フローを使用できるようにするには、アクティブ化する必要があります。 コマンド バーで、**[アクティブ化]** を選択します。 アクティブ化を確認したら、業務プロセス フローを使用できます。 業務プロセス フローでエラーが発生した場合、エラーが修正されるまでアクティブ化できません。  

## <a name="add-an-on-demand-action-to-a-business-process-flow"></a>業務プロセス フローにオンデマンド アクションを追加する
Dynamics 365 (オンライン) バージョン 9.0 の更新プログラムでは、業務プロセス フローの機能である、アクション ステップでの業務プロセス フローの自動化が導入されています。 アクションまたはワークフローをトリガーする業務プロセス フローにボタンを追加できます。

### <a name="add-on-demand-workflows-or-actions-using-an-action-step"></a>アクション ステップを使用してオンデマンドのワークフローまたはアクションを追加する
たとえば、営業案件の見込み評価プロセスの一部として、Contoso 組織で、すべての営業案件を指定されたレビュー担当者がレビューする必要があるとします。 その後、Contoso 組織では次のことを行うアクションが作成されました。 

- 営業案件のレビュー担当者に割り当てられているタスク レコードを作成する。 
- 営業案件のトピックに "レビュー準備完了" を加える。 

さらに、Contoso では、これらのアクションをオンデマンドで実行できる必要があります。 営業案件の見込み評価プロセスにこれらのタスクを統合するには、アクションが営業案件の業務プロセス フローに表示される必要があります。 この機能を有効にするには、**[業務プロセス フローのアクション ステップとして実行]** を選択します。
![業務プロセス フローとして実行可能](media/action-available-to-run.png)

次に、アクション ステップが Contoso の営業案件の業務プロセス フローに追加されます。 その後、プロセス フローが検証され、更新されます。

![営業案件の業務プロセス フローに追加されたアクション。](media/add-action-to-bpf.png)

これで、Contoso の販売員のメンバーは、**[実行]** を選択することにより、オンデマンドで**営業案件の見込み評価**業務プロセス ステップからアクションを開始することができます。

![アクションを実行します。](media/action-execute.png)

> [!IMPORTANT]
> - アクションまたはワークフローをオンデマンドで実行できるようにするには、業務プロセス フローにアクション ステップが含まれている必要があります。 アクション ステップでワークフローを実行する場合、オンデマンドで実行するようにワークフローを構成する必要があります。
> - アクションまたはワークフローに関連付けられたエンティティは、業務プロセス フローに関連付けられたエンティティと同じである必要があります。

### <a name="limitation-of-using-action-steps-in-a-business-process-flow"></a>業務プロセス フロー内のアクション ステップの使用上の制限

- 入力パラメーターまたは出力パラメーターが Entity、EntityCollection、または OptionSet (Picklist) という種類である場合、アクションをアクション ステップとして使用することはできません 複数の EntityReference 出力パラメーターまたは任意の数の EntityReference 入力パラメーターがあるアクションは、アクション ステップとして使用することはできません。 主エンティティ (グローバル アクション) に関連付けられていないアクションは、アクション ステップとして使用することはできません。

  
## <a name="next-steps"></a>次のステップ  
 [業務プロセス フローの概要](business-process-flows-overview.md) </br>   
 [分岐を使用して業務プロセス フローを強化する](enhance-business-process-flows-branching.md)

