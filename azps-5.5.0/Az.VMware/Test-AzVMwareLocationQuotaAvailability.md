---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
ms.openlocfilehash: 93ede93fc47d5afcabeda8a38a4d8c5fc57c30c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182538"
---
# Test-AzVMwareLocationQuotaAvailability

## SYNOPSIS
Przydział zwrotu dla subskrypcji według regionu

## SKŁADNIA

### Sprawdzanie (domyślne)
```
Test-AzVMwareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CheckViaIdentity
```
Test-AzVMwareLocationQuotaAvailability -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## OPIS
Przydział zwrotu dla subskrypcji według regionu

## PRZYKŁADY

### Przykład 1. Sprawdzanie dostępności przydziału
```powershell
PS C:\> Test-AzVMwareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

Sprawdzanie dostępności przydziału

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Lokalizacja
Region platformy Azure

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SubscriptionId
Identyfikator subskrypcji docelowej.

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.VCmdlet.Models.IVDentIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlet.V Jakas.Model.Api20200320.IQuota

## NOTATKI

ALIASY

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <IVMwareIdentity> Parametr tożsamości
  - `[AuthorizationName <String>]`: nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej
  - `[ClusterName <String>]`: nazwa klastra w chmurze prywatnej
  - `[HcxEnterpriseSiteName <String>]`: nazwa witryny HCX Enterprise w chmurze prywatnej
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[Location <String>]`: region platformy Azure
  - `[PrivateCloudName <String>]`: nazwa chmury prywatnej
  - `[ResourceGroupName <String>]`: nazwa grupy zasobów. W nazwie nie jest uwzględniania liter.
  - `[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.

## LINKI POKREWNE

