---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: f9e8eb9441604e3c07453f1e387ba17bd4623d55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526962"
---
# Get-AzureRmVMImage

## STRESZCZENIe
Pobiera wszystkie wersje VMImage.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ListVMImage
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [<CommonParameters>]
```

### GetVMImageDetail
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmVMImage** pobiera wszystkie wersje VMImage.

## Przykłady

### Przykład 1: pobieranie obiektów VMImage
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

To polecenie pobiera wszystkie wersje VMImage, które pasują do określonych wartości.

## PARAMETRÓW

### -FilterExpression
Określa wyrażenie filtru.

```yaml
Type: String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Offer
Określa typ oferty VMImage.
Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzureRmVMImageOffer.

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
Umożliwia określenie wydawcy VMImage.
Aby uzyskać wydawcę obrazu, użyj polecenia cmdlet Get-AzureRmVMImagePublisher.

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

### -SKU
Określa VMImage SKU.
Aby uzyskać jednostkę SKU, użyj polecenia cmdlet Get-AzureRmVMImageSku.

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

### -Version
Określa wersję VMImage.

```yaml
Type: String
Parameter Sets: GetVMImageDetail
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

[Get-AzureRmVMImageOffer](./Get-AzureRmVMImageOffer.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[Zapisz — AzureRmVMImage](./Save-AzureRmVMImage.md)


