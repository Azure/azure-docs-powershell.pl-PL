---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185802"
---
# <span data-ttu-id="53c55-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="53c55-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="53c55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53c55-102">SYNOPSIS</span></span>
<span data-ttu-id="53c55-103">Poprawki pola Tagi na monitorze SAP dla określonej subskrypcji, grupy zasobów i nazwy monitora.</span><span class="sxs-lookup"><span data-stu-id="53c55-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="53c55-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="53c55-104">SYNTAX</span></span>

### <span data-ttu-id="53c55-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="53c55-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="53c55-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="53c55-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="53c55-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="53c55-107">DESCRIPTION</span></span>
<span data-ttu-id="53c55-108">Poprawki pola Tagi na monitorze SAP dla określonej subskrypcji, grupy zasobów i nazwy monitora.</span><span class="sxs-lookup"><span data-stu-id="53c55-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="53c55-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="53c55-109">EXAMPLES</span></span>

### <span data-ttu-id="53c55-110">Przykład 1. Aktualizowanie monitora SAP według nazwy</span><span class="sxs-lookup"><span data-stu-id="53c55-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="53c55-111">To polecenie aktualizuje monitor SAP według nazwy.</span><span class="sxs-lookup"><span data-stu-id="53c55-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="53c55-112">Przykład 2. Aktualizowanie monitora SAP według obiektu</span><span class="sxs-lookup"><span data-stu-id="53c55-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="53c55-113">To polecenia aktualizuje monitor SAP według obiektów.</span><span class="sxs-lookup"><span data-stu-id="53c55-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="53c55-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53c55-114">PARAMETERS</span></span>

### <span data-ttu-id="53c55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c55-115">-DefaultProfile</span></span>
<span data-ttu-id="53c55-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="53c55-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53c55-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53c55-117">-InputObject</span></span>
<span data-ttu-id="53c55-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="53c55-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53c55-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="53c55-119">-Name</span></span>
<span data-ttu-id="53c55-120">Nazwa zasobu monitorowego SAP.</span><span class="sxs-lookup"><span data-stu-id="53c55-120">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c55-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53c55-121">-ResourceGroupName</span></span>
<span data-ttu-id="53c55-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="53c55-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="53c55-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53c55-123">-SubscriptionId</span></span>
<span data-ttu-id="53c55-124">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="53c55-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="53c55-125">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="53c55-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="53c55-126">— Tag</span><span class="sxs-lookup"><span data-stu-id="53c55-126">-Tag</span></span>
<span data-ttu-id="53c55-127">Pole Tagi zasobu.</span><span class="sxs-lookup"><span data-stu-id="53c55-127">Tags field of the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c55-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53c55-128">-Confirm</span></span>
<span data-ttu-id="53c55-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="53c55-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c55-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c55-130">-WhatIf</span></span>
<span data-ttu-id="53c55-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53c55-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53c55-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="53c55-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c55-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c55-133">CommonParameters</span></span>
<span data-ttu-id="53c55-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c55-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c55-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53c55-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c55-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53c55-136">INPUTS</span></span>

### <span data-ttu-id="53c55-137">Microsoft.Azure.PowerShell.Cmdlet.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="53c55-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="53c55-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53c55-138">OUTPUTS</span></span>

### <span data-ttu-id="53c55-139">Microsoft.Azure.PowerShell.Cmdlet.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="53c55-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="53c55-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="53c55-140">NOTES</span></span>

<span data-ttu-id="53c55-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="53c55-141">ALIASES</span></span>

<span data-ttu-id="53c55-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="53c55-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="53c55-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="53c55-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="53c55-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="53c55-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="53c55-145">INPUTOBJECT: <IHanaOnAzureIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="53c55-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="53c55-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="53c55-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="53c55-147">`[Location <String>]`: lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="53c55-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="53c55-148">`[OperationKind <AccessPolicyUpdateKind?>]`: nazwa operacji</span><span class="sxs-lookup"><span data-stu-id="53c55-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="53c55-149">`[ProviderInstanceName <String>]`: nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="53c55-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="53c55-150">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="53c55-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="53c55-151">`[ResourceName <String>]`: nazwa zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="53c55-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="53c55-152">`[SapMonitorName <String>]`: nazwa zasobu monitorów SAP.</span><span class="sxs-lookup"><span data-stu-id="53c55-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="53c55-153">`[Scope <String>]`: zakres dostawcy zasobów dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="53c55-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="53c55-154">Zasób nadrzędny jest rozszerzany przez tożsamości zarządzane.</span><span class="sxs-lookup"><span data-stu-id="53c55-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="53c55-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="53c55-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="53c55-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="53c55-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="53c55-157">`[VaultName <String>]`: nazwa magazynu</span><span class="sxs-lookup"><span data-stu-id="53c55-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="53c55-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53c55-158">RELATED LINKS</span></span>

