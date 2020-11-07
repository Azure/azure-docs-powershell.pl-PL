---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: f299d0f299eaef61ba3655e8ec221cc55f5ab578
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718949"
---
# Get-AzureRmVMImagePublisher

## STRESZCZENIe
Pobiera wydawców VMImage.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmVMImagePublisher -Location <String> [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmVMImagePublisher** pobiera wydawców VMImage.

## Przykłady

### Przykład 1: uzyskiwanie wydawców VMImage dla regionu
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

To polecenie umożliwia uzyskiwanie wydawców wystąpień VMImage dla centralnego regionu USA w ramach Twojego profilu platformy Azure.

## PARAMETRÓW

### — Lokalizacja
Określa lokalizację VMImage.

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

[Get-AzureRmVMImage](./Get-AzureRmVMImage.md)

[Get-AzureRmVMImageOffer](./Get-AzureRmVMImageOffer.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[Zapisz — AzureRmVMImage](./Save-AzureRmVMImage.md)


