---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055257"
---
# Get-AzureStorSimpleDeviceConnectedInitiator

## STRESZCZENIe
Pobiera połączenia iSCSI dostępne dla urządzenia StorSimple.

## POLECENIA

### IdentifyById
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorSimpleDeviceConnectedInitiator** pobiera listę połączeń iSCSI dostępnych dla urządzenia StorSimple.
Obiekty połączeń iSCSI, które ten aplet cmdlet zwróci, zawierają następujące właściwości:

- **AcrInstanceId**
- **AcrName**
- **AllowedVolumeNames**
- **InitiatorAddress**
- **Połączeń**
- **IQN**
- **IscsiConnectionId**

Ten aplet polecenia pobiera obiekt Connection tylko wtedy, gdy na urządzeniu są włączone połączenia iSCSI.
Połączenia są domyślnie wyłączone.

## Przykłady

### Przykład 1: uzyskiwanie wszystkich połączeń dla urządzenia
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

To polecenie pobiera wszystkie połączenia iSCSI dotyczące urządzenia o nazwie Contoso63-AppVm.
To polecenie zwraca połączenia tylko wtedy, gdy dla urządzenia są włączone połączenia.

## PARAMETRÓW

### -DeviceId
Określa identyfikator wystąpienia urządzenia StorSimple, z którego mają być odbierane inicjatory iSCSI.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Określa nazwę urządzenia StorSimple, z którego mają być odbierane inicjatory iSCSI.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

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

### Znaleziono

## WYSYŁA

### Lista\<IscsiConnection\>
To polecenie cmdlet zwraca obiekt połączenia iSCSI zawierający następujące właściwości: 

- **AcrInstanceId**
- **AcrName**
- **AllowedVolumeNames**
- **InitiatorAddress**
- **Połączeń**
- **IQN**
- **IscsiConnectionId**

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)


