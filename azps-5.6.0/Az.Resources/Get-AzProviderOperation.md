---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 61e38afcccccd6a96e92983d24442740351320ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016042"
---
# Get-AzProviderOperation

## SYNOPSIS
Pobiera operacje dla dostawcy zasobów platformy Azure, które są zabezpieczane przy użyciu usługi Azure RBAC.

## SKŁADNIA

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Ten Get-AzProviderOperation uzyskuje dostęp do operacji ujawnionych przez dostawców zasobów platformy Azure.
Operacje można tworzyć w celu utworzenia ról niestandardowych w usłudze Azure RBAC.
Polecenie przyjmuje jako dane wejściowe ciąg wyszukiwania operacji (z możliwymi znakami wieloznacznych()), który określa szczegóły operacji *do wyświetlenia. Użyj Get-AzProviderOperation * w celu uzyskania wszystkich operacji dla wszystkich dostawców zasobów platformy Azure. Użyj Get-AzProviderOperation Microsoft.Compute/,* aby uzyskać wszystkie operacje dostawcy zasobów Microsoft.Compute.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich akcji dla wszystkich dostawców
```powershell
PS C:\> Get-AzProviderOperation *
```

### Przykład 2. Uzyskiwanie akcji dla określonego dostawcy zasobów
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### Przykład 3. Uzyskaj wszystkie akcje, które mogą być wykonywane na komputerach wirtualnych
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperationSearchString
Ciąg wyszukiwania operacji (z możliwymi symbolami wieloznacznymi (*) )

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation

## NOTATKI
Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie

## LINKI POKREWNE
