---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: b9b9c746390df42a678177a506ffc6cd398af03e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181147"
---
# <span data-ttu-id="945a7-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="945a7-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="945a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="945a7-102">SYNOPSIS</span></span>
<span data-ttu-id="945a7-103">Usuwa niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="945a7-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="945a7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="945a7-104">SYNTAX</span></span>

### <span data-ttu-id="945a7-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="945a7-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="945a7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="945a7-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="945a7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="945a7-107">DESCRIPTION</span></span>
<span data-ttu-id="945a7-108">Usuwa niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="945a7-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="945a7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="945a7-109">EXAMPLES</span></span>

### <span data-ttu-id="945a7-110">Przykład 1. Usuwanie dostawcy niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="945a7-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="945a7-111">Usuwanie dostawcy niestandardowego</span><span class="sxs-lookup"><span data-stu-id="945a7-111">Remove a custom provider</span></span>

### <span data-ttu-id="945a7-112">Przykład 2. Usuwanie dostawcy niestandardowego za pomocą passthru</span><span class="sxs-lookup"><span data-stu-id="945a7-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="945a7-113">Usuwanie dostawcy niestandardowego za pomocą funkcji PassThru w celu wskazania sukcesu lub niepowodzenia.</span><span class="sxs-lookup"><span data-stu-id="945a7-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="945a7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="945a7-114">PARAMETERS</span></span>

### <span data-ttu-id="945a7-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="945a7-115">-AsJob</span></span>
<span data-ttu-id="945a7-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="945a7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="945a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="945a7-117">-DefaultProfile</span></span>
<span data-ttu-id="945a7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="945a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="945a7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="945a7-119">-InputObject</span></span>
<span data-ttu-id="945a7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="945a7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="945a7-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="945a7-121">-Name</span></span>
<span data-ttu-id="945a7-122">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="945a7-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="945a7-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="945a7-123">-NoWait</span></span>
<span data-ttu-id="945a7-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="945a7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="945a7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="945a7-125">-PassThru</span></span>
<span data-ttu-id="945a7-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="945a7-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="945a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="945a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="945a7-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="945a7-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="945a7-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="945a7-129">-SubscriptionId</span></span>
<span data-ttu-id="945a7-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="945a7-130">The Azure subscription ID.</span></span>
<span data-ttu-id="945a7-131">Jest to ciąg w formacie GUID (np. 000000000-0000-0000-0000-0000000000000)</span><span class="sxs-lookup"><span data-stu-id="945a7-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="945a7-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="945a7-132">-Confirm</span></span>
<span data-ttu-id="945a7-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="945a7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="945a7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="945a7-134">-WhatIf</span></span>
<span data-ttu-id="945a7-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="945a7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="945a7-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="945a7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="945a7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="945a7-137">CommonParameters</span></span>
<span data-ttu-id="945a7-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="945a7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="945a7-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="945a7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="945a7-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="945a7-140">INPUTS</span></span>

### <span data-ttu-id="945a7-141">Microsoft.Azure.PowerShell.Cmdlet.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="945a7-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="945a7-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="945a7-142">OUTPUTS</span></span>

### <span data-ttu-id="945a7-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="945a7-143">System.Boolean</span></span>

## <span data-ttu-id="945a7-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="945a7-144">NOTES</span></span>

<span data-ttu-id="945a7-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="945a7-145">ALIASES</span></span>

<span data-ttu-id="945a7-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="945a7-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="945a7-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="945a7-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="945a7-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="945a7-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="945a7-149">INPUTOBJECT: <ICustomProvidersIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="945a7-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="945a7-150">`[AssociationName <String>]`: nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="945a7-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="945a7-151">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="945a7-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="945a7-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="945a7-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="945a7-153">`[ResourceProviderName <String>]`: nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="945a7-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="945a7-154">`[Scope <String>]`: zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="945a7-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="945a7-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="945a7-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="945a7-156">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="945a7-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="945a7-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="945a7-157">RELATED LINKS</span></span>

