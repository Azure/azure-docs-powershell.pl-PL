---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 683a6105273bcd2ff2f254352cf6e991491c035d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976401"
---
# <span data-ttu-id="4014a-101">New-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="4014a-101">New-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="4014a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4014a-102">SYNOPSIS</span></span>
<span data-ttu-id="4014a-103">Tworzy udostępniony prywatny zasób linku dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="4014a-103">Creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4014a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4014a-104">SYNTAX</span></span>

```
New-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-PrivateLinkResourceId] <String> [-GroupId] <String> [-RequestMessage] <String> [[-ResourceRegion] <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4014a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4014a-105">DESCRIPTION</span></span>
<span data-ttu-id="4014a-106">**New-AzSearchSharedPrivateLinkResource** tworzy udostępniony prywatny zasób linków dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="4014a-106">The **New-AzSearchSharedPrivateLinkResource** creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4014a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4014a-107">EXAMPLES</span></span>

### <span data-ttu-id="4014a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4014a-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -PrivateLinkResourceId /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting -GroupId blob -RequestMessage "Please approve" 

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please approve
ResourceRegion        :
```

<span data-ttu-id="4014a-109">W tym przykładzie jest dzielony prywatny zasób linku do usługi obiektów blob konta magazynu dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="4014a-109">This example creates a shared private link resource to the blob service of a storage account for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4014a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4014a-110">PARAMETERS</span></span>

### <span data-ttu-id="4014a-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4014a-111">-AsJob</span></span>
<span data-ttu-id="4014a-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4014a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4014a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4014a-113">-DefaultProfile</span></span>
<span data-ttu-id="4014a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4014a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4014a-115">- GroupId</span><span class="sxs-lookup"><span data-stu-id="4014a-115">-GroupId</span></span>
<span data-ttu-id="4014a-116">Współużytkowanie identyfikatora grupy zasobów linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="4014a-116">Shared private link resource group id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4014a-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4014a-117">-Name</span></span>
<span data-ttu-id="4014a-118">Azure Cognitive Search Shared private link resource</span><span class="sxs-lookup"><span data-stu-id="4014a-118">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4014a-119">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="4014a-119">-PrivateLinkResourceId</span></span>
<span data-ttu-id="4014a-120">Udostępniony identyfikator zasobu docelowego linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="4014a-120">Shared private link target resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4014a-121">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="4014a-121">-RequestMessage</span></span>
<span data-ttu-id="4014a-122">Udostępniony komunikat o żądaniu prywatnego zasobu linku</span><span class="sxs-lookup"><span data-stu-id="4014a-122">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4014a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4014a-123">-ResourceGroupName</span></span>
<span data-ttu-id="4014a-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4014a-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4014a-125">-ResourceRegion</span><span class="sxs-lookup"><span data-stu-id="4014a-125">-ResourceRegion</span></span>
<span data-ttu-id="4014a-126">(Opcjonalnie) Udostępniony region zasobów linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="4014a-126">(Optional) Shared private link resource region</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4014a-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4014a-127">-ServiceName</span></span>
<span data-ttu-id="4014a-128">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="4014a-128">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4014a-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4014a-129">-Confirm</span></span>
<span data-ttu-id="4014a-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4014a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4014a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4014a-131">-WhatIf</span></span>
<span data-ttu-id="4014a-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4014a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4014a-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4014a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4014a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4014a-134">CommonParameters</span></span>
<span data-ttu-id="4014a-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4014a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4014a-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4014a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4014a-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4014a-137">INPUTS</span></span>

### <span data-ttu-id="4014a-138">Brak</span><span class="sxs-lookup"><span data-stu-id="4014a-138">None</span></span>

## <span data-ttu-id="4014a-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4014a-139">OUTPUTS</span></span>

### <span data-ttu-id="4014a-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="4014a-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="4014a-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4014a-141">NOTES</span></span>

## <span data-ttu-id="4014a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4014a-142">RELATED LINKS</span></span>

[<span data-ttu-id="4014a-143">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="4014a-143">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="4014a-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="4014a-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="4014a-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="4014a-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
