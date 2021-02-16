---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: c165f9d69b18631f53bdc9444a623f43599532fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177794"
---
# <span data-ttu-id="3a279-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="3a279-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="3a279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a279-102">SYNOPSIS</span></span>
<span data-ttu-id="3a279-103">Operacja usunięcia usługi CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3a279-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="3a279-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3a279-104">SYNTAX</span></span>

### <span data-ttu-id="3a279-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="3a279-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3a279-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3a279-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3a279-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3a279-107">DESCRIPTION</span></span>
<span data-ttu-id="3a279-108">Operacja usunięcia usługi CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3a279-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="3a279-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3a279-109">EXAMPLES</span></span>

### <span data-ttu-id="3a279-110">Przykład 1. Usunięcie określonego zasobu Azure Communication</span><span class="sxs-lookup"><span data-stu-id="3a279-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="3a279-111">Usuń/usuń zasób Azure Communication.</span><span class="sxs-lookup"><span data-stu-id="3a279-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="3a279-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a279-112">PARAMETERS</span></span>

### <span data-ttu-id="3a279-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3a279-113">-AsJob</span></span>
<span data-ttu-id="3a279-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="3a279-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3a279-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a279-115">-DefaultProfile</span></span>
<span data-ttu-id="3a279-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a279-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a279-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a279-117">-InputObject</span></span>
<span data-ttu-id="3a279-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3a279-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a279-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3a279-119">-Name</span></span>
<span data-ttu-id="3a279-120">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3a279-120">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="3a279-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3a279-121">-NoWait</span></span>
<span data-ttu-id="3a279-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="3a279-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3a279-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a279-123">-PassThru</span></span>
<span data-ttu-id="3a279-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="3a279-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3a279-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a279-125">-ResourceGroupName</span></span>
<span data-ttu-id="3a279-126">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="3a279-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3a279-127">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="3a279-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3a279-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a279-128">-SubscriptionId</span></span>
<span data-ttu-id="3a279-129">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a279-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3a279-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="3a279-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3a279-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a279-131">-Confirm</span></span>
<span data-ttu-id="3a279-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3a279-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a279-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a279-133">-WhatIf</span></span>
<span data-ttu-id="3a279-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a279-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a279-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3a279-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a279-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a279-136">CommonParameters</span></span>
<span data-ttu-id="3a279-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a279-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a279-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a279-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a279-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a279-139">INPUTS</span></span>

### <span data-ttu-id="3a279-140">Microsoft.Azure.PowerShell.Cmdlet.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="3a279-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="3a279-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a279-141">OUTPUTS</span></span>

### <span data-ttu-id="3a279-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a279-142">System.Boolean</span></span>

## <span data-ttu-id="3a279-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3a279-143">NOTES</span></span>

<span data-ttu-id="3a279-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="3a279-144">ALIASES</span></span>

<span data-ttu-id="3a279-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="3a279-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3a279-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3a279-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a279-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3a279-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3a279-148">INPUTOBJECT: <ICommunicationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="3a279-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a279-149">`[CommunicationServiceName <String>]`: nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3a279-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="3a279-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3a279-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a279-151">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3a279-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="3a279-152">`[OperationId <String>]`: Identyfikator trwającej operacji synchronizacji</span><span class="sxs-lookup"><span data-stu-id="3a279-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="3a279-153">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="3a279-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3a279-154">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="3a279-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3a279-155">`[SubscriptionId <String>]`: Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a279-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="3a279-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="3a279-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3a279-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a279-157">RELATED LINKS</span></span>

