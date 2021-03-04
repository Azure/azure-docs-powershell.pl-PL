---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: 777c02f6588d7c1fdb1a1d6e9e9c004f51694293
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012369"
---
# <span data-ttu-id="aa340-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="aa340-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="aa340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa340-102">SYNOPSIS</span></span>
<span data-ttu-id="aa340-103">Operacja usunięcia rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="aa340-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="aa340-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aa340-104">SYNTAX</span></span>

### <span data-ttu-id="aa340-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="aa340-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="aa340-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aa340-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aa340-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="aa340-107">DESCRIPTION</span></span>
<span data-ttu-id="aa340-108">Operacja usunięcia rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="aa340-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="aa340-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aa340-109">EXAMPLES</span></span>

### <span data-ttu-id="aa340-110">Przykład 1. Usuwanie rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="aa340-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="aa340-111">Usuwa rozszerzenie na komputerze.</span><span class="sxs-lookup"><span data-stu-id="aa340-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="aa340-112">Przykład 2. Usuwanie rozszerzenia za pośrednictwem potoku</span><span class="sxs-lookup"><span data-stu-id="aa340-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="aa340-113">Usuwa wszystkie rozszerzenia na określonym komputerze.</span><span class="sxs-lookup"><span data-stu-id="aa340-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="aa340-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa340-114">PARAMETERS</span></span>

### <span data-ttu-id="aa340-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="aa340-115">-AsJob</span></span>
<span data-ttu-id="aa340-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="aa340-116">Run the command as a job</span></span>

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

### <span data-ttu-id="aa340-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa340-117">-DefaultProfile</span></span>
<span data-ttu-id="aa340-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa340-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa340-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa340-119">-InputObject</span></span>
<span data-ttu-id="aa340-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="aa340-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aa340-121">— Nazwa_komputera</span><span class="sxs-lookup"><span data-stu-id="aa340-121">-MachineName</span></span>
<span data-ttu-id="aa340-122">Nazwa komputera, na którym rozszerzenie powinno zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="aa340-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="aa340-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="aa340-123">-Name</span></span>
<span data-ttu-id="aa340-124">Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="aa340-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="aa340-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aa340-125">-NoWait</span></span>
<span data-ttu-id="aa340-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="aa340-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aa340-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa340-127">-PassThru</span></span>
<span data-ttu-id="aa340-128">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="aa340-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="aa340-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa340-129">-ResourceGroupName</span></span>
<span data-ttu-id="aa340-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa340-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="aa340-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa340-131">-SubscriptionId</span></span>
<span data-ttu-id="aa340-132">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aa340-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aa340-133">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="aa340-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aa340-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa340-134">-Confirm</span></span>
<span data-ttu-id="aa340-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aa340-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa340-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa340-136">-WhatIf</span></span>
<span data-ttu-id="aa340-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa340-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa340-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="aa340-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa340-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa340-139">CommonParameters</span></span>
<span data-ttu-id="aa340-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa340-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa340-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa340-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa340-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa340-142">INPUTS</span></span>

### <span data-ttu-id="aa340-143">Microsoft.Azure.PowerShell.cmdlet.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="aa340-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="aa340-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa340-144">OUTPUTS</span></span>

### <span data-ttu-id="aa340-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa340-145">System.Boolean</span></span>

## <span data-ttu-id="aa340-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aa340-146">NOTES</span></span>

<span data-ttu-id="aa340-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="aa340-147">ALIASES</span></span>

<span data-ttu-id="aa340-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa340-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aa340-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="aa340-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa340-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aa340-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aa340-151">INPUTOBJECT: <IConnectedMachineIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="aa340-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aa340-152">`[ExtensionName <String>]`: nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="aa340-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="aa340-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="aa340-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aa340-154">`[Name <String>]`: nazwa komputera hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="aa340-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="aa340-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa340-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="aa340-156">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aa340-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="aa340-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="aa340-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="aa340-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa340-158">RELATED LINKS</span></span>

