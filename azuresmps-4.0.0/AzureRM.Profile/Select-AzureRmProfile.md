---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523557"
---
# Select-AzureRmProfile

## STRESZCZENIe
Ładuje informacje o uwierzytelnianiu platformy Azure z pliku.

## POLECENIA

### InMemoryProfile
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### ProfileFromDisk
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## Opis
Polecenie cmdlet Select-AzureRmProfile ładuje informacje uwierzytelniające z pliku w celu ustawienia środowiska i kontekstu platformy Azure.
Polecenia cmdlet uruchomione w bieżącej sesji używają tych informacji do uwierzytelniania żądań usługi Azure Resource Manager.

## Przykłady

### Przykład 1. Wybieranie profilu z PSAzureProfile
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

W tym przykładzie wybrano profil z PSAzureProfile, który przekazano do polecenia cmdlet.

### Przykład 2: Wybieranie profilu z pliku JSON
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

W tym przykładzie wybrano profil z pliku JSON przekazanego do polecenia cmdlet. Ten plik JSON można utworzyć w usłudze Save-AzureRmProfile.

## PARAMETRÓW

### -Path
Określa ścieżkę do informacji o profilu zapisanych przy użyciu polecenia Save-AzureRMProfile.

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### PSAzureProfile

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRMContext]()

