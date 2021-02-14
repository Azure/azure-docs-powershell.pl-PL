---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: e5d65cb334070cdc5e861a2f90bd95277d41fab5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176363"
---
# <span data-ttu-id="0e024-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0e024-101">Get-AzSearchService</span></span>

## <span data-ttu-id="0e024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e024-102">SYNOPSIS</span></span>
<span data-ttu-id="0e024-103">Pobiera usługę Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="0e024-103">Gets an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0e024-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e024-104">SYNTAX</span></span>

### <span data-ttu-id="0e024-105">ResourceGroupParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0e024-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e024-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e024-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e024-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e024-107">DESCRIPTION</span></span>
<span data-ttu-id="0e024-108">Polecenie **cmdlet Get-AzSearchService** pobiera określoną usługę Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="0e024-108">The **Get-AzSearchService** cmdlet gets the specified Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0e024-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e024-109">EXAMPLES</span></span>

### <span data-ttu-id="0e024-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e024-110">Example 1</span></span>
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

<span data-ttu-id="0e024-111">Uzyskaj usługę Azure Cognitive Search z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="0e024-111">Get an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="0e024-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e024-112">PARAMETERS</span></span>

### <span data-ttu-id="0e024-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e024-113">-DefaultProfile</span></span>
<span data-ttu-id="0e024-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e024-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e024-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0e024-115">-Name</span></span>
<span data-ttu-id="0e024-116">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="0e024-116">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="0e024-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e024-117">-ResourceGroupName</span></span>
<span data-ttu-id="0e024-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e024-118">Resource Group name.</span></span>

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

### <span data-ttu-id="0e024-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e024-119">-ResourceId</span></span>
<span data-ttu-id="0e024-120">Identyfikator zasobu usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="0e024-120">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="0e024-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e024-121">CommonParameters</span></span>
<span data-ttu-id="0e024-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e024-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e024-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e024-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e024-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e024-124">INPUTS</span></span>

### <span data-ttu-id="0e024-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0e024-125">System.String</span></span>

## <span data-ttu-id="0e024-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0e024-126">OUTPUTS</span></span>

### <span data-ttu-id="0e024-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="0e024-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="0e024-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e024-128">NOTES</span></span>

## <span data-ttu-id="0e024-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e024-129">RELATED LINKS</span></span>

[<span data-ttu-id="0e024-130">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0e024-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="0e024-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0e024-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="0e024-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0e024-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)