---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 0f124d818b95928f12cdc71f60c436f5691f8151
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998733"
---
# <span data-ttu-id="d7e12-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="d7e12-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="d7e12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7e12-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e12-103">Aktualizuje istniejącego niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7e12-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="d7e12-104">Jedyną wartością, która może być obecnie aktualizowana za pośrednictwem poprawki, są tagi.</span><span class="sxs-lookup"><span data-stu-id="d7e12-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="d7e12-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d7e12-105">SYNTAX</span></span>

### <span data-ttu-id="d7e12-106">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="d7e12-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7e12-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d7e12-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d7e12-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d7e12-108">DESCRIPTION</span></span>
<span data-ttu-id="d7e12-109">Aktualizuje istniejącego niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7e12-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="d7e12-110">Jedyną wartością, która może być obecnie aktualizowana za pośrednictwem poprawki, są tagi.</span><span class="sxs-lookup"><span data-stu-id="d7e12-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="d7e12-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d7e12-111">EXAMPLES</span></span>

### <span data-ttu-id="d7e12-112">Przykład 1. Dodawanie tagów do dostawcy niestandardowego</span><span class="sxs-lookup"><span data-stu-id="d7e12-112">Example 1: Add Tags to a custom Provider</span></span>
```powershell
PS C:\> Update-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -Tag @{MyTag="MyValue"} | Format-List

Action            :
Id                : /subscriptions/xxxxx-yyyyy-xxxx-yyyy/resourceGroups/mc-cp01/providers/Microsoft.CustomProviders/resourceproviders/Namespace.Type
Location          : West US 2
Name              : Namespace.Type
ProvisioningState : Succeeded
ResourceType      : {CustomRoute1, associations}
Tag               : Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ResourceTags
Type              : Microsoft.CustomProviders/resourceproviders
Validation        :
```

<span data-ttu-id="d7e12-113">Aktualizowanie tagów dostawcy niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="d7e12-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="d7e12-114">Przykład 2. Aktualizowanie dostawcy niestandardowego za pomocą rur</span><span class="sxs-lookup"><span data-stu-id="d7e12-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="d7e12-115">Aktualizowanie dostawcy niestandardowego za pomocą rur.</span><span class="sxs-lookup"><span data-stu-id="d7e12-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="d7e12-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7e12-116">PARAMETERS</span></span>

### <span data-ttu-id="d7e12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e12-117">-DefaultProfile</span></span>
<span data-ttu-id="d7e12-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7e12-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7e12-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7e12-119">-InputObject</span></span>
<span data-ttu-id="d7e12-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d7e12-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e12-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d7e12-121">-Name</span></span>
<span data-ttu-id="d7e12-122">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7e12-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e12-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7e12-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7e12-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7e12-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="d7e12-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7e12-125">-SubscriptionId</span></span>
<span data-ttu-id="d7e12-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d7e12-126">The Azure subscription ID.</span></span>
<span data-ttu-id="d7e12-127">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="d7e12-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="d7e12-128">— Tag</span><span class="sxs-lookup"><span data-stu-id="d7e12-128">-Tag</span></span>
<span data-ttu-id="d7e12-129">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="d7e12-129">Resource tags</span></span>

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

### <span data-ttu-id="d7e12-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7e12-130">-Confirm</span></span>
<span data-ttu-id="d7e12-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d7e12-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7e12-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7e12-132">-WhatIf</span></span>
<span data-ttu-id="d7e12-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7e12-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7e12-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d7e12-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7e12-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e12-135">CommonParameters</span></span>
<span data-ttu-id="d7e12-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7e12-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e12-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7e12-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e12-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7e12-138">INPUTS</span></span>

### <span data-ttu-id="d7e12-139">Microsoft.Azure.PowerShell.Cmdlet.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="d7e12-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="d7e12-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7e12-140">OUTPUTS</span></span>

### <span data-ttu-id="d7e12-141">Microsoft.Azure.PowerShell.cmdlet.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="d7e12-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="d7e12-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d7e12-142">NOTES</span></span>

<span data-ttu-id="d7e12-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d7e12-143">ALIASES</span></span>

<span data-ttu-id="d7e12-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7e12-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7e12-145">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d7e12-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7e12-146">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d7e12-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7e12-147">INPUTOBJECT: <ICustomProvidersIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d7e12-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d7e12-148">`[AssociationName <String>]`: nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="d7e12-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="d7e12-149">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d7e12-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d7e12-150">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7e12-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d7e12-151">`[ResourceProviderName <String>]`: nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7e12-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="d7e12-152">`[Scope <String>]`: zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="d7e12-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="d7e12-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d7e12-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="d7e12-154">Jest to ciąg w formacie IDENTYFIKATORA GUID (np. 000000000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="d7e12-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="d7e12-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7e12-155">RELATED LINKS</span></span>

