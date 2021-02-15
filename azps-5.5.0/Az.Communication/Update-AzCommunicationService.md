---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 717c0981397ecbf419edbaa9f62bcc66443946fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238999"
---
# <span data-ttu-id="1f754-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="1f754-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="1f754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f754-102">SYNOPSIS</span></span>
<span data-ttu-id="1f754-103">Operacja aktualizacji istniejącej usługi CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="1f754-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="1f754-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1f754-104">SYNTAX</span></span>

### <span data-ttu-id="1f754-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="1f754-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1f754-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1f754-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1f754-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1f754-107">DESCRIPTION</span></span>
<span data-ttu-id="1f754-108">Operacja aktualizacji istniejącej usługi CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="1f754-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="1f754-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1f754-109">EXAMPLES</span></span>

### <span data-ttu-id="1f754-110">Przykład 1. Aktualizowanie istniejącego zasobu ACS w celu użycia tagów</span><span class="sxs-lookup"><span data-stu-id="1f754-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="1f754-111">Dołącza podane tagi do określonego zasobu ACS.</span><span class="sxs-lookup"><span data-stu-id="1f754-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="1f754-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f754-112">PARAMETERS</span></span>

### <span data-ttu-id="1f754-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f754-113">-DefaultProfile</span></span>
<span data-ttu-id="1f754-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f754-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f754-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f754-115">-InputObject</span></span>
<span data-ttu-id="1f754-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="1f754-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f754-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1f754-117">-Name</span></span>
<span data-ttu-id="1f754-118">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="1f754-118">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f754-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f754-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f754-120">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="1f754-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1f754-121">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="1f754-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1f754-122">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f754-122">-SubscriptionId</span></span>
<span data-ttu-id="1f754-123">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1f754-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1f754-124">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="1f754-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1f754-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="1f754-125">-Tag</span></span>
<span data-ttu-id="1f754-126">Tagi usługi, która jest listą kluczy par wartości opisujących zasób.</span><span class="sxs-lookup"><span data-stu-id="1f754-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="1f754-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f754-127">-Confirm</span></span>
<span data-ttu-id="1f754-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f754-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f754-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f754-129">-WhatIf</span></span>
<span data-ttu-id="1f754-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f754-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f754-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1f754-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f754-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f754-132">CommonParameters</span></span>
<span data-ttu-id="1f754-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f754-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f754-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f754-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f754-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f754-135">INPUTS</span></span>

### <span data-ttu-id="1f754-136">Microsoft.Azure.PowerShell.cmdlet.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="1f754-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="1f754-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f754-137">OUTPUTS</span></span>

### <span data-ttu-id="1f754-138">Microsoft.Azure.PowerShell.cmdlet.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="1f754-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="1f754-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1f754-139">NOTES</span></span>

<span data-ttu-id="1f754-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="1f754-140">ALIASES</span></span>

<span data-ttu-id="1f754-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="1f754-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1f754-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1f754-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f754-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1f754-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1f754-144">INPUTOBJECT: <ICommunicationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="1f754-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f754-145">`[CommunicationServiceName <String>]`: nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="1f754-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="1f754-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="1f754-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f754-147">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1f754-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="1f754-148">`[OperationId <String>]`: Identyfikator trwającej operacji synchronizacji</span><span class="sxs-lookup"><span data-stu-id="1f754-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="1f754-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="1f754-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1f754-150">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="1f754-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1f754-151">`[SubscriptionId <String>]`: Otrzymuje identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1f754-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="1f754-152">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="1f754-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1f754-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f754-153">RELATED LINKS</span></span>

