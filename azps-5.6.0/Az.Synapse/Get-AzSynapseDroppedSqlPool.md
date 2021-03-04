---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedroppedsqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
ms.openlocfilehash: 26e4e5c77913f01b8a7097f6baebd68977ceed22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981834"
---
# Get-AzSynapseDroppedSqlPool

## SYNOPSIS
Pobiera upuszczona kopia zapasowa puli sql dla puli składni Synapse Sql.

## SKŁADNIA

### GetByNameParameterSet (domyślne)
```
Get-AzSynapseDroppedSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DroppedSqlPoolResourceId
```
Get-AzSynapseDroppedSqlPool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzSynapseDroppedSqlPool** pobiera określoną usuniętą kopię zapasową puli SQL, która można przywrócić, lub wszystkie usunięte kopie zapasowe, które można przywrócić w obszarze roboczym. 


## PRZYKŁADY

### Przykład 1. Uzyskiwanie określonych upuszczanych buforów sql z puli sql
```powershell
PS C:\> Get-AzSynapseDroppedSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name "ContosoSqlPool"
```
Polecenie cmdlet pobiera upuszczane bufory sql dla puli sql.

### Przykład 2. Uzyskiwanie całej usuniętej buforu sql w obszarze roboczym
```
PS C:\>Get-AzSynapseDroppedSqlPool -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
To polecenie jest dostępne wszystkiego w upuszczanej bazie danych sqlpool w określonym obszarze roboczym.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### — Nazwa
Pula języka Sql Synapse.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: AzSynapseDroppedSqlPool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Wprowadzanie usuniętego identyfikatora zasobu puli sql.

```yaml
Type: System.String
Parameter Sets: DroppedSqlPoolResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Nazwa obszaru roboczego aplikacji Synapse.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel

## NOTATKI

## LINKI POKREWNE
