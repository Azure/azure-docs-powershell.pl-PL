---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 7139831accd920858e7b97f775146d01b91cef3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972538"
---
# <span data-ttu-id="7f4e1-101">Set-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="7f4e1-101">Set-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="7f4e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f4e1-102">SYNOPSIS</span></span>
<span data-ttu-id="7f4e1-103">Zaktualizuj udostępniony zasób linków prywatnych dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="7f4e1-103">Update the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="7f4e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7f4e1-104">SYNTAX</span></span>

### <span data-ttu-id="7f4e1-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7f4e1-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -RequestMessage <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4e1-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f4e1-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> -RequestMessage <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f4e1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f4e1-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceId] <String> -RequestMessage <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f4e1-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f4e1-108">InputObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -RequestMessage <String> -InputObject <PSSharedPrivateLinkResource>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f4e1-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="7f4e1-109">DESCRIPTION</span></span>
<span data-ttu-id="7f4e1-110">Ten **plik Set-AzSearchSharedPrivateLinkResource aktualizuje** udostępniony zasób linków prywatnych dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="7f4e1-110">This **Set-AzSearchSharedPrivateLinkResource** updates the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="7f4e1-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7f4e1-111">EXAMPLES</span></span>

### <span data-ttu-id="7f4e1-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f4e1-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -RequestMessage "Please kindly approve"


Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please kindly approve
ResourceRegion        :
```

<span data-ttu-id="7f4e1-113">W tym przykładzie jest aktualizowany komunikat żądania dla oczekującego udostępnionego zasobu prywatnego linku dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="7f4e1-113">This example updates the request message for the pending shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="7f4e1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f4e1-114">PARAMETERS</span></span>

### <span data-ttu-id="7f4e1-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7f4e1-115">-AsJob</span></span>
<span data-ttu-id="7f4e1-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7f4e1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f4e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f4e1-117">-DefaultProfile</span></span>
<span data-ttu-id="7f4e1-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f4e1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f4e1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f4e1-119">-InputObject</span></span>
<span data-ttu-id="7f4e1-120">Udostępniony obiekt wejściowy zasobu prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="7f4e1-120">Shared private link resource input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4e1-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7f4e1-121">-Name</span></span>
<span data-ttu-id="7f4e1-122">Azure Cognitive Search Shared private link resource</span><span class="sxs-lookup"><span data-stu-id="7f4e1-122">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f4e1-123">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="7f4e1-123">-ParentObject</span></span>
<span data-ttu-id="7f4e1-124">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="7f4e1-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4e1-125">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="7f4e1-125">-RequestMessage</span></span>
<span data-ttu-id="7f4e1-126">Udostępniony komunikat o żądaniu prywatnego zasobu linku</span><span class="sxs-lookup"><span data-stu-id="7f4e1-126">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f4e1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f4e1-127">-ResourceGroupName</span></span>
<span data-ttu-id="7f4e1-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f4e1-128">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f4e1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f4e1-129">-ResourceId</span></span>
<span data-ttu-id="7f4e1-130">Udostępniony identyfikator zasobu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="7f4e1-130">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f4e1-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7f4e1-131">-ServiceName</span></span>
<span data-ttu-id="7f4e1-132">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="7f4e1-132">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f4e1-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f4e1-133">-Confirm</span></span>
<span data-ttu-id="7f4e1-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7f4e1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f4e1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f4e1-135">-WhatIf</span></span>
<span data-ttu-id="7f4e1-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f4e1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f4e1-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7f4e1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f4e1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f4e1-138">CommonParameters</span></span>
<span data-ttu-id="7f4e1-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f4e1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f4e1-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f4e1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f4e1-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f4e1-141">INPUTS</span></span>

### <span data-ttu-id="7f4e1-142">Brak</span><span class="sxs-lookup"><span data-stu-id="7f4e1-142">None</span></span>

## <span data-ttu-id="7f4e1-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f4e1-143">OUTPUTS</span></span>

### <span data-ttu-id="7f4e1-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="7f4e1-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="7f4e1-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7f4e1-145">NOTES</span></span>

## <span data-ttu-id="7f4e1-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f4e1-146">RELATED LINKS</span></span>

[<span data-ttu-id="7f4e1-147">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="7f4e1-147">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="7f4e1-148">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="7f4e1-148">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="7f4e1-149">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="7f4e1-149">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)