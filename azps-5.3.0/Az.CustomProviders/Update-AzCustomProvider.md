---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503752"
---
# <span data-ttu-id="6bcb8-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="6bcb8-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="6bcb8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6bcb8-102">SYNOPSIS</span></span>
<span data-ttu-id="6bcb8-103">Aktualizuje istniejącego niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="6bcb8-104">Jedyną wartością, którą można zaktualizować za pośrednictwem poprawki, są obecnie Tagi.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="6bcb8-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6bcb8-105">SYNTAX</span></span>

### <span data-ttu-id="6bcb8-106">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6bcb8-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6bcb8-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6bcb8-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6bcb8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6bcb8-108">DESCRIPTION</span></span>
<span data-ttu-id="6bcb8-109">Aktualizuje istniejącego niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="6bcb8-110">Jedyną wartością, którą można zaktualizować za pośrednictwem poprawki, są obecnie Tagi.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="6bcb8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6bcb8-111">EXAMPLES</span></span>

### <span data-ttu-id="6bcb8-112">Przykład 1: Dodawanie znaczników do dostawcy niestandardowego</span><span class="sxs-lookup"><span data-stu-id="6bcb8-112">Example 1: Add Tags to a custom Provider</span></span>
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

<span data-ttu-id="6bcb8-113">Zaktualizuj znaczniki dostawcy niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="6bcb8-114">Przykład 2: aktualizowanie dostawcy niestandardowego przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="6bcb8-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="6bcb8-115">Zaktualizuj dostawcę niestandardowego przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="6bcb8-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6bcb8-116">PARAMETERS</span></span>

### <span data-ttu-id="6bcb8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bcb8-117">-DefaultProfile</span></span>
<span data-ttu-id="6bcb8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bcb8-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6bcb8-119">-InputObject</span></span>
<span data-ttu-id="6bcb8-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6bcb8-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6bcb8-121">-Name</span></span>
<span data-ttu-id="6bcb8-122">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="6bcb8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bcb8-123">-ResourceGroupName</span></span>
<span data-ttu-id="6bcb8-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="6bcb8-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6bcb8-125">-SubscriptionId</span></span>
<span data-ttu-id="6bcb8-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-126">The Azure subscription ID.</span></span>
<span data-ttu-id="6bcb8-127">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="6bcb8-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="6bcb8-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="6bcb8-128">-Tag</span></span>
<span data-ttu-id="6bcb8-129">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="6bcb8-129">Resource tags</span></span>

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

### <span data-ttu-id="6bcb8-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6bcb8-130">-Confirm</span></span>
<span data-ttu-id="6bcb8-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bcb8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bcb8-132">-WhatIf</span></span>
<span data-ttu-id="6bcb8-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bcb8-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bcb8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bcb8-135">CommonParameters</span></span>
<span data-ttu-id="6bcb8-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bcb8-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bcb8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bcb8-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bcb8-138">INPUTS</span></span>

### <span data-ttu-id="6bcb8-139">Microsoft. Azure. PowerShell. polecenia. CustomProviders. models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="6bcb8-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="6bcb8-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6bcb8-140">OUTPUTS</span></span>

### <span data-ttu-id="6bcb8-141">Microsoft. Azure. PowerShell. polecenia. CustomProviders. models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="6bcb8-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="6bcb8-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6bcb8-142">NOTES</span></span>

<span data-ttu-id="6bcb8-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6bcb8-143">ALIASES</span></span>

<span data-ttu-id="6bcb8-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6bcb8-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6bcb8-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6bcb8-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6bcb8-147">INPUTobject <ICustomProvidersIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="6bcb8-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6bcb8-148">`[AssociationName <String>]`: Nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="6bcb8-149">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6bcb8-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6bcb8-150">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6bcb8-151">`[ResourceProviderName <String>]`: Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="6bcb8-152">`[Scope <String>]`: Zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="6bcb8-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6bcb8-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="6bcb8-154">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="6bcb8-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="6bcb8-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bcb8-155">RELATED LINKS</span></span>

