---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 199b61bc8ef075aabc09870cde436a0e49598ee8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244019"
---
# Update-AzContainerService

## SYNOPSIS
Aktualizuje stan usługi kontenerowej.

## SKŁADNIA

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Update-AzContainerService** aktualizuje stan usługi kontenerowej w celu dopasowania do lokalnego wystąpienia usługi.

## PRZYKŁADY

### Przykład 1. Aktualizowanie usługi kontenerowej
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

To polecenie pobiera usługę kontenera o nazwie CSResourceGroup17 za pomocą Get-AzContainerService cmdlet.
Polecenie przekazuje ten obiekt do Remove-AzContainerServiceAgentPoolProfile cmdlet przy użyciu operatora potoku.
**Remove-AzContainerServiceAgentPoolProfile** usuwa profil o nazwie AgentPool01.
Polecenie przekazuje wynik do Add-AzContainerServiceAgentPoolProfile cmdlet.
**Add-AzContainerServiceAgentPoolProfile** dodaje profil o nazwie AgentPool01 i ma określone właściwości.
Polecenie przekazuje wynik do bieżącego polecenia cmdlet.
Bieżące polecenie cmdlet aktualizuje usługę kontenerów w celu odzwierciedlenia zmian wprowadzonych za pomocą tego polecenia.

## PARAMETERS

### — AsJob
Uruchamianie polecenia cmdlet w tle

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerService
Określa obiekt **lokalny ContainerService** zawierający zmiany.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
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

### — Nazwa
Określa nazwę usługi kontenerów, która będzie aktualizowana przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa grupę zasobów usługi kontenerów, która jest aktualizowana przez to polecenie cmdlet.

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService

## NOTATKI

## LINKI POKREWNE

[Add-AzContainerServiceAgentPoolProfile](./Add-AzContainerServiceAgentPoolProfile.md)

[Get-AzContainerService](./Get-AzContainerService.md)

[New-AzContainerService](./New-AzContainerService.md)

[Remove-AzContainerService](./Remove-AzContainerService.md)

[Remove-AzContainerServiceAgentPoolProfile](./Remove-AzContainerServiceAgentPoolProfile.md)


