---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/remove-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 5a29444c5f6d05ddbf614e86cd13af6818d24d79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956458"
---
# <span data-ttu-id="c9743-101">Remove-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="c9743-101">Remove-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="c9743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9743-102">SYNOPSIS</span></span>
<span data-ttu-id="c9743-103">Usuwa wystąpienia ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="c9743-103">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="c9743-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9743-104">SYNTAX</span></span>

### <span data-ttu-id="c9743-105">DeleteExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="c9743-105">DeleteExpanded (Default)</span></span>
```
Remove-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstance <String[]> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c9743-106">DeleteViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c9743-106">DeleteViaIdentityExpanded</span></span>
```
Remove-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c9743-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9743-107">DESCRIPTION</span></span>
<span data-ttu-id="c9743-108">Usuwa wystąpienia ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="c9743-108">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="c9743-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9743-109">EXAMPLES</span></span>

### <span data-ttu-id="c9743-110">Przykład 1. Usuwanie wystąpienia roli usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="c9743-110">Example 1: Remove a cloud service role instance</span></span>
```powershell
PS C:\> Remove-AzCloudServiceInstance -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="c9743-111">To polecenie usuwa wystąpienie roli o nazwie ContosoFrontEnd_IN_0 o nazwie ContosoCS, które należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="c9743-111">This command removes the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="c9743-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9743-112">PARAMETERS</span></span>

### <span data-ttu-id="c9743-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c9743-113">-AsJob</span></span>
<span data-ttu-id="c9743-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="c9743-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c9743-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="c9743-115">-CloudServiceName</span></span>
<span data-ttu-id="c9743-116">Nazwa usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="c9743-116">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9743-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9743-117">-DefaultProfile</span></span>
<span data-ttu-id="c9743-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9743-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9743-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9743-119">-InputObject</span></span>
<span data-ttu-id="c9743-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c9743-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: DeleteViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9743-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c9743-121">-NoWait</span></span>
<span data-ttu-id="c9743-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="c9743-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c9743-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9743-123">-PassThru</span></span>
<span data-ttu-id="c9743-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="c9743-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c9743-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9743-125">-ResourceGroupName</span></span>
<span data-ttu-id="c9743-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9743-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9743-127">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="c9743-127">-RoleInstance</span></span>
<span data-ttu-id="c9743-128">Lista nazw wystąpień ról usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="c9743-128">List of cloud service role instance names.</span></span>
<span data-ttu-id="c9743-129">Wartość "\*" oznacza wszystkie wystąpienia ról usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="c9743-129">Value of '\*' will signify all role instances of the cloud service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9743-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9743-130">-SubscriptionId</span></span>
<span data-ttu-id="c9743-131">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c9743-131">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c9743-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="c9743-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9743-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9743-133">-Confirm</span></span>
<span data-ttu-id="c9743-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9743-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9743-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9743-135">-WhatIf</span></span>
<span data-ttu-id="c9743-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9743-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9743-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c9743-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9743-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9743-138">CommonParameters</span></span>
<span data-ttu-id="c9743-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9743-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9743-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9743-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9743-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9743-141">INPUTS</span></span>

### <span data-ttu-id="c9743-142">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="c9743-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="c9743-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9743-143">OUTPUTS</span></span>

### <span data-ttu-id="c9743-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c9743-144">System.Boolean</span></span>

## <span data-ttu-id="c9743-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9743-145">NOTES</span></span>

<span data-ttu-id="c9743-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c9743-146">ALIASES</span></span>

<span data-ttu-id="c9743-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9743-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c9743-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c9743-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9743-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c9743-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c9743-150">INPUTOBJECT: <ICloudServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="c9743-150">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c9743-151">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="c9743-151">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="c9743-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c9743-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c9743-153">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="c9743-153">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="c9743-154">`[RoleInstanceName <String>]`: nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="c9743-154">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="c9743-155">`[RoleName <String>]`: nazwa roli.</span><span class="sxs-lookup"><span data-stu-id="c9743-155">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="c9743-156">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c9743-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c9743-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="c9743-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c9743-158">`[UpdateDomain <Int32?>]`: określa wartość całkowitą identyfikującą domenę aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="c9743-158">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="c9743-159">Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.</span><span class="sxs-lookup"><span data-stu-id="c9743-159">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="c9743-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9743-160">RELATED LINKS</span></span>

