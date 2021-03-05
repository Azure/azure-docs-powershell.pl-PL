---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-AzSearchPrivateLinkResource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
ms.openlocfilehash: a04af740a320d2550eb3fb4668689328bbe60857
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963729"
---
# <span data-ttu-id="8dc7c-101">Get-AzSearchPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="8dc7c-101">Get-AzSearchPrivateLinkResource</span></span>

## <span data-ttu-id="8dc7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dc7c-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc7c-103">Pobiera szczegóły zasobów prywatnych linków dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-103">Gets private link resource details for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="8dc7c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8dc7c-104">SYNTAX</span></span>

### <span data-ttu-id="8dc7c-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8dc7c-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateLinkResource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc7c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dc7c-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc7c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dc7c-107">InputObjectParameterSet</span></span>
```
Get-AzSearchPrivateLinkResource [-InputObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc7c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8dc7c-108">DESCRIPTION</span></span>
<span data-ttu-id="8dc7c-109">Polecenie **cmdlet Get-AzSearchPrivateLinkResource** pobiera szczegóły prywatnych zasobów linków dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-109">The **Get-AzSearchPrivateLinkResource** cmdlet gets private link resource details for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="8dc7c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8dc7c-110">EXAMPLES</span></span>

### <span data-ttu-id="8dc7c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8dc7c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateLinkResource -ResourceGroupName arjagann -Name arjagann-test-cuseuap | ConvertTo-Json

  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateLinkResources/searchService",
  "Type": "Microsoft.Search/searchServices/privateLinkResources",
  "GroupId": "searchService",
  "RequiredMembers": [
    "searchService"
  ],
  "RequiredZoneNames": [
    "privatelink.search-dogfood.windows-int.net"
  ],
  "ShareablePrivateLinkResourceTypes": [
    {
      "Name": "blob",
      "Description": "Azure Cognitive Search indexers can connect to blobs in Azure Storage for reading data (data source), for writing intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "blob"
    },
    {
      "Name": "table",
      "Description": "Azure Cognitive Search indexers can connect to tables in Azure Storage for reading data (data source), for writing book-keeping information about intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "table"
    },
    {
      "Name": "Sql",
      "Description": "Azure Cognitive Search indexers can connect to CosmosDB using the SQL head for reading data (data source).",
      "Type": "Microsoft.DocumentDB/databaseAccounts",
      "GroupId": "Sql"
    },
    {
      "Name": "plr",
      "Description": "Azure Cognitive Search indexers can connect to AzureSQL databases in a SQL server for reading data (data source).",
      "Type": "Microsoft.Sql/servers",
      "GroupId": "sqlServer"
    },
    {
      "Name": "vault",
      "Description": "Azure Cognitive Search can access keys in Azure Key Vault to encrypt search index and synonym map data",
      "Type": "Microsoft.KeyVault/vaults",
      "GroupId": "vault"
    }
  ]
}
```

<span data-ttu-id="8dc7c-112">W tym przykładzie pokazano, jak uzyskać dla wygody szczegóły prywatnego zasobu linku (w formie JSON) dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-112">The example shows how to get the private link resource details (in JSON form for convenience) for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="8dc7c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dc7c-113">PARAMETERS</span></span>

### <span data-ttu-id="8dc7c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc7c-114">-DefaultProfile</span></span>
<span data-ttu-id="8dc7c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dc7c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dc7c-116">-InputObject</span></span>
<span data-ttu-id="8dc7c-117">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-117">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc7c-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8dc7c-118">-Name</span></span>
<span data-ttu-id="8dc7c-119">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-119">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="8dc7c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc7c-120">-ResourceGroupName</span></span>
<span data-ttu-id="8dc7c-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-121">Resource Group name.</span></span>

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

### <span data-ttu-id="8dc7c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc7c-122">-ResourceId</span></span>
<span data-ttu-id="8dc7c-123">Identyfikator zasobu usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-123">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="8dc7c-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8dc7c-124">-Confirm</span></span>
<span data-ttu-id="8dc7c-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc7c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc7c-126">-WhatIf</span></span>
<span data-ttu-id="8dc7c-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dc7c-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc7c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc7c-129">CommonParameters</span></span>
<span data-ttu-id="8dc7c-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc7c-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8dc7c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc7c-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8dc7c-132">INPUTS</span></span>

### <span data-ttu-id="8dc7c-133">Brak</span><span class="sxs-lookup"><span data-stu-id="8dc7c-133">None</span></span>

## <span data-ttu-id="8dc7c-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8dc7c-134">OUTPUTS</span></span>

### <span data-ttu-id="8dc7c-135">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="8dc7c-135">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="8dc7c-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8dc7c-136">NOTES</span></span>

## <span data-ttu-id="8dc7c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8dc7c-137">RELATED LINKS</span></span>

[<span data-ttu-id="8dc7c-138">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="8dc7c-138">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="8dc7c-139">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="8dc7c-139">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="8dc7c-140">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="8dc7c-140">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="8dc7c-141">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="8dc7c-141">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)