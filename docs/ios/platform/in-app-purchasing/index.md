---
title: アプリ内購入 Xamarin.iOS で
description: このドキュメントでは、デジタルの製品や StoreKit Api を使用してサービスを販売する方法について説明します。 構成、使用できる製品、以外が使用できる製品、トランザクション、サブスクリプション、および詳細を説明するガイドにリンクします。
ms.prod: xamarin
ms.assetid: B41929D8-47E4-466D-1F09-6CC3C09C83B2
ms.technology: xamarin-ios
author: bradumbaugh
ms.author: brumbaug
ms.openlocfilehash: 8a41ed44a331c91a333b95c1d62136244a6945dd
ms.sourcegitcommit: ea1dc12a3c2d7322f234997daacbfdb6ad542507
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/05/2018
ms.locfileid: "34787342"
---
# <a name="in-app-purchasing-in-xamarinios"></a>アプリ内購入 Xamarin.iOS で

iOS アプリケーションは、デジタルの製品または StoreKit – Apple id です。 それらを使用してユーザーの金融取引を実行するためには、Apple のサーバーと通信する iOS によって提供される Api のセットを使用してサービスを販売できます。 StoreKit Api は製品情報の取得、トランザクションを実行すると、主に懸念 – ユーザー インターフェイス コンポーネントがありません。 アプリ内購入を実装するアプリケーションは必要があります、独自のユーザー インターフェイスをビルドしてをユーザーに必要な製品やサービスを提供するカスタム コードで購入した項目を追跡します。

アプリ内購入機能を提供するには、いくつかの手順が必要です。

-  **アプリを構成する**– アプリケーションのプロビジョニング プロファイルでは、セットアップを正しくする必要があります。
-  **製品を作成する**– iTunes Connect ポータルでは、製品の説明と価格を作成する必要があります。
-  **StoreKit を実装する**– 販売されている製品の種類に従って StoreKit API を実装する必要があります。
-  **ユーザー インターフェイスおよび製品自体の構築**– を各注文書を追跡およびバックアップ/復元する場合は、適切なメカニズムを含む、製品を実装する必要があります。
-  **Sales を監視および資金の受信**– iTunes Connect によって提供される情報を使用して売上傾向を監視し、収入を追跡します。

このドキュメントでは、アプリ内購入 Xamarin.iOS を使用して提供するこれらすべての手順を完了する方法について説明します。

## <a name="requirements"></a>必要条件

アプリ内購入をサポートするために以降 Xcode 7 では、Xamarin.iOS 5.0 以降を使用する必要があります。

## <a name="contents"></a>目次

 * [アプリ内購入の基本と構成](~/ios/platform/in-app-purchasing/in-app-purchase-basics-and-configuration.md)

 * [StoreKit 概要および製品情報を取得中](~/ios/platform/in-app-purchasing/store-kit-overview-and-retreiving-product-information.md)

 * [コンシューマブル製品の購入](~/ios/platform/in-app-purchasing/purchasing-consumable-products.md)

 * [非コンシューマブル製品の購入](~/ios/platform/in-app-purchasing/purchasing-non-consumable-products.md)

 * [トランザクションと検証](~/ios/platform/in-app-purchasing/transactions-and-verification.md)

 * [サブスクリプションとレポート](~/ios/platform/in-app-purchasing/subscriptions-and-reporting.md)

## <a name="summary"></a>まとめ

この記事の内容がアプリ内購入の概念が導入されましたに活用するためにアプリケーションを構成する方法を説明した、Xamarin.iOS の使用例を表示します。 これがについて説明します。

-  **iOS プロビジョニング ポータル**– アプリで有効にするためのガイドラインが機能を購入します。
-  **iTunes Connect** – アプリを販売する製品を構成します。
-  **キットを格納**– アプリ内購入機能を構築するために使用するクラスの説明。
-  **アプリを購入するためのコーディング**– Xamarin.iOS アプリにアプリ内購入を構築する方法の例を示します。
-  **Reporting** – iTunes Connect 経由で入手できる統計の概要について説明します。


## <a name="related-links"></a>関連リンク

- [InAppPurchaseSample](https://developer.xamarin.com/samples/StoreKit/)
- [アプリ購入プログラミング ガイド](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/StoreKitGuide/Introduction.html)
- [iTunes Connect 開発者ガイド](https://developer.apple.com/library/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/iTunesConnect_Guide.pdf)
- [キット フレームワーク参照を保存します。](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/StoreKit_Collection/StoreKit_Collection.pdf)
- [Q & A に製品の Id をアプリ内購入](https://developer.apple.com/library/ios/#qa/qa1329/_index.html)
- [テクニカル ノートのアプリ内購入](https://developer.apple.com/library/ios/#technotes/tn2259/_index.html)
- [最初のアプリ ストアに提出](https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/Introduction/Introduction.html)
- [アプリ ストア リソース センター](https://developer.apple.com/appstore/index.html)
- [App Store への提出に関するヒント](https://developer.apple.com/appstore/resources/submission/tips.html)
- [App Store の審査に関するガイドライン](https://developer.apple.com/appstore/resources/approval/guidelines.html)
- [アプリを管理します。](https://developer.apple.com/appstore/resources/managing/index.html)
