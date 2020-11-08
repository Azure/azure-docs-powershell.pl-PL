---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054669"
---
# Clear-AzureRemoteAppVmStaleAdObject

## STRESZCZENIe
Usuwa obiekty w usłudze Azure Active Directory skojarzone z maszynami wirtualnymi Azure RemoteApp, które już nie istnieją.

## POLECENIA

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Clear-AzureRemoteAppVmStaleAdObject** usuwa obiekty w usłudze Azure Active Directory skojarzone z maszynami wirtualnymi usługi Azure RemoteApp, które już nie istnieją.
Musisz użyć poświadczeń, które mają uprawnienia do usuwania obiektów usługi Azure Active Directory.
W przypadku określenia parametru Common *verbose* to polecenie cmdlet wyświetla nazwę każdego usuniętego obiektu.

## Przykłady

### Przykład 1. Wyczyść stare obiekty dla kolekcji
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

Po pierwszym poleceniu zostanie wyświetlony monit o podanie nazwy użytkownika i hasła przy użyciu funkcji **Uzyskaj-Credential**.
Polecenie zapisuje wyniki w zmiennej $AdminCredentials.

Drugie polecenie czyści stare obiekty dla kolekcji o nazwie contoso.
Polecenie korzysta z poświadczeń przechowywanych w zmiennej $AdminCredentials.
Aby wykonanie polecenia powiodło się, te poświadczenia muszą mieć odpowiednie prawa.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRemoteAppVmStaleAdObject](./Get-AzureRemoteAppVmStaleAdObject.md)


