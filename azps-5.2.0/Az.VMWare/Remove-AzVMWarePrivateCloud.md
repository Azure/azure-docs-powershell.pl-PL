---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345013"
---
# Remove-AzVMWarePrivateCloud

## STRESZCZENIe
Usuwanie prywatnej chmury

## POLECENIA

### Usuń (domyślnie)
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### DeleteViaIdentity
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Opis
Usuwanie prywatnej chmury

## Przykłady

### Przykład 1: usuwanie prywatnej chmury
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

Usuń chmurę prywatną

## PARAMETRÓW

### -AsJob
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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Inputobject
Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa prywatnej chmury

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nowait
Wykonywanie polecenia asynchronicznie

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

### -PassThru
Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.

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

### -ResourceGroupName
Nazwa grupy zasobów.
W nazwie nie jest rozróżniana wielkość liter.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subskrypcji
Identyfikator subskrypcji docelowej.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. PowerShell. cmdlets. VMWare. modele. IVMWareIdentity

## WYSYŁA

### System. Boolean

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


INPUTobject <IVMWareIdentity> : parametr Identity
  - `[AuthorizationName <String>]`: Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze
  - `[ClusterName <String>]`: Nazwa klastra w prywatnej chmurze
  - `[HcxEnterpriseSiteName <String>]`: Nazwa witryny usługi HCX Enterprise w chmurze prywatnej
  - `[Id <String>]`: Ścieżka tożsamości zasobu
  - `[Location <String>]`: Region platformy Azure
  - `[PrivateCloudName <String>]`: Nazwa chmury prywatnej
  - `[ResourceGroupName <String>]`: Nazwa grupy zasobów. W nazwie nie jest rozróżniana wielkość liter.
  - `[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.

## LINKI POKREWNE

