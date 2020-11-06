---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: 179b4b028c7dd9338e75d07f559a61052b3d2bcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527010"
---
# Set-AzureRmCdnOrigin

## STRESZCZENIe
Aktualizuje serwer pochodzenia sieci CDN.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmCdnOrigin** aktualizuje serwer pochodzenia sieci dostarczania zawartości platformy Azure (CDN).

## Przykłady

## PARAMETRÓW

### -CdnOrigin
Określa serwer pochodzenia, który jest aktualizowany przez to polecenie cmdlet.

```yaml
Type: PSOrigin
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### PSOrigin
Parametr "CdnOrigin' akceptuje wartość typu" PSOrigin' z rurociągu

## WYSYŁA

### Microsoft. Azure. Commands. CDN. MODELES. Origin. PSOrigin

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmCdnOrigin](./Get-AzureRmCdnOrigin.md)


