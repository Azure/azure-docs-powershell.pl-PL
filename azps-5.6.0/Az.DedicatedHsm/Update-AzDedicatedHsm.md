---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: ba005802294ef4fa1c890230230cbd44bc783216
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980746"
---
# <span data-ttu-id="efa19-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="efa19-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="efa19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efa19-102">SYNOPSIS</span></span>
<span data-ttu-id="efa19-103">Aktualizowanie dedykowanego modułu HSM w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="efa19-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="efa19-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="efa19-104">SYNTAX</span></span>

### <span data-ttu-id="efa19-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="efa19-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="efa19-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="efa19-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="efa19-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="efa19-107">DESCRIPTION</span></span>
<span data-ttu-id="efa19-108">Aktualizowanie dedykowanego modułu HSM w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="efa19-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="efa19-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="efa19-109">EXAMPLES</span></span>

### <span data-ttu-id="efa19-110">Przykład 1. Aktualizowanie tagu parametru Dedicated HSM według nazwy</span><span class="sxs-lookup"><span data-stu-id="efa19-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="efa19-111">To polecenie aktualizuje tag parametru Dedicated HSM według nazwy</span><span class="sxs-lookup"><span data-stu-id="efa19-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="efa19-112">Przykład 2. Aktualizowanie tagu parametru Dedicated HSM według obiektu</span><span class="sxs-lookup"><span data-stu-id="efa19-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="efa19-113">To polecenie aktualizuje tag parametru dedicated HSM według obiektu</span><span class="sxs-lookup"><span data-stu-id="efa19-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="efa19-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efa19-114">PARAMETERS</span></span>

### <span data-ttu-id="efa19-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="efa19-115">-AsJob</span></span>
<span data-ttu-id="efa19-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="efa19-116">Run the command as a job</span></span>

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

### <span data-ttu-id="efa19-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa19-117">-DefaultProfile</span></span>
<span data-ttu-id="efa19-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="efa19-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efa19-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efa19-119">-InputObject</span></span>
<span data-ttu-id="efa19-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="efa19-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efa19-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="efa19-121">-Name</span></span>
<span data-ttu-id="efa19-122">Nazwa dedykowanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="efa19-122">Name of the dedicated HSM</span></span>

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

### <span data-ttu-id="efa19-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="efa19-123">-NoWait</span></span>
<span data-ttu-id="efa19-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="efa19-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="efa19-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa19-125">-ResourceGroupName</span></span>
<span data-ttu-id="efa19-126">Nazwa grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="efa19-126">The name of the Resource Group to which the server belongs.</span></span>

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

### <span data-ttu-id="efa19-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="efa19-127">-SubscriptionId</span></span>
<span data-ttu-id="efa19-128">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="efa19-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="efa19-129">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="efa19-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="efa19-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="efa19-130">-Tag</span></span>
<span data-ttu-id="efa19-131">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="efa19-131">Resource tags</span></span>

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

### <span data-ttu-id="efa19-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="efa19-132">-Confirm</span></span>
<span data-ttu-id="efa19-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="efa19-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efa19-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa19-134">-WhatIf</span></span>
<span data-ttu-id="efa19-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efa19-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efa19-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="efa19-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efa19-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa19-137">CommonParameters</span></span>
<span data-ttu-id="efa19-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efa19-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa19-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efa19-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa19-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efa19-140">INPUTS</span></span>

### <span data-ttu-id="efa19-141">Microsoft.Azure.PowerShell.Cmdlet.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="efa19-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="efa19-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efa19-142">OUTPUTS</span></span>

### <span data-ttu-id="efa19-143">Microsoft.Azure.PowerShell.Cmdlet.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="efa19-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="efa19-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="efa19-144">NOTES</span></span>

<span data-ttu-id="efa19-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="efa19-145">ALIASES</span></span>

<span data-ttu-id="efa19-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="efa19-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="efa19-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="efa19-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="efa19-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="efa19-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="efa19-149">INPUTOBJECT: <IDedicatedHsmIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="efa19-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="efa19-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="efa19-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="efa19-151">`[Name <String>]`: nazwa dedykowanego hsm</span><span class="sxs-lookup"><span data-stu-id="efa19-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="efa19-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="efa19-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="efa19-153">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="efa19-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="efa19-154">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="efa19-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="efa19-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efa19-155">RELATED LINKS</span></span>

