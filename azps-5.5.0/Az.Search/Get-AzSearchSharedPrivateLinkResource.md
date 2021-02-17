---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 1a49d73ea564cab6f01b9482a7c110aeaa7fc307
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192707"
---
# <span data-ttu-id="d8677-101">Get-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d8677-101">Get-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="d8677-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8677-102">SYNOPSIS</span></span>
<span data-ttu-id="d8677-103">Pobiera udostępnione zasoby linków prywatnych usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d8677-103">Gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d8677-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8677-104">SYNTAX</span></span>

### <span data-ttu-id="d8677-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d8677-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8677-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8677-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8677-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8677-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8677-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8677-108">DESCRIPTION</span></span>
<span data-ttu-id="d8677-109">Polecenie **cmdlet Get-AzSearchSharedPrivateLinkResource** pobiera udostępnione prywatne zasoby linków usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d8677-109">The **Get-AzSearchSharedPrivateLinkResource** cmdlet gets shared private link resources(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d8677-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8677-110">EXAMPLES</span></span>

### <span data-ttu-id="d8677-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d8677-111">Example 1</span></span>
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

<span data-ttu-id="d8677-112">W tym przykładzie wymieniono wszystkie udostępnione zasoby prywatnego linku usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d8677-112">This example lists all the shared private link resources of the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="d8677-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d8677-113">Example 2</span></span>
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

<span data-ttu-id="d8677-114">W tym przykładzie wymieniono określony udostępniony prywatny zasób linków według nazwy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d8677-114">This example lists a specific shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d8677-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8677-115">PARAMETERS</span></span>

### <span data-ttu-id="d8677-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8677-116">-DefaultProfile</span></span>
<span data-ttu-id="d8677-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8677-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8677-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d8677-118">-Name</span></span>
<span data-ttu-id="d8677-119">Azure Cognitive Search Shared private link resource</span><span class="sxs-lookup"><span data-stu-id="d8677-119">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="d8677-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="d8677-120">-ParentObject</span></span>
<span data-ttu-id="d8677-121">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d8677-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="d8677-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8677-122">-ResourceGroupName</span></span>
<span data-ttu-id="d8677-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8677-123">Resource Group name.</span></span>

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

### <span data-ttu-id="d8677-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8677-124">-ResourceId</span></span>
<span data-ttu-id="d8677-125">Udostępniony identyfikator zasobu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="d8677-125">Shared private link resource id</span></span>

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

### <span data-ttu-id="d8677-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d8677-126">-ServiceName</span></span>
<span data-ttu-id="d8677-127">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d8677-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="d8677-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8677-128">-Confirm</span></span>
<span data-ttu-id="d8677-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d8677-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8677-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8677-130">-WhatIf</span></span>
<span data-ttu-id="d8677-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8677-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8677-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d8677-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8677-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8677-133">CommonParameters</span></span>
<span data-ttu-id="d8677-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8677-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8677-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8677-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8677-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8677-136">INPUTS</span></span>

### <span data-ttu-id="d8677-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d8677-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="d8677-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d8677-138">System.String</span></span>

## <span data-ttu-id="d8677-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8677-139">OUTPUTS</span></span>

### <span data-ttu-id="d8677-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d8677-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="d8677-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8677-141">NOTES</span></span>

## <span data-ttu-id="d8677-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8677-142">RELATED LINKS</span></span>

[<span data-ttu-id="d8677-143">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d8677-143">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="d8677-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d8677-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="d8677-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d8677-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
