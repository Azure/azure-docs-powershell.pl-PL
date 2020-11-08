---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055184"
---
# New-AzureServiceProject

## STRESZCZENIe
Tworzy wymagane pliki i konfigurację dla nowej usługi.

## POLECENIA

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **New-AzureServiceProject** tworzy wymagane pliki i konfigurację dla nowej usługi Azure w bieżącym katalogu.

## Przykłady

### Przykład 1. Tworzenie szkieletów dla usługi
```
PS C:\> New-AzureServiceProject MyService1
```

W tym przykładzie przedstawiono tworzenie szkieletów dla nowej usługi platformy Azure o nazwie MyService1 w bieżącym katalogu.

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

### -ServiceName
Określa nazwę usługi.
Określa pierwszą sekcję nazwy hosta w usłudze (na przykład name.cloudapp.net) oraz katalog, który będzie zawierać usługę.
Nazwa może zawierać tylko litery, cyfry i znaki kreski (-).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[Dodaj-AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[Publikowanie — AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


