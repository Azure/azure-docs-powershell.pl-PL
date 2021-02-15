---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwareCluster.md
ms.openlocfilehash: cfe9a8aa16803433055eb0cec5993cedcbcb5874
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182530"
---
# Update-AzVMwareCluster

## SYNOPSIS
Aktualizowanie klastrów w chmurze prywatnej

## SKŁADNIA

### UpdateExpanded (Domyślna)
```
Update-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzVMwareCluster -InputObject <IVMwareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## OPIS
Aktualizowanie klastrów w chmurze prywatnej

## PRZYKŁADY

### Przykład 1. Aktualizowanie rozmiaru klastrów według nazwy
```powershell
PS C:\> Update-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

Aktualizowanie rozmiaru klastrów według nazwy

### Przykład 2. Aktualizowanie rozmiaru klastrów według obiektu wejściowego
```powershell
PS C:\> Get-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMwareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

Aktualizowanie rozmiaru klastrów według obiektu wejściowego

## PARAMETERS

### — AsJob
Uruchamianie polecenia jako zadania

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

### - ClusterSize
Rozmiar klastrów

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Nazwa klastra w chmurze prywatnej

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Uruchamianie polecenia asynchronicznie

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

### - PrivateCloudName
Nazwa chmury prywatnej

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.
W nazwie nie jest uwzględniania liter.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
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
Parameter Sets: UpdateExpanded
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

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.VCmdlet.Models.Api20200320.ICluster

## NOTATKI

ALIASY

COMPLEX PARAMETER PROPERTIES

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


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

