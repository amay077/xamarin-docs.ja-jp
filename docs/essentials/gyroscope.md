---
title: 'Xamarin.Essentials: ジャイロスコープなどがあります'
description: Xamarin.Essentials のジャイロスコープ クラスを使用して、デバイスの 3 つのプライマリ軸の周りの回転角度を測定するデバイスのジャイロスコープ センサーを監視できます。
ms.assetid: DA4F968A-D988-41F5-8745-1BEE693660A1
author: jamesmontemagno
ms.author: jamont
ms.date: 05/04/2018
ms.openlocfilehash: 3c83b3a9d8a7801e531006f50f8db2e1ad23e48c
ms.sourcegitcommit: 632955f8cdb80712abd8dcc30e046cb9c435b922
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/10/2018
ms.locfileid: "37947216"
---
# <a name="xamarinessentials-gyroscope"></a>Xamarin.Essentials: ジャイロスコープなどがあります

![NuGet にプレリリースします。](~/media/shared/pre-release.png)

**ジャイロスコープ**クラスを使用して、デバイスの 3 つのプライマリ軸の周りの回転は、デバイスのジャイロスコープ センサーを監視できます。

## <a name="using-gyroscope"></a>ジャイロスコープを使用します。

クラスで Xamarin.Essentials への参照を追加します。

```csharp
using Xamarin.Essentials;
```

ジャイロスコープ機能が呼び出すことによって、`Start`と`Stop`ジャイロスコープへの変更をリッスンするメソッド。 加えた変更は通過して送信、`ReadingChanged`イベント。 使用例を次に示します。

```csharp

public class GyroscopeTest
{
    // Set speed delay for monitoring changes.
    SensorSpeed speed = SensorSpeed.Ui;

    public GyroscopeTest()
    {
        // Register for reading changes.
        Gyroscope.ReadingChanged += Gyroscope_ReadingChanged;
    }

    void Gyroscope_ReadingChanged(GyroscopeChangedEventArgs e)
    {
        var data = e.Reading;
        // Process Angular Velocity X, Y, and Z
        Console.WriteLine($"Reading: X: {data.AngularVelocity.X}, Y: {data.AngularVelocity.Y}, Z: {data.AngularVelocity.Z}");
    }

    public void ToggleGyroscope()
    {
        try
        {
            if (Gyroscope.IsMonitoring)
              Gyroscope.Stop();
            else
              Gyroscope.Start(speed);
        }
        catch (FeatureNotSupportedException fnsEx)
        {
            // Feature not supported on device
        }
        catch (Exception ex)
        {
            // Other error has occurred.
        }
    }
}
```

[!include[](~/essentials/includes/sensor-speed.md)]

## <a name="api"></a>API

- [ソース コードのジャイロスコープなどがあります。](https://github.com/xamarin/Essentials/tree/master/Xamarin.Essentials/Gyroscope)
- [ジャイロスコープ API ドキュメント](xref:Xamarin.Essentials.Gyroscope)
