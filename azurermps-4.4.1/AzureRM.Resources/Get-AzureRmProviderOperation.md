---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: d4e58e1fc2da68d9293afa27072a4cf32023f661
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717804"
---
# Get-AzureRmProviderOperation

## STRESZCZENIe
Pobiera operacje dla dostawcy zasobów platformy Azure, które są zabezpieczane przy użyciu usługi Azure RBAC.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmProviderOperation [-OperationSearchString] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Get-AzureRmProviderOperation pobiera operacje udostępnione przez dostawców zasobów platformy Azure.
Operacje mogą być składane w celu utworzenia ról niestandardowych w usłudze Azure RBAC.
Polecenie przyjmuje jako wartość wejściową ciąg wyszukiwania operacji (z możliwymi znakami wieloznacznymi (*)), który określa szczegóły operacji do wyświetlenia.

Użyj Get-AzureRmProviderOperation *, aby pobrać wszystkie operacje dla wszystkich dostawców zasobów platformy Azure.

Użyj Get-AzureRmProviderOperation Microsoft. COMPUTE/*, aby pobrać wszystkie operacje dotyczące dostawcy zasobów Microsoft. COMPUTE.

## Przykłady

### --------------------------Pobierać wszystkie akcje dla wszystkich dostawców--------------------------
```
PS C:\> Get-AzureRmProviderOperation *
```

### --------------------------Otrzymywać akcje dla konkretnego dostawcy zasobów--------------------------
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### --------------------------Pobierać wszystkie akcje, które można wykonywać na maszynach wirtualnych--------------------------
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## PARAMETRÓW

### -OperationSearchString
Ciąg wyszukiwania operacji (z możliwymi symbolami wieloznacznymi (*))

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### Ciąg
Parametr "OperationSearchString" akceptuje wartość typu "String" z procesu

## WYSYŁA

### Microsoft. Azure. Commands. resources. models. PSResourceProviderOperation

## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie

## LINKI POKREWNE

