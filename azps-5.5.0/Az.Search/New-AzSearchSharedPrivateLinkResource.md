---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 1a9f76ef0d1955076171cc157686b7ae5d7be266
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192691"
---
# <span data-ttu-id="d31e1-101">New-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d31e1-101">New-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="d31e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d31e1-102">SYNOPSIS</span></span>
<span data-ttu-id="d31e1-103">Tworzy udostępniony prywatny zasób linku dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d31e1-103">Creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d31e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d31e1-104">SYNTAX</span></span>

```
New-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-PrivateLinkResourceId] <String> [-GroupId] <String> [-RequestMessage] <String> [[-ResourceRegion] <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d31e1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d31e1-105">DESCRIPTION</span></span>
<span data-ttu-id="d31e1-106">**New-AzSearchSharedPrivateLinkResource** tworzy udostępniony prywatny zasób linków dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d31e1-106">The **New-AzSearchSharedPrivateLinkResource** creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d31e1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d31e1-107">EXAMPLES</span></span>

### <span data-ttu-id="d31e1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d31e1-108">Example 1</span></span>
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

<span data-ttu-id="d31e1-109">W tym przykładzie jest dzielony prywatny zasób linku do usługi obiektów blob konta magazynu dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d31e1-109">This example creates a shared private link resource to the blob service of a storage account for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d31e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d31e1-110">PARAMETERS</span></span>

### <span data-ttu-id="d31e1-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d31e1-111">-AsJob</span></span>
<span data-ttu-id="d31e1-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d31e1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d31e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d31e1-113">-DefaultProfile</span></span>
<span data-ttu-id="d31e1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d31e1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d31e1-115">- GroupId</span><span class="sxs-lookup"><span data-stu-id="d31e1-115">-GroupId</span></span>
<span data-ttu-id="d31e1-116">Współużytkowanie identyfikatora grupy zasobów linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="d31e1-116">Shared private link resource group id</span></span>

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

### <span data-ttu-id="d31e1-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d31e1-117">-Name</span></span>
<span data-ttu-id="d31e1-118">Azure Cognitive Search Shared private link resource</span><span class="sxs-lookup"><span data-stu-id="d31e1-118">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="d31e1-119">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="d31e1-119">-PrivateLinkResourceId</span></span>
<span data-ttu-id="d31e1-120">Udostępniony identyfikator zasobu docelowego linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="d31e1-120">Shared private link target resource id</span></span>

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

### <span data-ttu-id="d31e1-121">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="d31e1-121">-RequestMessage</span></span>
<span data-ttu-id="d31e1-122">Udostępniony komunikat o żądaniu prywatnego zasobu linku</span><span class="sxs-lookup"><span data-stu-id="d31e1-122">Shared private link resource request message</span></span>

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

### <span data-ttu-id="d31e1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d31e1-123">-ResourceGroupName</span></span>
<span data-ttu-id="d31e1-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d31e1-124">Resource Group name.</span></span>

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

### <span data-ttu-id="d31e1-125">-ResourceRegion</span><span class="sxs-lookup"><span data-stu-id="d31e1-125">-ResourceRegion</span></span>
<span data-ttu-id="d31e1-126">(Opcjonalnie) Udostępniony region zasobów linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="d31e1-126">(Optional) Shared private link resource region</span></span>

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

### <span data-ttu-id="d31e1-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d31e1-127">-ServiceName</span></span>
<span data-ttu-id="d31e1-128">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d31e1-128">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="d31e1-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d31e1-129">-Confirm</span></span>
<span data-ttu-id="d31e1-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d31e1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d31e1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d31e1-131">-WhatIf</span></span>
<span data-ttu-id="d31e1-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d31e1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d31e1-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d31e1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d31e1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d31e1-134">CommonParameters</span></span>
<span data-ttu-id="d31e1-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d31e1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d31e1-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d31e1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d31e1-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d31e1-137">INPUTS</span></span>

### <span data-ttu-id="d31e1-138">Brak</span><span class="sxs-lookup"><span data-stu-id="d31e1-138">None</span></span>

## <span data-ttu-id="d31e1-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d31e1-139">OUTPUTS</span></span>

### <span data-ttu-id="d31e1-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d31e1-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="d31e1-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d31e1-141">NOTES</span></span>

## <span data-ttu-id="d31e1-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d31e1-142">RELATED LINKS</span></span>

[<span data-ttu-id="d31e1-143">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d31e1-143">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="d31e1-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d31e1-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="d31e1-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d31e1-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
