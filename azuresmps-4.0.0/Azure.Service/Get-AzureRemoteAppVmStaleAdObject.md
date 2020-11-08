---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054596"
---
# Get-AzureRemoteAppVmStaleAdObject

## STRESZCZENIe
Pobiera obiekty w usłudze Azure Active Directory skojarzone z maszynami wirtualnymi usługi Azure RemoteApp, które już nie istnieją.

## POLECENIA

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRemoteAppVmStaleAdObject** Pobiera obiekty w usłudze Azure Active Directory skojarzone z maszynami wirtualnymi usługi Azure RemoteApp, które już nie istnieją.
To polecenie cmdlet spowoduje wyświetlenie nazwy każdego z obiektów, które ma on pobierać.

## Przykłady

### Przykład 1: pobieranie starych obiektów dla kolekcji
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

To drugie polecenie pobiera stare obiekty kolekcji o nazwie contoso.

## PARAMETRÓW

### -CollectionName
Określa nazwę kolekcji funkcji Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Poświadczenie
Określa poświadczenie, które ma uprawnienia do wykonania tej akcji.
Aby uzyskać obiekt **PSCredential** , użyj polecenia cmdlet **Get-Credential** .
Jeśli nie podano tego parametru, to polecenie cmdlet użyje bieżących poświadczeń użytkownika.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Ciąg

## INFORMACYJN

## LINKI POKREWNE

[Clear-AzureRemoteAppVmStaleAdObject](./Clear-AzureRemoteAppVmStaleAdObject.md)


