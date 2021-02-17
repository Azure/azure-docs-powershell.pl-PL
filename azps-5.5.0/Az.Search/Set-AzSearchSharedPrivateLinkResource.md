---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 5fd69c2ec5542ebcf8737f24cfbe068d775f1c04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178667"
---
# <span data-ttu-id="d4d1d-101">Set-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d4d1d-101">Set-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="d4d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d1d-103">Zaktualizuj udostępniony zasób linków prywatnych dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-103">Update the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d4d1d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d4d1d-104">SYNTAX</span></span>

### <span data-ttu-id="d4d1d-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d4d1d-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -RequestMessage <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4d1d-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d1d-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> -RequestMessage <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d1d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d1d-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource [-ResourceId] <String> -RequestMessage <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4d1d-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4d1d-108">InputObjectParameterSet</span></span>
```
Set-AzSearchSharedPrivateLinkResource -RequestMessage <String> -InputObject <PSSharedPrivateLinkResource>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4d1d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d4d1d-109">DESCRIPTION</span></span>
<span data-ttu-id="d4d1d-110">Ten **set-AzSearchSharedPrivateLinkResource** aktualizuje udostępniony prywatny zasób linków dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-110">This **Set-AzSearchSharedPrivateLinkResource** updates the shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d4d1d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d4d1d-111">EXAMPLES</span></span>

### <span data-ttu-id="d4d1d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d4d1d-112">Example 1</span></span>
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

<span data-ttu-id="d4d1d-113">W tym przykładzie jest aktualizowany komunikat o żądaniu dla oczekującego udostępnionego zasobu prywatnego linku dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-113">This example updates the request message for the pending shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d4d1d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4d1d-114">PARAMETERS</span></span>

### <span data-ttu-id="d4d1d-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d4d1d-115">-AsJob</span></span>
<span data-ttu-id="d4d1d-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d4d1d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4d1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d1d-117">-DefaultProfile</span></span>
<span data-ttu-id="d4d1d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4d1d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4d1d-119">-InputObject</span></span>
<span data-ttu-id="d4d1d-120">Udostępniony obiekt wejściowy zasobu prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="d4d1d-120">Shared private link resource input object</span></span>

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

### <span data-ttu-id="d4d1d-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d4d1d-121">-Name</span></span>
<span data-ttu-id="d4d1d-122">Azure Cognitive Search Shared private link resource</span><span class="sxs-lookup"><span data-stu-id="d4d1d-122">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="d4d1d-123">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="d4d1d-123">-ParentObject</span></span>
<span data-ttu-id="d4d1d-124">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="d4d1d-125">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="d4d1d-125">-RequestMessage</span></span>
<span data-ttu-id="d4d1d-126">Udostępniony komunikat o żądaniu prywatnego zasobu linku</span><span class="sxs-lookup"><span data-stu-id="d4d1d-126">Shared private link resource request message</span></span>

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

### <span data-ttu-id="d4d1d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4d1d-127">-ResourceGroupName</span></span>
<span data-ttu-id="d4d1d-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-128">Resource Group name.</span></span>

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

### <span data-ttu-id="d4d1d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4d1d-129">-ResourceId</span></span>
<span data-ttu-id="d4d1d-130">Udostępniony identyfikator zasobu linku prywatnego</span><span class="sxs-lookup"><span data-stu-id="d4d1d-130">Shared private link resource id</span></span>

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

### <span data-ttu-id="d4d1d-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d4d1d-131">-ServiceName</span></span>
<span data-ttu-id="d4d1d-132">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-132">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="d4d1d-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4d1d-133">-Confirm</span></span>
<span data-ttu-id="d4d1d-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4d1d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4d1d-135">-WhatIf</span></span>
<span data-ttu-id="d4d1d-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4d1d-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4d1d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d1d-138">CommonParameters</span></span>
<span data-ttu-id="d4d1d-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4d1d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d1d-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4d1d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d1d-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4d1d-141">INPUTS</span></span>

### <span data-ttu-id="d4d1d-142">Brak</span><span class="sxs-lookup"><span data-stu-id="d4d1d-142">None</span></span>

## <span data-ttu-id="d4d1d-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4d1d-143">OUTPUTS</span></span>

### <span data-ttu-id="d4d1d-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d4d1d-144">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="d4d1d-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d4d1d-145">NOTES</span></span>

## <span data-ttu-id="d4d1d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4d1d-146">RELATED LINKS</span></span>

[<span data-ttu-id="d4d1d-147">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d4d1d-147">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="d4d1d-148">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d4d1d-148">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="d4d1d-149">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="d4d1d-149">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)