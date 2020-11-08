---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054742"
---
# Start-AzureStorSimpleDeviceFailoverJob

## STRESZCZENIe
Inicjuje operację przejęcia awaryjnego grup kontenerów woluminów.

## POLECENIA

### Empty (domyślnie)
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Start-AzureStorSimpleDeviceFailoverJob** inicjuje działanie trybu failover jednej lub większej liczby grup kontenerów woluminów z jednego urządzenia na inny.

## Przykłady

### Przykład 1. Uruchom zadanie przejęcia awaryjnego dla nazwanego urządzenia i nazwanego urządzenia docelowego.
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

To polecenie pobiera kontenery woluminów trybu failover dla urządzenia o nazwie ChewD_App7 przy użyciu polecenia cmdlet **Get-AzureStorSimpleFailoverVolumeContainers** .
Polecenie przekazuje wyniki do polecenia cmdlet **WHERE-Object** , które powoduje porzucanie tych kontenerów, które mają wartość inną niż $true dla właściwości **IsDCGroupEligibleForDR** .
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Where-Object` .
Bieżące polecenie cmdlet uruchamia zadania trybu failover dla pozostałych kontenerów woluminu pracy awaryjnej.
Polecenie określa nazwę urządzenia i nazwę urządzenia docelowego.
Polecenie zwraca identyfikator wystąpienia zadania uruchamiającego polecenie cmdlet.

### Przykład 2: uruchamianie zadania trybu failover dla urządzenia i urządzenia docelowego określonego przez identyfikator
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

To polecenie uzyskuje kontenery woluminów trybu failover dla urządzenia o nazwie ChewD_App7 przy użyciu polecenia **Get-AzureStorSimpleFailoverVolumeContainers**.
Polecenie przekazuje wyniki do **obiektu WHERE-Object** , który porzuca te osoby, które mają wartość inną niż $true dla właściwości **IsDCGroupEligibleForDR** .
Polecenie cmdlet przekazuje wyniki do polecenia cmdlet **Select-Object** , które wybiera pierwszy obiekt, który ma zostać przekazany do bieżącego polecenia cmdlet.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Select-Object` .
Bieżące polecenie cmdlet rozpoczyna zadania trybu failover dla wybranego kontenera woluminu trybu failover.
Polecenie określa identyfikator urządzenia i identyfikator urządzenia docelowego.
Polecenie zwraca identyfikator wystąpienia zadania uruchamiającego polecenie cmdlet.

## PARAMETRÓW

### -DeviceId
Określa identyfikator wystąpienia urządzenia StorSimple, na którym znajdują się grupy kontenerów woluminów.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Określa nazwę urządzenia StorSimple, na którym znajdują się grupy kontenerów woluminów.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDeviceId
Określa identyfikator wystąpienia urządzenia StorSimple, do którego odbędzie się błąd tego polecenia w grupach kontenerów woluminów.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDeviceName
Określa nazwę urządzenia StorSimple, na którym jest zawodzi to polecenie cmdlet w grupach kontenerów woluminów.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumecontainerGroups
Określa listę grup kontenerów woluminów, które ten polecenie cmdlet może przełączyć na inne urządzenie.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Lista\<DataContainerGroup\>
Do tego polecenia cmdlet można przetworzyć listę grup kontenerów woluminów.

## WYSYŁA

### Ciąg

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorSimpleFailoverVolumeContainers](./Get-AzureStorSimpleFailoverVolumeContainers.md)


