---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: b17b8198b54a6c1fd85b2f8bcb37b4c73e8be0ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013841"
---
# Get-AzVMDscExtensionStatus

## SYNOPSIS
Pobiera stan programu obsługi rozszerzenia DSC dla maszyny wirtualnej.

## SKŁADNIA

### GetDscExtension (Domyślne)
```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VMParameterSet
```
Get-AzVMDscExtensionStatus [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzVMDscExtensionStatus** pobiera stan programu obsługi rozszerzenia Żądana konfiguracja województwa (DSC) dla maszyny wirtualnej w grupie zasobów.
Po zastosowaniu konfiguracji to polecenie cmdlet daje wyniki zgodne z Start-DscConfiguration cmdlet.

## PRZYKŁADY

### Przykład 1

Pobiera stan programu obsługi rozszerzenia DSC dla maszyny wirtualnej. (wygenerowane automatycznie)

```powershell
<!-- Aladdin Generated Example --> 
Get-AzVMDscExtensionStatus -Name 'AgentPool01' -ResourceGroupName myresourcegroup -VMName 'VM01'
```

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
Określa nazwę zasobu usługi Azure Resource Manager reprezentującą to rozszerzenie.
Polecenie cmdlet Set-AzVMDscExtension ustawia tę nazwę na Microsoft.Powershell.DSC, która jest tą samą wartością używaną przez serwer **Get-AzVMDscExtensionStatus.**
Określ ten parametr tylko wtedy, gdy zmieniono nazwę domyślną w poleceniach cmdlet Set lub używano innej nazwy zasobu w szablonie Menedżer zasobów.

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — MASZYNY WIRTUALNEJ
Określa obiekt maszyny wirtualnej, dla których rozszerzenie jest wł.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NAZWA.MASZYNY.WIRTUALNEJ
Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet uzyskuje stan rozszerzenia DSC.

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
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

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView

## NOTATKI

## LINKI POKREWNE

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


