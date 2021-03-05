---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 516bc63d7866ffd8a3c16fd224a49697c0cc972f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001802"
---
# Get-AzCloudServiceRoleInstance

## SYNOPSIS
Pobiera wystąpienie roli z usługi w chmurze.

## SKŁADNIA

### Lista (domyślna)
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Pobierz
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## OPIS
Pobiera wystąpienie roli z usługi w chmurze.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich wystąpień ról
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard
ContosoFrontEnd_IN_1    eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard

```

To polecenie pobiera właściwości wszystkich wystąpień ról usługi w chmurze o nazwie ContosoCS, które należą do grupy zasobów o nazwie ContosOrg.

### Przykład 2. Uzyskiwanie właściwości pojedynczego wystąpienia roli
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard

```

To polecenie pobiera właściwości wystąpienia roli o nazwie ContosoFrontEnd_IN_0 o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.

## PARAMETERS

### -CloudServiceName
.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
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

### — Rozwiń
Wyrażenie rozwijania, które ma być stosowane do operacji.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.InstanceViewTypes
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleInstanceName
Nazwa wystąpienia roli.

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
Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.
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

### Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.ICloudServiceIdentity

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.IRoleInstance

## NOTATKI

ALIASY

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`: nazwa wystąpienia roli.
  - `[RoleName <String>]`: nazwa roli.
  - `[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.
  - `[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji. Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.

## LINKI POKREWNE

