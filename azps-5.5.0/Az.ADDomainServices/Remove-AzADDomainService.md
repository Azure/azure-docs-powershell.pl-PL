---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/remove-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
ms.openlocfilehash: f29fbbdd805abb9891f707ed983bcf8aebefc46c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176587"
---
# <span data-ttu-id="d72cd-101">Remove-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="d72cd-101">Remove-AzADDomainService</span></span>

## <span data-ttu-id="d72cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d72cd-102">SYNOPSIS</span></span>
<span data-ttu-id="d72cd-103">Operacja Usuń usługę domeny powoduje usunięcie istniejącej usługi domeny.</span><span class="sxs-lookup"><span data-stu-id="d72cd-103">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="d72cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d72cd-104">SYNTAX</span></span>

### <span data-ttu-id="d72cd-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="d72cd-105">Delete (Default)</span></span>
```
Remove-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d72cd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d72cd-106">DeleteViaIdentity</span></span>
```
Remove-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d72cd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d72cd-107">DESCRIPTION</span></span>
<span data-ttu-id="d72cd-108">Operacja Usuń usługę domeny usuwa istniejącą usługę domeny.</span><span class="sxs-lookup"><span data-stu-id="d72cd-108">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="d72cd-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d72cd-109">EXAMPLES</span></span>

### <span data-ttu-id="d72cd-110">Przykład 1. Usunięcie domeny AzADDomain według pola ResourceGroupName i Name</span><span class="sxs-lookup"><span data-stu-id="d72cd-110">Example 1: Delete the AzADDomain by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName

```

<span data-ttu-id="d72cd-111">Usuwanie domeny AzADDomain za pomocą pola ResourceGroupName i Name</span><span class="sxs-lookup"><span data-stu-id="d72cd-111">Delete the AzADDomain by ResourceGroupName and Name</span></span>

### <span data-ttu-id="d72cd-112">Przykład 2. Usuwanie domeny AzADDomain przez InputObject</span><span class="sxs-lookup"><span data-stu-id="d72cd-112">Example 2: Delete the AzADDomain by InputObject</span></span>
```powershell
PS C:\> $GetADDomainExample = Get-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName
Remove-AzADDomainService -InputObject $GetADDomainExample

```

<span data-ttu-id="d72cd-113">Usuwanie domeny AzADDomain przez InputObject</span><span class="sxs-lookup"><span data-stu-id="d72cd-113">Delete the AzADDomain by InputObject</span></span>

## <span data-ttu-id="d72cd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d72cd-114">PARAMETERS</span></span>

### <span data-ttu-id="d72cd-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d72cd-115">-AsJob</span></span>
<span data-ttu-id="d72cd-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="d72cd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d72cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72cd-117">-DefaultProfile</span></span>
<span data-ttu-id="d72cd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d72cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d72cd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d72cd-119">-InputObject</span></span>
<span data-ttu-id="d72cd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d72cd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d72cd-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d72cd-121">-Name</span></span>
<span data-ttu-id="d72cd-122">Nazwa usługi domeny.</span><span class="sxs-lookup"><span data-stu-id="d72cd-122">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72cd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d72cd-123">-NoWait</span></span>
<span data-ttu-id="d72cd-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="d72cd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d72cd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d72cd-125">-PassThru</span></span>
<span data-ttu-id="d72cd-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d72cd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d72cd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d72cd-127">-ResourceGroupName</span></span>
<span data-ttu-id="d72cd-128">Nazwa grupy zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d72cd-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="d72cd-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="d72cd-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d72cd-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d72cd-130">-SubscriptionId</span></span>
<span data-ttu-id="d72cd-131">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d72cd-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d72cd-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d72cd-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d72cd-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d72cd-133">-Confirm</span></span>
<span data-ttu-id="d72cd-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d72cd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d72cd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d72cd-135">-WhatIf</span></span>
<span data-ttu-id="d72cd-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d72cd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d72cd-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d72cd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d72cd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72cd-138">CommonParameters</span></span>
<span data-ttu-id="d72cd-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d72cd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72cd-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d72cd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72cd-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d72cd-141">INPUTS</span></span>

### <span data-ttu-id="d72cd-142">Microsoft.Azure.PowerShell.Cmdlet.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="d72cd-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="d72cd-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d72cd-143">OUTPUTS</span></span>

### <span data-ttu-id="d72cd-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d72cd-144">System.Boolean</span></span>

## <span data-ttu-id="d72cd-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d72cd-145">NOTES</span></span>

<span data-ttu-id="d72cd-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d72cd-146">ALIASES</span></span>

<span data-ttu-id="d72cd-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d72cd-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d72cd-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d72cd-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d72cd-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d72cd-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d72cd-150">INPUTOBJECT: <IAdDomainServicesIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d72cd-150">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d72cd-151">`[DomainServiceName <String>]`: nazwa usługi domeny.</span><span class="sxs-lookup"><span data-stu-id="d72cd-151">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="d72cd-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d72cd-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d72cd-153">`[ResourceGroupName <String>]`: nazwa grupy zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d72cd-153">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="d72cd-154">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="d72cd-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="d72cd-155">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d72cd-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d72cd-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d72cd-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d72cd-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d72cd-157">RELATED LINKS</span></span>

