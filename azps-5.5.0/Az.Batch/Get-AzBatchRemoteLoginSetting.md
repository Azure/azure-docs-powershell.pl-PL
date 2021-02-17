---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239300"
---
# Get-AzBatchRemoteLoginSetting

## SYNOPSIS
Pobiera ustawienia logowania zdalnego dla węzła obliczeniowego.

## SKŁADNIA

### Identyfikator (domyślne)
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzBatchRemoteLoginSetting** pobiera ustawienia logowania zdalnego dla węzła obliczeniowego w puli opartej na infrastrukturze maszyn wirtualnych.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie ustawień logowania zdalnego dla wszystkich węzłów w puli
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

Pierwsze polecenie uzyskuje kontekst konta wsadowego zawierającego klucze dostępu dla Twojej subskrypcji przy użyciu klucza **Get-AzBatchAccountKey.**
Polecenie przechowuje kontekst w zmiennej $Context do użycia w następnym poleceniu.
Drugie polecenie pobiera każdy węzeł obliczeniowy w puli o identyfikatorze ContosoPool przy użyciu polecenia **Get-AzBatchComputeNode.**
Polecenie przekazuje każdy węzeł komputera do bieżącego polecenia cmdlet przy użyciu operatora potoku.
Polecenie pobiera ustawienia logowania zdalnego dla każdego węzła obliczeniowego.

### Przykład 2. Uzyskiwanie ustawień logowania zdalnego dla węzła
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

Pierwsze polecenie pobiera kontekst konta wsadowego zawierającego klucze dostępu dla twojej subskrypcji, a następnie przechowuje je w $Context danych.
Drugie polecenie pobiera ustawienia logowania zdalnego dla węzła obliczeniowego, który ma określony identyfikator w puli, która ma identyfikator ContosoPool.

## PARAMETERS

### - BatchContext
Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.
Aby uzyskać **batchAccountContext** zawierający klucze dostępu dla subskrypcji, użyj Get-AzBatchAccountKey cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### - ComputeNode
Określa węzeł obliczeniowy jako **obiekt PSComputeNode,** dla którego to polecenie cmdlet pobiera ustawienia logowania zdalnego.
Aby uzyskać obiekt węzła obliczeniowego, użyj Get-AzBatchComputeNode cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
Określa identyfikator węzła obliczeniowego, dla którego mają być obliczane ustawienia logowania zdalnego.
dla którego to polecenie cmdlet uzyskuje dostęp do ustawień logowania zdalnego.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### - PoolId
Określa identyfikator puli zawierającej maszynę wirtualną.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Batch. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## OUTPUTS

### Microsoft.Azure.Commands.Batch. Models.PSRemoteLoginSettings

## NOTATKI

## LINKI POKREWNE

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Get-AzBatchRemoteDesktopProtocolFile](./Get-AzBatchRemoteDesktopProtocolFile.md)

[Polecenia cmdlet partii platformy Azure](/powershell/module/Az.Batch/)
