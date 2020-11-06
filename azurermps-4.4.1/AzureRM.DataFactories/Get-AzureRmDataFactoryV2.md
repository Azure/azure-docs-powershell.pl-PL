---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
ms.openlocfilehash: cba3540f47d2ce53b11a11f237adb28aa0bec6a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527686"
---
# Get-AzureRmDataFactoryV2

## STRESZCZENIe
Pobiera informacje o fabryce danych.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Get-AzureRmDataFactoryV2 pobiera informacje na temat fabryk danych w grupie zasobów platformy Azure.
Jeśli określisz nazwę fabryki danych, to polecenie cmdlet będzie pobierać informacje na temat fabryki danych.
Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich fabryk danych w grupie zasobów platformy Azure.

## Przykłady

### Przykład 1: pobieranie wszystkich fabryk danych
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded
```

Wyświetla informacje dotyczące wszystkich fabryk danych w subskrypcji platformy Azure.

### Przykład 2: uzyskiwanie określonej fabryki danych
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

To polecenie wyświetla informacje o fabryce danych o nazwie WikiADF w subskrypcji grupy zasobów o nazwie ADF, a następnie zapisuje je w zmiennej $DataFactory.
Określ parametr DataFactory w kolejnych poleceniach cmdlet, aby użyć fabryki danych przechowywanej w $DataFactory.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę fabryki danych, o której należy uzyskać informacje.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet umożliwia pobieranie informacji na temat fabryk danych należących do grupy, którą określa ten parametr.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String

## WYSYŁA

### System. Collections. Generic. list "1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral; PublicKeyToken = null]]
Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory

## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki

## LINKI POKREWNE

[Set-AzureRmDataFactoryV2]()

[Remove-AzureRmDataFactoryV2]()

