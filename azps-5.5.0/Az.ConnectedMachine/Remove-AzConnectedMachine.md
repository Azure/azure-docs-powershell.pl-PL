---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243979"
---
# <span data-ttu-id="095a1-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="095a1-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="095a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="095a1-102">SYNOPSIS</span></span>
<span data-ttu-id="095a1-103">Operacja usunięcia hybrydowej tożsamości komputera na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="095a1-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="095a1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="095a1-104">SYNTAX</span></span>

### <span data-ttu-id="095a1-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="095a1-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="095a1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="095a1-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="095a1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="095a1-107">DESCRIPTION</span></span>
<span data-ttu-id="095a1-108">Operacja usunięcia hybrydowej tożsamości komputera na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="095a1-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="095a1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="095a1-109">EXAMPLES</span></span>

### <span data-ttu-id="095a1-110">Przykład 1. Usuwanie połączonego komputera</span><span class="sxs-lookup"><span data-stu-id="095a1-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="095a1-111">Usuwa połączony komputer.</span><span class="sxs-lookup"><span data-stu-id="095a1-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="095a1-112">Przykład 2. Usuwanie połączonych komputerów za pośrednictwem potoku</span><span class="sxs-lookup"><span data-stu-id="095a1-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="095a1-113">Usuwa wszystkie komputery z `contoso-connected-machines` grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="095a1-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="095a1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="095a1-114">PARAMETERS</span></span>

### <span data-ttu-id="095a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095a1-115">-DefaultProfile</span></span>
<span data-ttu-id="095a1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="095a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="095a1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="095a1-117">-InputObject</span></span>
<span data-ttu-id="095a1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="095a1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="095a1-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="095a1-119">-Name</span></span>
<span data-ttu-id="095a1-120">Nazwa komputera hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="095a1-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="095a1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="095a1-121">-PassThru</span></span>
<span data-ttu-id="095a1-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="095a1-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="095a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="095a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="095a1-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="095a1-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="095a1-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="095a1-125">-SubscriptionId</span></span>
<span data-ttu-id="095a1-126">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="095a1-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="095a1-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="095a1-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="095a1-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="095a1-128">-Confirm</span></span>
<span data-ttu-id="095a1-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="095a1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="095a1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="095a1-130">-WhatIf</span></span>
<span data-ttu-id="095a1-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="095a1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="095a1-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="095a1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="095a1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095a1-133">CommonParameters</span></span>
<span data-ttu-id="095a1-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095a1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095a1-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="095a1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095a1-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="095a1-136">INPUTS</span></span>

### <span data-ttu-id="095a1-137">Microsoft.Azure.PowerShell.cmdlet.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="095a1-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="095a1-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="095a1-138">OUTPUTS</span></span>

### <span data-ttu-id="095a1-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="095a1-139">System.Boolean</span></span>

## <span data-ttu-id="095a1-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="095a1-140">NOTES</span></span>

<span data-ttu-id="095a1-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="095a1-141">ALIASES</span></span>

<span data-ttu-id="095a1-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="095a1-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="095a1-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="095a1-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="095a1-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="095a1-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="095a1-145">INPUTOBJECT: <IConnectedMachineIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="095a1-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="095a1-146">`[ExtensionName <String>]`: nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="095a1-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="095a1-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="095a1-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="095a1-148">`[Name <String>]`: nazwa komputera hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="095a1-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="095a1-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="095a1-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="095a1-150">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="095a1-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="095a1-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="095a1-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="095a1-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="095a1-152">RELATED LINKS</span></span>

