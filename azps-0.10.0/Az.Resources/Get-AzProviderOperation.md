---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 21e1af2a36478f2e0b8e470660d0fbe2539a396e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892582"
---
# Get-AzProviderOperation

## STRESZCZENIe
Pobiera operacje dla dostawcy zasobów platformy Azure, które są zabezpieczane przy użyciu usługi Azure RBAC.

## POLECENIA

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Get-AzProviderOperation pobiera operacje udostępnione przez dostawców zasobów platformy Azure.
Operacje mogą być składane w celu utworzenia ról niestandardowych w usłudze Azure RBAC.
Polecenie przyjmuje jako wartość wejściową ciąg wyszukiwania operacji (z możliwymi znakami wieloznacznymi) *, który określa szczegóły operacji do wyświetlenia. Użyj Get-AzProviderOperation *, aby pobrać wszystkie operacje dla wszystkich dostawców zasobów platformy Azure. Użyj Get-AzProviderOperation Microsoft. COMPUTE/* , aby pobrać wszystkie operacje dotyczące dostawcy zasobów Microsoft. COMPUTE.

## Przykłady

### Pobierz wszystkie akcje dla wszystkich dostawców
```
PS C:\> Get-AzProviderOperation *
```

### Uzyskiwanie akcji dla określonego dostawcy zasobów
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Uzyskiwanie wszystkich akcji, które można wykonywać na maszynach wirtualnych
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationSearchString
Ciąg wyszukiwania operacji (z możliwymi symbolami wieloznacznymi (*))

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String
Parametry: OperationSearchString (ByValue)

## WYSYŁA

### Microsoft. Azure. Commands. resources. models. PSResourceProviderOperation

## INFORMACYJN
Słowa kluczowe: Azure, AZ, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie

## LINKI POKREWNE
