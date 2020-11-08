---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: e4751232969c407484b978d495d348dc61810715
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063232"
---
# <span data-ttu-id="66a55-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="66a55-101">Get-AzSearchService</span></span>

## <span data-ttu-id="66a55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66a55-102">SYNOPSIS</span></span>
<span data-ttu-id="66a55-103">Pobiera usługę Azure Search.</span><span class="sxs-lookup"><span data-stu-id="66a55-103">Gets an Azure Search service.</span></span>

## <span data-ttu-id="66a55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66a55-104">SYNTAX</span></span>

### <span data-ttu-id="66a55-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="66a55-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66a55-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66a55-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66a55-107">Opis</span><span class="sxs-lookup"><span data-stu-id="66a55-107">DESCRIPTION</span></span>
<span data-ttu-id="66a55-108">Polecenie cmdlet **Get-AzSearchService** pobiera określoną usługę Azure Search.</span><span class="sxs-lookup"><span data-stu-id="66a55-108">The **Get-AzSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="66a55-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66a55-109">EXAMPLES</span></span>

### <span data-ttu-id="66a55-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="66a55-110">Example 1</span></span>
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

<span data-ttu-id="66a55-111">Uzyskaj usługę Azure Search z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="66a55-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="66a55-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66a55-112">PARAMETERS</span></span>

### <span data-ttu-id="66a55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a55-113">-DefaultProfile</span></span>
<span data-ttu-id="66a55-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66a55-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66a55-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66a55-115">-Name</span></span>
<span data-ttu-id="66a55-116">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="66a55-116">Search Service name.</span></span>

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

### <span data-ttu-id="66a55-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a55-117">-ResourceGroupName</span></span>
<span data-ttu-id="66a55-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66a55-118">Resource Group name.</span></span>

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

### <span data-ttu-id="66a55-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66a55-119">-ResourceId</span></span>
<span data-ttu-id="66a55-120">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="66a55-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="66a55-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a55-121">CommonParameters</span></span>
<span data-ttu-id="66a55-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a55-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a55-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a55-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a55-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66a55-124">INPUTS</span></span>

### <span data-ttu-id="66a55-125">System. String</span><span class="sxs-lookup"><span data-stu-id="66a55-125">System.String</span></span>

## <span data-ttu-id="66a55-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66a55-126">OUTPUTS</span></span>

### <span data-ttu-id="66a55-127">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="66a55-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="66a55-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66a55-128">NOTES</span></span>

## <span data-ttu-id="66a55-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66a55-129">RELATED LINKS</span></span>

[<span data-ttu-id="66a55-130">Nowe — AzSearchService</span><span class="sxs-lookup"><span data-stu-id="66a55-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="66a55-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="66a55-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="66a55-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="66a55-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)