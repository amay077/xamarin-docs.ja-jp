---
title: Visual Studio 2017 での Xamarin のインストール
description: このドキュメントでは、Visual Studio 2017 で Xamarin をインストールする方法を説明します。 要件、インストール プロセス、インストールの確認について説明します。
ms.prod: xamarin
ms.assetid: E20D4463-368E-4B60-A059-F50DB8C5552D
author: asb3993
ms.author: amburns
ms.date: 09/29/2017
ms.openlocfilehash: 6c2fe10b9b29901dfbb6173df131d093fe726bff
ms.sourcegitcommit: 3f2737f8abf9b855edf060474aa222e973abda3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/28/2018
ms.locfileid: "37066953"
---
# <a name="installing-xamarin-in-visual-studio-2017"></a>Visual Studio 2017 での Xamarin のインストール

<a name="requirements" />

## <a name="requirements"></a>必要条件

Visual Studio 2017 で Xamarin をインストールするには、以下のものが必要です。

1. Windows 7 以上。

2. Visual Studio 2017 (Community、Professional、または Enterprise)。

3. Xamarin for Visual Studio。

Xamarin をインストールして使用するための前提条件の詳細については、「[System Requirements](~/cross-platform/get-started/requirements.md)」 (システム要件) を参照してください。

<a name="installation" />

## <a name="installation"></a>インストール

Xamarin は、新しい Visual Studio 2017 の一部としてインストールできます。
そのためには、次の手順を使用します。

1. [Visual Studio](https://visualstudio.microsoft.com/vs/) ページから、Visual Studio 2017 Community、Visual Studio Professional、または Visual Studio Enterprise をダウンロードします (ダウンロード リンクは下部にあります)。

2. ダウンロードしたパッケージをダブルクリックしてインストールを開始します。

3. インストール画面で **[.NET によるモバイル開発]** ワークロードを選択します。 

    [![ワークロード画面での [.NET によるモバイル開発] の選択](windows-images/01-mobile-dev-workload-sml.png)](windows-images/01-mobile-dev-workload.png#lightbox)

4. **[.NET によるモバイル開発]** が選択されている間に、右側の **[概要]** パネルを確認します。 ここで、インストールしないモバイル開発オプションの選択を解除することができます。 既定では、次のスクリーン ショットに示されているすべてのオプション (**Xamarin Workbooks**、**Xamarin Profiler**、**Xamarin Remoted Simulator**、**Android NDK**、**Android SDK**、**Java SE Development Kit**、**Google Android エミュレーター**、**F# サポート**、および **Intel HAXM**) がインストールされます。

    ![インストールする Xamarin オプションがリストされている [概要] パネル](windows-images/02-summary.png)

5. Visual Studio 2017 のインストールを開始する準備ができたら、右下にある **[インストール]** ボタンをクリックします。

    ![インストール ボタンの場所](windows-images/03-click-install.png)

   インストールする Visual Studio 2017 のエディションに応じて、インストール プロセスが完了するまでに長時間かかる場合があります。 進行状況バーを使用して、インストールを監視することができます。

    ![インストール中の進行状況バーの例を示すスクリーン ショット](windows-images/04-progress-bars.png)

6. Visual Studio 2017 のインストールが完了したら、**[起動]** ボタンをクリックして Visual Studio を起動します。

    ![[起動] ボタンの場所](windows-images/05-launch.png)

<a name="vs2017" />

### <a name="adding-xamarin-to-visual-studio-2017"></a>Visual Studio 2017 への Xamarin の追加

Visual Studio 2017 が既にインストールされている場合は、Visual Studio 2017 インストーラーを再実行し、ワークロードを変更することで、Xamarin を追加できます (詳細については、[Visual Studio の変更](https://docs.microsoft.com/visualstudio/install/modify-visual-studio)に関するページを参照してください)。 次に、前述の手順に従って、Xamarin をインストールします。

Visual Studio 2017 のダウンロードとインストールの詳細については、「[Visual Studio 2017 のインストール](https://docs.microsoft.com/visualstudio/install/install-visual-studio)」を参照してください。


### <a name="verifying-installation"></a>インストールの確認

Visual Studio 2017 で、**[ヘルプ]** メニューをクリックして、Xamarin がインストールされていることを確認できます。 Xamarin がインストールされている場合は、以下のスクリーン ショットのように、**Xamarin** のメニュー項目が表示されます。

![[ヘルプ] メニューに表示されている Xamarin のメニュー項目](windows-images/12-xamarin-menu-item.png)

以前のバージョンの Visual Studio を使用している場合は、**[ヘルプ]、[Microsoft Visual Studio のバージョン情報]** の順にクリックし、インストールされている製品のリストをスクロールして、Xamarin がインストールされているかどうかを確認できます。

![Visual Studio のインストールされている製品画面](windows-images/13-xamarin-is-installed.png)

バージョン情報を見つける方法の詳細については、「[Where can I find my version information and logs?](~/cross-platform/troubleshooting/questions/version-logs.md)」 (バージョン情報とログはどこにありますか?) を参照してください

<a name="nextsteps" />

## <a name="next-steps"></a>次の手順

Visual Studio 2017 に Xamarin をインストールすることで、アプリのコードの記述を開始できるようになりますが、シミュレーター、エミュレーター、デバイスにアプリを構築および展開するための追加のセットアップは必要ありません。 インストールを完了し、クロス プラットフォームのアプリの構築を開始するには、以下のガイドを参照してください。

### <a name="ios"></a>iOS

詳細については、「[Installing Xamarin.iOS on Windows](~/ios/get-started/installation/windows/index.md)」(Windows への Xamarin.iOS のインストール) ガイドを参照してください。 

1. [Visual Studio for Mac をインストールする](https://docs.microsoft.com/visualstudio/mac/installation)
2. [Mac ビルド ホストへの Visual Studio の接続](~/ios/get-started/installation/windows/connecting-to-mac/index.md)
3. [iOS 開発者のセットアップ](~/ios/get-started/installation/device-provisioning/index.md) - デバイスでアプリケーションを実行するために必要
5. [リモートの iOS シミュレーター](~/tools/ios-simulator.md)
6. [Xamarin.iOS for Visual Studio の概要](~/ios/get-started/installation/windows/introduction-to-xamarin-ios-for-visual-studio.md)

### <a name="android"></a>Android

詳細については、「[Installing Xamarin.Android on Windows](~/android/get-started/installation/windows.md)」(Windows への Xamarin.Android のインストール) ガイドを参照してください。

1. [Xamarin.Android の構成](~/android/get-started/installation/windows.md#configuration)
2. [Xamarin Android SDK Manager の使用](~/android/get-started/installation/android-sdk.md?ide=vs)
3. [Android SDK エミュレーター](~/android/get-started/installation/android-emulator/index.md)
4. [開発用のデバイスの設定](~/android/get-started/installation/set-up-device-for-development.md)
