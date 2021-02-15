---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182163"
---
# Register-AzAutomationDscNode

## SYNOPSIS
Rejestruje maszynę wirtualną platformy Azure z systemem operacyjnym Windows jako węzeł dsc dla konta automatyzacji.

## SKŁADNIA

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Register-AzAutomationDscNode** rejestruje maszynę wirtualną platformy Azure jako węzeł APS Desired State Configuration (DSC) na koncie usługi Azure Automation. To polecenie cmdlet zarejestruje tylko maszyny wirtualne z systemem operacyjnym Windows jako węzeł automatyzacji DSC dla konta.

Jeśli musisz zarejestrować węzeł do konta automatyzacji w innej subskrypcji, musisz użyć szablonu ARM zamiast polecenia cmdlet. Aby uzyskać więcej szczegółowych [informacji,](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) zapoznaj się z dokumentacją usługi Azure Automation.

## PRZYKŁADY

### Przykład 1. Rejestrowanie maszyny wirtualnej platformy Azure jako węzła usługi Azure DSC
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

To polecenie rejestruje maszynę wirtualną platformy Azure o nazwie VirtualMachine01 jako węzeł DSC w koncie automatyzacji o nazwie Contoso17.

## PARAMETERS

### -ActionAfterReboot
Określa akcję, która zostanie uruchomiona przez maszynę wirtualną po jej ponownym uruchomieniu.
Prawidłowe wartości to: 
- ContinueConfiguration 
- StopConfiguration

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AllowModuleOverwrite
Określa, czy nowe konfiguracje pobierane przez ten węzeł dsc z serwera pobierania dsc automatyzacji Azure zastępują istniejące moduły już w węźle docelowym.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutomationAccountName
Określa nazwę konta automatyzacji, w którym to polecenie cmdlet rejestruje maszynę wirtualną.

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

### -AzureVMLocation
Lokalizacja maszyny wirtualnej platformy Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### —AzureVMName
Nazwa maszyny wirtualnej platformy Azure, która ma być zarejestrowana w celu zarządzania w usłudze Azure Automation DSC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMResourceGroup
Nazwa grupy zasobów maszyny wirtualnej platformy Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - ConfigurationMode
Określa tryb konfiguracji dsc.
Prawidłowe wartości to: 
- ApplyAndMonitor 
- ApplyAndAutocorrect 
- ApplyOnly

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationModeFrequencyMins
Określa częstotliwość (w minutach), z jaką aplikacja dsc w tle próbuje zaimplementować bieżącą konfigurację w węźle docelowym.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -NodeConfigurationName
Określa nazwę konfiguracji węzła, która jest konfigurowana przez to polecenie cmdlet w celu skonfigurowania maszyny wirtualnej do ściągania z centrum ds. automatyzacji Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RebootNodeIfNeeded
Określa, czy w razie potrzeby uruchomić ponownie maszynę wirtualną.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RefreshFrequencyMins
Określa częstotliwość w minutach, z którą lokalny Menedżer konfiguracji kontaktuje się z serwerem pobierania dsc automatyzacji Azure, aby pobrać najnowszą konfigurację węzła.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów.
Konto automatyzacji, za pomocą którego to polecenie cmdlet rejestruje maszynę wirtualną, należy do grupy zasobów, którą określa ten parametr.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### System.Int32

### System.Boolean

## OUTPUTS

### System.Void

## NOTATKI

## LINKI POKREWNE

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Set-AzAutomationDscNode](./Set-AzAutomationDscNode.md)

[Unregister-AzAutomationDscNode](./Unregister-AzAutomationDscNode.md)


