---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: 0f9369e3ad2427fc633239b9775f485db01e87b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962177"
---
# <span data-ttu-id="1bfa3-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="1bfa3-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="1bfa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bfa3-102">SYNOPSIS</span></span>
<span data-ttu-id="1bfa3-103">Usuwa określony moduł HSM dedykowany platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="1bfa3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1bfa3-104">SYNTAX</span></span>

### <span data-ttu-id="1bfa3-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="1bfa3-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1bfa3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1bfa3-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1bfa3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1bfa3-107">DESCRIPTION</span></span>
<span data-ttu-id="1bfa3-108">Usuwa określony moduł HSM dedykowany platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="1bfa3-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1bfa3-109">EXAMPLES</span></span>

### <span data-ttu-id="1bfa3-110">Przykład 1. Usunięcie dedykowanego modułu HSM według nazwy</span><span class="sxs-lookup"><span data-stu-id="1bfa3-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="1bfa3-111">Ten commnad usuwa moduł zabezpieczeń sprzętu (HSM) według nazwy.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="1bfa3-112">Przykład 2. Usuwanie dedykowanego modułu HSM według obiektu</span><span class="sxs-lookup"><span data-stu-id="1bfa3-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="1bfa3-113">Ten commnad usuwa dedykowany moduł HSM według obiektu.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="1bfa3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bfa3-114">PARAMETERS</span></span>

### <span data-ttu-id="1bfa3-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1bfa3-115">-AsJob</span></span>
<span data-ttu-id="1bfa3-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="1bfa3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1bfa3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bfa3-117">-DefaultProfile</span></span>
<span data-ttu-id="1bfa3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bfa3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bfa3-119">-InputObject</span></span>
<span data-ttu-id="1bfa3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bfa3-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1bfa3-121">-Name</span></span>
<span data-ttu-id="1bfa3-122">Nazwa dedykowanego modułu HSM do usunięcia</span><span class="sxs-lookup"><span data-stu-id="1bfa3-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="1bfa3-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1bfa3-123">-NoWait</span></span>
<span data-ttu-id="1bfa3-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="1bfa3-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1bfa3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bfa3-125">-PassThru</span></span>
<span data-ttu-id="1bfa3-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1bfa3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bfa3-127">-ResourceGroupName</span></span>
<span data-ttu-id="1bfa3-128">Nazwa grupy zasobów, do której należy dedykowany moduł HSM.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="1bfa3-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1bfa3-129">-SubscriptionId</span></span>
<span data-ttu-id="1bfa3-130">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1bfa3-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1bfa3-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1bfa3-132">-Confirm</span></span>
<span data-ttu-id="1bfa3-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bfa3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bfa3-134">-WhatIf</span></span>
<span data-ttu-id="1bfa3-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bfa3-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bfa3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bfa3-137">CommonParameters</span></span>
<span data-ttu-id="1bfa3-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bfa3-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bfa3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bfa3-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1bfa3-140">INPUTS</span></span>

### <span data-ttu-id="1bfa3-141">Microsoft.Azure.PowerShell.Cmdlet.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="1bfa3-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="1bfa3-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1bfa3-142">OUTPUTS</span></span>

### <span data-ttu-id="1bfa3-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1bfa3-143">System.Boolean</span></span>

## <span data-ttu-id="1bfa3-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1bfa3-144">NOTES</span></span>

<span data-ttu-id="1bfa3-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="1bfa3-145">ALIASES</span></span>

<span data-ttu-id="1bfa3-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1bfa3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1bfa3-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1bfa3-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1bfa3-149">INPUTOBJECT: <IDedicatedHsmIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="1bfa3-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1bfa3-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="1bfa3-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1bfa3-151">`[Name <String>]`: nazwa dedykowanego hsm</span><span class="sxs-lookup"><span data-stu-id="1bfa3-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="1bfa3-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="1bfa3-153">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1bfa3-154">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="1bfa3-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1bfa3-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1bfa3-155">RELATED LINKS</span></span>

