---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 1ac6f9b17f954361d95e6855a618c7dbbf3d20f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001786"
---
# Get-AzVmssVM

## SYNOPSIS
Pobiera właściwości maszyny wirtualnej MASZYNY WIRTUALNEJ.

## SKŁADNIA

### DefaultParameters (domyślny)
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzVmssVM** pobiera widok modelu i widok wystąpienia maszyny wirtualnej ( VIRTUAL Machine Scale Set) maszyny wirtualnej .
Widok modelu to właściwości maszyny wirtualnej określone przez użytkownika.
Widok wystąpienia jest stanem poziomu wystąpienia maszyny wirtualnej.
Określ parametr *statusu,* aby uzyskać tylko widok wystąpienia maszyny wirtualnej.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie właściwości maszyny wirtualnej MASZYNY WIRTUALNEJ
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

To polecenie pobiera właściwości maszyny wirtualnej MASZYNY WIRTUALNEJ o nazwie VIRTUALSS001, która należy do grupy zasobów o nazwie Group001.
Ponieważ to polecenie nie określa *parametru przełącznika InstanceView,* polecenie cmdlet pobiera widok modelu maszyny wirtualnej.

### Przykład 2. Uzyskiwanie właściwości widoku modelu maszyny wirtualnej MASZYNY WIRTUALNEJ
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

To polecenie pobiera właściwości maszyny wirtualnej MASZYNY WIRTUALNEJ o nazwie VIRTUALSS04, która należy do grupy zasobów o nazwie Group002.
To polecenie pobiera identyfikator wystąpienia przechowywany w zmiennej $ID, dla której można uzyskać widok modelu.

### Przykład 3. Uzyskiwanie właściwości widoku wystąpienia maszyny wirtualnej MASZYNY WIRTUALNEJ
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

To polecenie pobiera właściwości maszyny wirtualnej MASZYNY WIRTUALNEJ o nazwie VIRTUALSS04, która należy do grupy zasobów o nazwie Group002.
Ponieważ to polecenie określa parametr *przełącznika InstanceView,* polecenie cmdlet pobiera widok wystąpienia maszyny wirtualnej.
To polecenie pobiera identyfikator wystąpienia przechowywany w zmiennej $ID, dla której można uzyskać widok wystąpienia.

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

### -InstanceId
Określa identyfikator wystąpienia, dla którego ma być pobrać widok modelu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceView
Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia maszyny wirtualnej.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyn wirtualnych.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Nazwa maszyny wirtualnej to "gatunek".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## NOTATKI

## LINKI POKREWNE

[Set-AzVmssVM](./Set-AzVmssVM.md)

[Get-AzVmss](./Get-AzVmss.md)


