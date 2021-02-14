---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237720"
---
# Get-AzSapMonitor

## SYNOPSIS
Pobiera właściwości monitora SAP dla określonej subskrypcji, grupy zasobów i nazwy zasobu.

## SKŁADNIA

### Lista (domyślna)
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Pobierz
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## OPIS
Pobiera właściwości monitora SAP dla określonej subskrypcji, grupy zasobów i nazwy zasobu.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich monitorów SAP w ramach subskrypcji
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

To polecenie pobiera monitory SAP w ramach subskrypcji.

### Przykład 2. Uzyskiwanie monitora SAP według nazwy
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

To polecenie otrzymuje monitor SAP według nazwy.

### Przykład 3. Uzyskiwanie monitora SAP według obiektu
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

To polecenie pobiera obiektowy monitor SAP.

### Przykład 4. Uzyskiwanie monitora SAP według potoku
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

To polecenie pobiera monitor SAP według potoku.

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
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Nazwa zasobu monitorowego SAP.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SubscriptionId
Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.
Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.HanaOnAzure.Models.IHanaOnAzureIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlet.HanaOnAzure.Models.Api20200207Preview.ISapMonitor

## NOTATKI

ALIASY

COMPLEX PARAMETER PROPERTIES

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <IHanaOnAzureIdentity> Parametr tożsamości
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[Location <String>]`: lokalizacja usuniętego magazynu.
  - `[OperationKind <AccessPolicyUpdateKind?>]`: nazwa operacji
  - `[ProviderInstanceName <String>]`: nazwa wystąpienia dostawcy.
  - `[ResourceGroupName <String>]`: nazwa grupy zasobów.
  - `[ResourceName <String>]`: nazwa zasobu tożsamości.
  - `[SapMonitorName <String>]`: nazwa zasobu monitorów SAP.
  - `[Scope <String>]`: zakres dostawcy zasobów dla zasobu. Zasób nadrzędny jest rozszerzany przez tożsamości zarządzane.
  - `[SubscriptionId <String>]`: Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.
  - `[VaultName <String>]`: nazwa magazynu

## LINKI POKREWNE

