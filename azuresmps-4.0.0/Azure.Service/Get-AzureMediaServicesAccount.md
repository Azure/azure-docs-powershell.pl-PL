---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055301"
---
# Get-AzureMediaServicesAccount

## STRESZCZENIe
Pobiera dostępne konta usługi Azure Media Services.

**Uwaga:** Ta wersja jest przestarzała, sprawdź [nowszą wersję](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).

## POLECENIA

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Aby wyświetlić listę wszystkich kont, użyj `Get-AzureMediaServicesAccount` polecenia cmdlet.
Aby uzyskać bardziej szczegółowe informacje na temat określonego konta, użyj `Get-AzureMediaServicesAccount -Name YourAccountName` polecenia cmdlet.

## Przykłady

### Przykład 1: Lista wszystkich kont usług multimedialnych
```
PS C:\> Get-AzureMediaServicesAccount
```

To polecenie wyświetla listę wszystkich dostępnych kont usług multimedialnych.

### Przykład 2: uzyskiwanie szczegółowych informacji o koncie usług multimedialnych
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

To polecenie wyświetla właściwości konta usług multimedialnych.

## PARAMETRÓW

### -Name (nazwa)
Nazwa konta usług multimedialnych.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## INFORMACYJN

## LINKI POKREWNE

[Jak używać usługi Azure PowerShell dla usług multimedialnych](https://go.microsoft.com/fwlink/?LinkId=324179)


