---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
ms.openlocfilehash: 57b09ea3267447f16ceadf4d1eae51f997c53a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541444"
---
# <span data-ttu-id="70e41-101">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="70e41-101">Get-AzureRmSearchService</span></span>

## <span data-ttu-id="70e41-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70e41-102">SYNOPSIS</span></span>
<span data-ttu-id="70e41-103">Pobiera usługę Azure Search.</span><span class="sxs-lookup"><span data-stu-id="70e41-103">Gets an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70e41-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70e41-104">SYNTAX</span></span>

### <span data-ttu-id="70e41-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="70e41-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSearchService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70e41-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70e41-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70e41-107">Opis</span><span class="sxs-lookup"><span data-stu-id="70e41-107">DESCRIPTION</span></span>
<span data-ttu-id="70e41-108">Polecenie cmdlet **Get-AzureRmSearchService** pobiera określoną usługę Azure Search.</span><span class="sxs-lookup"><span data-stu-id="70e41-108">The **Get-AzureRmSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="70e41-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70e41-109">EXAMPLES</span></span>

### <span data-ttu-id="70e41-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="70e41-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="70e41-111">Uzyskaj usługę Azure Search z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="70e41-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="70e41-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70e41-112">PARAMETERS</span></span>

### <span data-ttu-id="70e41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e41-113">-DefaultProfile</span></span>
<span data-ttu-id="70e41-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70e41-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70e41-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70e41-115">-Name</span></span>
<span data-ttu-id="70e41-116">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="70e41-116">Search Service name.</span></span>

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

### <span data-ttu-id="70e41-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e41-117">-ResourceGroupName</span></span>
<span data-ttu-id="70e41-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70e41-118">Resource Group name.</span></span>

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

### <span data-ttu-id="70e41-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70e41-119">-ResourceId</span></span>
<span data-ttu-id="70e41-120">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="70e41-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="70e41-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e41-121">CommonParameters</span></span>
<span data-ttu-id="70e41-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70e41-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e41-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70e41-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e41-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70e41-124">INPUTS</span></span>

### <span data-ttu-id="70e41-125">System. String</span><span class="sxs-lookup"><span data-stu-id="70e41-125">System.String</span></span>

## <span data-ttu-id="70e41-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70e41-126">OUTPUTS</span></span>

### <span data-ttu-id="70e41-127">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="70e41-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="70e41-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70e41-128">NOTES</span></span>

## <span data-ttu-id="70e41-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70e41-129">RELATED LINKS</span></span>

[<span data-ttu-id="70e41-130">Nowe — AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="70e41-130">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="70e41-131">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="70e41-131">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="70e41-132">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="70e41-132">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
