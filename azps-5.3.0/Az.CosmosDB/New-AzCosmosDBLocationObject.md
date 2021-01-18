---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501734"
---
# <span data-ttu-id="4524a-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="4524a-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="4524a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4524a-102">SYNOPSIS</span></span>
<span data-ttu-id="4524a-103">Utwórz nowy obiekt lokalizacji CosmosDB (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="4524a-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="4524a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4524a-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4524a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4524a-105">DESCRIPTION</span></span>
<span data-ttu-id="4524a-106">Utwórz nowy obiekt lokalizacji CosmosDB (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="4524a-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="4524a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4524a-107">EXAMPLES</span></span>

### <span data-ttu-id="4524a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4524a-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="4524a-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4524a-109">PARAMETERS</span></span>

### <span data-ttu-id="4524a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4524a-110">-DefaultProfile</span></span>
<span data-ttu-id="4524a-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4524a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4524a-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="4524a-112">-FailoverPriority</span></span>
<span data-ttu-id="4524a-113">Priorytet pracy awaryjnej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4524a-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="4524a-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="4524a-114">-IsZoneRedundant</span></span>
<span data-ttu-id="4524a-115">Wartość logiczna wskazująca, czy dany region jest AvailabilityZone.</span><span class="sxs-lookup"><span data-stu-id="4524a-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="4524a-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="4524a-116">-LocationName</span></span>
<span data-ttu-id="4524a-117">Nazwa lokalizacji w ciągu.</span><span class="sxs-lookup"><span data-stu-id="4524a-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="4524a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4524a-118">CommonParameters</span></span>
<span data-ttu-id="4524a-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4524a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4524a-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4524a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4524a-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4524a-121">INPUTS</span></span>

### <span data-ttu-id="4524a-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4524a-122">None</span></span>

## <span data-ttu-id="4524a-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4524a-123">OUTPUTS</span></span>

### <span data-ttu-id="4524a-124">Microsoft. Azure. Commands. CosmosDB. models. PSLocation</span><span class="sxs-lookup"><span data-stu-id="4524a-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="4524a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4524a-125">NOTES</span></span>

## <span data-ttu-id="4524a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4524a-126">RELATED LINKS</span></span>
