---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImageType.md
ms.openlocfilehash: 15b1316940c42534844245eaaf1aee3e450adc4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526966"
---
# Get-AzureRmVMExtensionImageType

## STRESZCZENIe
Pobiera typ rozszerzenia platformy Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmVMExtensionImageType -Location <String> -PublisherName <String> [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmVMExtensionImageType** Pobiera typ rozszerzenia platformy Azure.

## Przykłady

### Przykład 1: uzyskiwanie typu obrazu rozszerzenia
```
PS C:\> Get-AzureRmVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

To polecenie pobiera typ obrazu rozszerzenia dla określonego wydawcy i lokalizacji.

## PARAMETRÓW

### — Lokalizacja
Określa lokalizację rozszerzenia.
To polecenie cmdlet umożliwia pobieranie typu rozszerzenia w lokalizacji, w której ten parametr określa.

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

### -PublisherName
Określa nazwę wydawcy rozszerzenia.
Aby uzyskać wydawcę rozszerzenia, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.
To polecenie cmdlet umożliwia pobieranie typu rozszerzenia od wydawcy, który określa ten parametr.

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

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)


