---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6badeec8b2425a5ca8e10dc88039a1d28e055cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527957"
---
# New-AzureRmPowerBIEmbeddedCapacity

## STRESZCZENIe
Tworzy nową, zawbudowaną pojemność usługi PowerBI.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmPowerBIEmbeddedCapacity 
    [-ResourceGroupName] <String> 
    [-Name] <String> 
    [-Location] <String>
    [-Sku] <String> 
    [-Administrator] <String>
    [[-Tag] <Hashtable>] 
    [-WhatIf] 
    [-Confirm] 
    [<CommonParameters>]
```

## Opis
Polecenie cmdlet New-AzureRmPowerBIEmbeddedCapacity tworzy nową, zawbudowaną pojemność usługi PowerBI

## Przykłady

### Przykład 1
```
PS C:\> New-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

Tworzy wydajność o nazwie testcapacity w regionie Azure Region Zachodni (Stanów Zjednoczonych) i w grupie zasób testRG. Poziom wersji SKU dla wydajności to a1.

## PARAMETRÓW

### -ResourceGroupName
Nazwa grupy zasobów platformy Azure, do której należy pojemność

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa wbudowanej pojemności usługi PowerBI

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### — Lokalizacja
Obszar platformy Azure, w którym jest hostowana pojemność osadzona w usłudze PowerBI

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept wildcard characters: False
```

### -SKU
Nazwa jednostki SKU dla pojemności.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept wildcard characters: False
```

### -Administrator
Nazwy pojemności rozdzielone przecinkami, które są ustawiane jako administrator na stanowisku

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept wildcard characters: False
```

### -Tag
Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na pojemności.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### -Potwierdź
Monituje użytkownika o potwierdzenie, czy wykonać operację.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. PowerBI. modele. PSPowerBIEmbeddedCapacity

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmPowerBIEmbeddedCapacity](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[Remove-AzureRmPowerBIEmbeddedCapacity](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
