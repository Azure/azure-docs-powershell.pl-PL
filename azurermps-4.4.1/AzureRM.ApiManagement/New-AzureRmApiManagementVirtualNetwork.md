---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525793"
---
# New-AzureRmApiManagementVirtualNetwork

## STRESZCZENIe
Tworzy wystąpienie PsApiManagementVirtualNetwork.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmApiManagementVirtualNetwork** jest poleceniem pomagającym w celu utworzenia wystąpienia **PsApiManagementVirtualNetwork**.
To polecenie jest używane przy użyciu polecenia cmdlet **Set-AzureRMApiManagementVirtualNetworks** .

## Przykłady

### Przykład 1. Tworzenie sieci wirtualnej
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

W tym przykładzie jest tworzona Sieć wirtualna, a następnie jest wywoływana funkcja cmdlet **Set-AzureRmApiManagementVirtualNetworks** .

## PARAMETRÓW

### — Lokalizacja
Określa lokalizację sieci wirtualnej, w której to polecenie cmdlet tworzy wystąpienie.

Dopuszczalne wartości tego parametru to:

- Północno-środkowe USA
- Południowa Centrala amerykańska
- Centralny stan
- Europa Zachodnia
- Europa Północna
- Zachodnie USA
- Wschodnie USA
- Wschód USA 2
- Japonia wschodni
- Japonia Zachodnia
- Brazylia Południowa
- Azja Południowo-Wschodnia
- Azja Wschodnia
- Australia Wschodnia
- Australia południowy

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetResourceId
Określa identyfikator zasobu podsieci sieci wirtualnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
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

## WYSYŁA

### Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVirtualNetwork

## INFORMACYJN

## LINKI POKREWNE

