---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: ac27d706afcce4b8b431e0253b0a4e5146883640
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982186"
---
# <span data-ttu-id="f46d6-101">Get-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f46d6-101">Get-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="f46d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f46d6-102">SYNOPSIS</span></span>
<span data-ttu-id="f46d6-103">Pobiera udostępnione zasoby linków prywatnych usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="f46d6-103">Gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="f46d6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f46d6-104">SYNTAX</span></span>

### <span data-ttu-id="f46d6-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f46d6-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f46d6-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f46d6-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f46d6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f46d6-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f46d6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f46d6-108">DESCRIPTION</span></span>
<span data-ttu-id="f46d6-109">Polecenie **cmdlet Get-AzSearchSharedPrivateLinkResource** pobiera udostępnione prywatne zasoby linków usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="f46d6-109">The **Get-AzSearchSharedPrivateLinkResource** cmdlet gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="f46d6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f46d6-110">EXAMPLES</span></span>

### <span data-ttu-id="f46d6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f46d6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/cosmos-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : cosmos-pe
GroupId               : Sql
PrivateLinkResourceId : /subscriptions/dc95d1b6-71a8-4dff-bcc9-a1c282bdbd8b/resourceGroups/arjagann/providers/Microsoft.DocumentDb/databaseAccounts/arjagann-sql
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe2
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe2
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting2
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="f46d6-112">W tym przykładzie wymieniono wszystkie udostępnione zasoby prywatnego linku usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="f46d6-112">This example lists all the shared private link resources of the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="f46d6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f46d6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name table-pe

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/table-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : table-pe
GroupId               : table
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : please approve
ResourceRegion        :
```

<span data-ttu-id="f46d6-114">W tym przykładzie wymieniono określony udostępniony zasób prywatny linku według nazwy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="f46d6-114">This example lists a specific shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="f46d6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f46d6-115">PARAMETERS</span></span>

### <span data-ttu-id="f46d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46d6-116">-DefaultProfile</span></span>
<span data-ttu-id="f46d6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f46d6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f46d6-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f46d6-118">-Name</span></span>
<span data-ttu-id="f46d6-119">Azure Cognitive Search Shared private link resource</span><span class="sxs-lookup"><span data-stu-id="f46d6-119">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46d6-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="f46d6-120">-ParentObject</span></span>
<span data-ttu-id="f46d6-121">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="f46d6-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f46d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f46d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="f46d6-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f46d6-123">Resource Group name.</span></span>

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

### <span data-ttu-id="f46d6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f46d6-124">-ResourceId</span></span>
<span data-ttu-id="f46d6-125">Udostępniony identyfikator zasobu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="f46d6-125">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f46d6-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f46d6-126">-ServiceName</span></span>
<span data-ttu-id="f46d6-127">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="f46d6-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="f46d6-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f46d6-128">-Confirm</span></span>
<span data-ttu-id="f46d6-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f46d6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f46d6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f46d6-130">-WhatIf</span></span>
<span data-ttu-id="f46d6-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f46d6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f46d6-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f46d6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f46d6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46d6-133">CommonParameters</span></span>
<span data-ttu-id="f46d6-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f46d6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46d6-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f46d6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46d6-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f46d6-136">INPUTS</span></span>

### <span data-ttu-id="f46d6-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="f46d6-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="f46d6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f46d6-138">System.String</span></span>

## <span data-ttu-id="f46d6-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f46d6-139">OUTPUTS</span></span>

### <span data-ttu-id="f46d6-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f46d6-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="f46d6-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f46d6-141">NOTES</span></span>

## <span data-ttu-id="f46d6-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f46d6-142">RELATED LINKS</span></span>

[<span data-ttu-id="f46d6-143">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="f46d6-143">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="f46d6-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="f46d6-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="f46d6-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="f46d6-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
