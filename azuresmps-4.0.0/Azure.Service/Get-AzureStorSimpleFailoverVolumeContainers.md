---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054527"
---
# Get-AzureStorSimpleFailoverVolumeContainers

## STRESZCZENIe
Pobiera grupy kontenerów woluminów dla trybu failover urządzenia.

## POLECENIA

### IdentifyById
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorSimpleFailoverVolumeContainers** umożliwia pobieranie grup kontenerów woluminów dla trybu failover urządzenia.
Przekazanie pojedynczej grupy **VolumeContainer** lub tablicy grup **VolumeContainer** do polecenia cmdlet **Start-AzureStorSimpleDeviceFailover** .
Tylko grupy, które mają wartość $True dla właściwości **IsDCGroupEligibleForDR** , kwalifikują się do przejęcia awaryjnego.

## Przykłady

### Przykład 1: pobieranie kontenerów woluminów w trybie failover
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

To polecenie umożliwia przejęcie pracy awaryjnej kontenery woluminów.
W przypadku pracy awaryjnej urządzenia można użyć tylko DCGroups z wartością $True dla właściwości **IsDCGroupEligibleForDR** .

## PARAMETRÓW

### -DeviceId
Określa identyfikator wystąpienia urządzenia StorSimple, na którym ma być uruchomione polecenie cmdlet.

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
Określa nazwę urządzenia StorSimple, na którym ma być uruchomione polecenie cmdlet.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### IList\<DataContainerGroup\>
To polecenie cmdlet zwraca listę grup **VolumeContainer** .

## INFORMACYJN

## LINKI POKREWNE

[Start — AzureStorSimpleDeviceFailoverJob](./Start-AzureStorSimpleDeviceFailoverJob.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)


