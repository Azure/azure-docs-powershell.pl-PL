---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
ms.openlocfilehash: 133dc4dd259025556ab5f8dd3b848ae70a5101c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988625"
---
# Test-AzVMWareLocationTrialAvailability

## SYNOPSIS
Zwracanie stanu wersji próbnej dla subskrypcji według regionu

## SKŁADNIA

### Sprawdzanie (domyślne)
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CheckViaIdentity
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## OPIS
Zwracanie stanu wersji próbnej dla subskrypcji według regionu

## PRZYKŁADY

### Przykład 1. Sprawdzanie dostępności wersji próbnej
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

Sprawdzanie dostępności wersji próbnej

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
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
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

### Microsoft.Azure.PowerShell.Cmdlet.VMWare.Models.IVMWareIdentity

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.cmdlet.VMWare.Models.Api20200320.ITrial

## NOTATKI

ALIASY

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <IVMWareIdentity> Parametr tożsamości
  - `[AuthorizationName <String>]`: nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej
  - `[ClusterName <String>]`: nazwa klastra w chmurze prywatnej
  - `[HcxEnterpriseSiteName <String>]`: nazwa witryny HCX Enterprise w chmurze prywatnej
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[Location <String>]`: region platformy Azure
  - `[PrivateCloudName <String>]`: nazwa chmury prywatnej
  - `[ResourceGroupName <String>]`: nazwa grupy zasobów. W nazwie nie jest uwzględniania liter.
  - `[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.

## LINKI POKREWNE

