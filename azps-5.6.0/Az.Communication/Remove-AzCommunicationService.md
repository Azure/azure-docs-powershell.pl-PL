---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: 3feb6e2246e2265c36e67d64621a5726eaabb6a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991600"
---
# <span data-ttu-id="94289-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="94289-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="94289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94289-102">SYNOPSIS</span></span>
<span data-ttu-id="94289-103">Operacja usunięcia usługi CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="94289-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="94289-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94289-104">SYNTAX</span></span>

### <span data-ttu-id="94289-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="94289-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="94289-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94289-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="94289-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="94289-107">DESCRIPTION</span></span>
<span data-ttu-id="94289-108">Operacja usunięcia usługi CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="94289-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="94289-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94289-109">EXAMPLES</span></span>

### <span data-ttu-id="94289-110">Przykład 1. Usuwanie określonego zasobu Azure Communication</span><span class="sxs-lookup"><span data-stu-id="94289-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="94289-111">Usuń/usuń zasób Azure Communication.</span><span class="sxs-lookup"><span data-stu-id="94289-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="94289-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94289-112">PARAMETERS</span></span>

### <span data-ttu-id="94289-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="94289-113">-AsJob</span></span>
<span data-ttu-id="94289-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="94289-114">Run the command as a job</span></span>

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

### <span data-ttu-id="94289-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94289-115">-DefaultProfile</span></span>
<span data-ttu-id="94289-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="94289-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94289-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94289-117">-InputObject</span></span>
<span data-ttu-id="94289-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="94289-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94289-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="94289-119">-Name</span></span>
<span data-ttu-id="94289-120">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="94289-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94289-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="94289-121">-NoWait</span></span>
<span data-ttu-id="94289-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="94289-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="94289-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94289-123">-PassThru</span></span>
<span data-ttu-id="94289-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="94289-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="94289-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94289-125">-ResourceGroupName</span></span>
<span data-ttu-id="94289-126">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="94289-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="94289-127">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="94289-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="94289-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94289-128">-SubscriptionId</span></span>
<span data-ttu-id="94289-129">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="94289-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="94289-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="94289-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="94289-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94289-131">-Confirm</span></span>
<span data-ttu-id="94289-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94289-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94289-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94289-133">-WhatIf</span></span>
<span data-ttu-id="94289-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94289-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94289-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94289-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94289-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94289-136">CommonParameters</span></span>
<span data-ttu-id="94289-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94289-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94289-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94289-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94289-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94289-139">INPUTS</span></span>

### <span data-ttu-id="94289-140">Microsoft.Azure.PowerShell.cmdlet.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="94289-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="94289-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94289-141">OUTPUTS</span></span>

### <span data-ttu-id="94289-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94289-142">System.Boolean</span></span>

## <span data-ttu-id="94289-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94289-143">NOTES</span></span>

<span data-ttu-id="94289-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="94289-144">ALIASES</span></span>

<span data-ttu-id="94289-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94289-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94289-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="94289-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94289-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="94289-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94289-148">INPUTOBJECT: <ICommunicationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="94289-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94289-149">`[CommunicationServiceName <String>]`: nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="94289-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="94289-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="94289-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94289-151">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="94289-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="94289-152">`[OperationId <String>]`: Identyfikator trwającej operacji synchronizacji</span><span class="sxs-lookup"><span data-stu-id="94289-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="94289-153">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="94289-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="94289-154">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="94289-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="94289-155">`[SubscriptionId <String>]`: Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="94289-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="94289-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="94289-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="94289-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94289-157">RELATED LINKS</span></span>

