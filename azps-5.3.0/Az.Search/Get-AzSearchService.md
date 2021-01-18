---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: e4751232969c407484b978d495d348dc61810715
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498433"
---
# <span data-ttu-id="92f16-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="92f16-101">Get-AzSearchService</span></span>

## <span data-ttu-id="92f16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92f16-102">SYNOPSIS</span></span>
<span data-ttu-id="92f16-103">Pobiera usługę Azure Search.</span><span class="sxs-lookup"><span data-stu-id="92f16-103">Gets an Azure Search service.</span></span>

## <span data-ttu-id="92f16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92f16-104">SYNTAX</span></span>

### <span data-ttu-id="92f16-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="92f16-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92f16-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92f16-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92f16-107">Opis</span><span class="sxs-lookup"><span data-stu-id="92f16-107">DESCRIPTION</span></span>
<span data-ttu-id="92f16-108">Polecenie cmdlet **Get-AzSearchService** pobiera określoną usługę Azure Search.</span><span class="sxs-lookup"><span data-stu-id="92f16-108">The **Get-AzSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="92f16-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92f16-109">EXAMPLES</span></span>

### <span data-ttu-id="92f16-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="92f16-110">Example 1</span></span>
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

<span data-ttu-id="92f16-111">Uzyskaj usługę Azure Search z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="92f16-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="92f16-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92f16-112">PARAMETERS</span></span>

### <span data-ttu-id="92f16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f16-113">-DefaultProfile</span></span>
<span data-ttu-id="92f16-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92f16-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92f16-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92f16-115">-Name</span></span>
<span data-ttu-id="92f16-116">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="92f16-116">Search Service name.</span></span>

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

### <span data-ttu-id="92f16-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f16-117">-ResourceGroupName</span></span>
<span data-ttu-id="92f16-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92f16-118">Resource Group name.</span></span>

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

### <span data-ttu-id="92f16-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92f16-119">-ResourceId</span></span>
<span data-ttu-id="92f16-120">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="92f16-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="92f16-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f16-121">CommonParameters</span></span>
<span data-ttu-id="92f16-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f16-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f16-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f16-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f16-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92f16-124">INPUTS</span></span>

### <span data-ttu-id="92f16-125">System. String</span><span class="sxs-lookup"><span data-stu-id="92f16-125">System.String</span></span>

## <span data-ttu-id="92f16-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92f16-126">OUTPUTS</span></span>

### <span data-ttu-id="92f16-127">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="92f16-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="92f16-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92f16-128">NOTES</span></span>

## <span data-ttu-id="92f16-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92f16-129">RELATED LINKS</span></span>

[<span data-ttu-id="92f16-130">Nowe — AzSearchService</span><span class="sxs-lookup"><span data-stu-id="92f16-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="92f16-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="92f16-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="92f16-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="92f16-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)