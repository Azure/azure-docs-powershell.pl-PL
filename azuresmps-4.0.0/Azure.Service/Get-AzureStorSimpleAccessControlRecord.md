---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055518"
---
# Get-AzureStorSimpleAccessControlRecord

## STRESZCZENIe
Pobiera rekordy kontroli dostępu w konfiguracji usługi.

## POLECENIA

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorSimpleAccessControlRecord** pobiera rekordy kontroli dostępu w konfiguracji usługi StorSimple Manager.
To polecenie cmdlet pobiera wszystkie rekordy lub nazwany rekord.

Rekordy kontroli dostępu są kontenerami parametrów inicjatora iSCSI.
Te parametry określają, którzy inicjatorzy mogą uzyskać dostęp do woluminu.
Gdy inicjator iSCSI próbuje połączyć się z woluminem, urządzenie sprawdza rekordy kontroli dostępu przypisane do tego woluminu.
Jeśli parametry inicjatora iSCSI pasują do jednego z wpisów w rekordzie kontroli dostępu zamapowanym na ten wolumin, inicjator iSCSI może nawiązywać połączenie.

## Przykłady

### Przykład 1. pobieranie wszystkich rekordów kontroli dostępu
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

To polecenie pobiera wszystkie rekordy kontroli dostępu.

### Przykład 2: uzyskiwanie określonego rekordu kontroli dostępu
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

To polecenie uzyskuje rekord kontroli dostępu o nazwie Acr11.

## PARAMETRÓW

### -ACRName
Określa nazwę rekordu kontroli dostępu, który ma zostać wyświetlony.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### AccessControlRecord, IList\<AccessControlRecord\>
To polecenie cmdlet zwraca obiekt **AccessControlRecord** lub obiekt **IList \<AccessControlRecord\>** .
Obiekt **AccessControlRecord** zawiera następujące pola: 

- **GlobalId** ( **ciąg** ) 
- **Initiatorname** ( **ciąg** ) 
- **InstanceId** ( **ciąg** ) 
- **Name** ( **ciąg** ) 
- **OperationInProgress** ( **OperationInProgress** ) 
- **VolumeCount** ( **int** )

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Remove-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)


