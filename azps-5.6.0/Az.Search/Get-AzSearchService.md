---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: f4f360cc7fd9151735f131878565a09933f1be54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963681"
---
# <span data-ttu-id="1c80c-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="1c80c-101">Get-AzSearchService</span></span>

## <span data-ttu-id="1c80c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c80c-102">SYNOPSIS</span></span>
<span data-ttu-id="1c80c-103">Pobiera usługę Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1c80c-103">Gets an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1c80c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1c80c-104">SYNTAX</span></span>

### <span data-ttu-id="1c80c-105">ResourceGroupParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1c80c-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c80c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c80c-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c80c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1c80c-107">DESCRIPTION</span></span>
<span data-ttu-id="1c80c-108">Polecenie **cmdlet Get-AzSearchService** pobiera określoną usługę Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1c80c-108">The **Get-AzSearchService** cmdlet gets the specified Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1c80c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1c80c-109">EXAMPLES</span></span>

### <span data-ttu-id="1c80c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1c80c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="1c80c-111">Uzyskaj usługę Azure Cognitive Search z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="1c80c-111">Get an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="1c80c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c80c-112">PARAMETERS</span></span>

### <span data-ttu-id="1c80c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c80c-113">-DefaultProfile</span></span>
<span data-ttu-id="1c80c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c80c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c80c-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1c80c-115">-Name</span></span>
<span data-ttu-id="1c80c-116">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1c80c-116">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c80c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c80c-117">-ResourceGroupName</span></span>
<span data-ttu-id="1c80c-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c80c-118">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c80c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c80c-119">-ResourceId</span></span>
<span data-ttu-id="1c80c-120">Identyfikator zasobu usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1c80c-120">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="1c80c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c80c-121">CommonParameters</span></span>
<span data-ttu-id="1c80c-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c80c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c80c-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c80c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c80c-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c80c-124">INPUTS</span></span>

### <span data-ttu-id="1c80c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="1c80c-125">System.String</span></span>

## <span data-ttu-id="1c80c-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c80c-126">OUTPUTS</span></span>

### <span data-ttu-id="1c80c-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="1c80c-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="1c80c-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1c80c-128">NOTES</span></span>

## <span data-ttu-id="1c80c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c80c-129">RELATED LINKS</span></span>

[<span data-ttu-id="1c80c-130">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="1c80c-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="1c80c-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="1c80c-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="1c80c-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="1c80c-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)