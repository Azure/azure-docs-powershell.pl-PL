---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055017"
---
# Set-AzureRemoteAppWorkspace

## STRESZCZENIe
Ustawia właściwości obszaru roboczego usługi Azure RemoteApp.

## POLECENIA

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRemoteAppWorkspace** ustawia właściwości obszaru roboczego usługi Azure RemoteApp.

## Przykłady

### Przykład 1. Ustawianie nazwy obszaru roboczego
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

To polecenie ustawia nazwę obszaru roboczego usługi Azure RemoteApp na aplikacje firm contoso.

## PARAMETRÓW

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

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

### -Nazwa_obszaru_roboczego
Określa nazwę obszaru roboczego funkcji Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN
* Wszystkie kolekcje usługi Azure RemoteApp dla określonego abonamentu istnieją w udostępnionym obszarze roboczym.

## LINKI POKREWNE

[Get-AzureRemoteAppWorkspace](./Get-AzureRemoteAppWorkspace.md)


