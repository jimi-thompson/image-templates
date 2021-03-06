---

copyright:
  years: 2014, 2018
lastupdated: "2018-10-30"

keywords:

subcollection: image-templates

---


{:new_window: target="_blank"}
{:tip: .tip}
{:faq: data-hd-content-type='faq'}

# FAQ: イメージ・テンプレート
{: #faq-image-templates}

## 標準イメージ・テンプレートとは何ですか?
{: faq}

標準イメージ・テンプレートは、{{site.data.keyword.BluSoftlayer_notm}} の{{site.data.keyword.virtualmachineslong}}のイメージ作成方法の 1 つです。
標準イメージ・テンプレートでは、オペレーティング・システムに関係なく、既存の仮想サーバーのイメージを取り込み、そのイメージに基づいて新しい仮想サーバーを作成することができます。

## ISO テンプレートとは何ですか?
{: faq}

ISO テンプレートは、特に ISO 用に予約されているタイプのテンプレートであり、VSI のブートに使用できます。 ISO テンプレートには、パブリックとプライベートという 2 つのバージョンがあります。 パブリック ISO テンプレートは、{{site.data.keyword.BluSoftlayer_notm}} によって提供されている事前構成済みテンプレートで、どのお客様も使用できます。 プライベート ISO テンプレートは、{{site.data.keyword.objectstorageshort}}・アカウントに保管されている ISO のイメージをインポートして作成されます。 「イメージ・テンプレート」画面に ISO をインポートするためには、ISO がブート可能でなければなりません。

ISO テンプレートを VSI にロードするために使用できるのは、{{site.data.keyword.BluSoftlayer_notm}} がサポートするオペレーティング・システムだけです。 詳細情報については、[Supported Operating Systems ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://www.softlayer.com/services/software/) を参照してください。
{:tip}

## パブリック・イメージとプライベート・イメージとの違いは?
{: faq}

パブリック・イメージは、どの {{site.data.keyword.BluSoftlayer_notm}} ユーザーも表示し、新しい仮想サーバーに適用できるイメージです。 {{site.data.keyword.BluSoftlayer_notm}} は、現在、さまざまなデバイスの構成オプションのためにパブリック・イメージをソリューションとして作成しています。 お客様もイメージを公開し、どのユーザーも使用できるようにすることができます。 プライベート・イメージは、許可ユーザーのみが表示できるイメージです。 デフォルトでは、お客様のアカウントのすべてのユーザーが許可ユーザーになりますが、{{site.data.keyword.slportal}} で共有オプションを更新することにより、複数のアカウントでイメージを共有することもできます。

## 自己管理型ハイパーバイザーを使用して、仮想サーバーを取り込んでデプロイすることはできますか?
{: faq}

取り込んでデプロイできるのは、{{site.data.keyword.BluSoftlayer_notm}} によってプロビジョンされているサーバーのみになります。 個人のデバイス上に手動で作成された個別の仮想サーバーを取り込んだり、プロビジョンしたり、デプロイしたりすることはできません。

## プライベート ISO テンプレートを他のお客様と共有できますか?
{: faq}

すべてのお客様に公開される ISO テンプレートは、{{site.data.keyword.BluSoftlayer_notm}} によって生成されるテンプレートだけです。 プライベート ISO テンプレートはアカウント固有であり、{{site.data.keyword.slportal}}を介してお客様間で共有することはできません。

## イメージからのブートを実行するには、ISO テンプレートを仮想サーバーと同じデータ・センターに配置する必要がありますか?
{: faq}

はい。イメージからブートするためには、ISO テンプレートを仮想サーバーと同じデータ・センターに配置する必要があります。 同じデータ・センターにない場合は、操作を実行するために、ISO テンプレートを適切なデータ・センターにコピーしなければなりません。 この状況が発生すると、そのトランザクションに関する警告が表示されます。 ISO テンプレートを別のデータ・センターにコピーする場合、他のタイプのイメージ・テンプレートのコピーに料金が適用されるのと同じ方法で少額の料金がアカウントに課金されます。

## 物理データとボリュームのサイズの違いとは?
{: faq}

ボリュームはファイルの保管に使用できるディスク・スペースであり、物理データはディスクに保管されている実際のファイルで構成されます。

## イメージのインポート/エクスポート機能とは?
{: faq}

{{site.data.keyword.slportal}}の「イメージ・テンプレート」ページにあるイメージのインポート/エクスポート機能により、{{site.data.keyword.objectstorageshort}}・アカウントに保管されている VHD と ISO をイメージ・テンプレートに変換したり、その逆に変換したりすることができます。 イメージをインポートするとき、指定された [{{site.data.keyword.objectstorageshort}}] アカウントのコンテナーから特定のファイル (VHD または ISO) が取得され、イメージ・テンプレートに変換されます。 そして、そのイメージ・テンプレートをデバイスのブートまたはロードに使用できます。 イメージをエクスポートすると、イメージ・テンプレートが 1 つのファイル (テンプレートに複数のディスクがある場合は複数のファイル) に変換され、そのファイルが {{site.data.keyword.objectstorageshort}}・アカウントのコンテナー上の指定された場所に保管されます。

## 1 次ドライブだけでなくサーバー全体のイメージ・テンプレートを作成するには、どうしたらよいですか?
{: faq}

サーバー全体のイメージ・テンプレートを作成するには、[イメージ・テンプレートの作成](/docs/infrastructure/image-templates?topic=image-templates-creating-an-image-template)の手順を参照してください。

イメージ・テンプレートを IBM Cloud オブジェクト・ストレージにエクスポートした場合は、各ブロック・デバイス (またはディスク) に独自のファイルが関連付けられます。 例えば、イメージ・ファイルの名前が image.vhd の場合、1 つ目のブロック・デバイスは image-0.vhd としてエクスポートされます。 2 つ目のブロック・デバイスは image-1.vhd としてエクスポートされる、というように続きます。
{: tip}
