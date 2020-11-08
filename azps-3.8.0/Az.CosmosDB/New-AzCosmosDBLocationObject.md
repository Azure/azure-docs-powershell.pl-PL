---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052612"
---
# <span data-ttu-id="50a54-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="50a54-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="50a54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50a54-102">SYNOPSIS</span></span>
<span data-ttu-id="50a54-103">Utwórz nowy obiekt lokalizacji CosmosDB (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="50a54-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="50a54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50a54-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50a54-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50a54-105">DESCRIPTION</span></span>
<span data-ttu-id="50a54-106">Utwórz nowy obiekt lokalizacji CosmosDB (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="50a54-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="50a54-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50a54-107">EXAMPLES</span></span>

### <span data-ttu-id="50a54-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="50a54-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="50a54-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50a54-109">PARAMETERS</span></span>

### <span data-ttu-id="50a54-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50a54-110">-DefaultProfile</span></span>
<span data-ttu-id="50a54-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50a54-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a54-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="50a54-112">-FailoverPriority</span></span>
<span data-ttu-id="50a54-113">Priorytet pracy awaryjnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="50a54-113">Failover priority of the location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a54-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="50a54-114">-IsZoneRedundant</span></span>
<span data-ttu-id="50a54-115">Wartość logiczna wskazująca, czy dany region jest AvailabilityZone.</span><span class="sxs-lookup"><span data-stu-id="50a54-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a54-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="50a54-116">-LocationName</span></span>
<span data-ttu-id="50a54-117">Nazwa lokalizacji w ciągu.</span><span class="sxs-lookup"><span data-stu-id="50a54-117">Name of the Location in string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a54-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a54-118">CommonParameters</span></span>
<span data-ttu-id="50a54-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50a54-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a54-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50a54-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a54-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50a54-121">INPUTS</span></span>

### <span data-ttu-id="50a54-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="50a54-122">None</span></span>

## <span data-ttu-id="50a54-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50a54-123">OUTPUTS</span></span>

### <span data-ttu-id="50a54-124">Microsoft. Azure. Commands. CosmosDB. models. PSLocation</span><span class="sxs-lookup"><span data-stu-id="50a54-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="50a54-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50a54-125">NOTES</span></span>

## <span data-ttu-id="50a54-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50a54-126">RELATED LINKS</span></span>
