---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 829bd1f01be1226346d67f9b662915675cd70f80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986868"
---
# <span data-ttu-id="287c5-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="287c5-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="287c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="287c5-102">SYNOPSIS</span></span>
<span data-ttu-id="287c5-103">Utwórz nowy obiekt lokalizacji Dla firmy Adb (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="287c5-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="287c5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="287c5-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="287c5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="287c5-105">DESCRIPTION</span></span>
<span data-ttu-id="287c5-106">Utwórz nowy obiekt lokalizacji Dla firmy Adb (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="287c5-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="287c5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="287c5-107">EXAMPLES</span></span>

### <span data-ttu-id="287c5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="287c5-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="287c5-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="287c5-109">PARAMETERS</span></span>

### <span data-ttu-id="287c5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287c5-110">-DefaultProfile</span></span>
<span data-ttu-id="287c5-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="287c5-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="287c5-112">- FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="287c5-112">-FailoverPriority</span></span>
<span data-ttu-id="287c5-113">Priorytet trybu failover lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="287c5-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="287c5-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="287c5-114">-IsZoneRedundant</span></span>
<span data-ttu-id="287c5-115">Wartość logiczna wskazująca, czy ten region jest strefą dostępności.</span><span class="sxs-lookup"><span data-stu-id="287c5-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="287c5-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="287c5-116">-LocationName</span></span>
<span data-ttu-id="287c5-117">Nazwa wartości Lokalizacja w ciągu.</span><span class="sxs-lookup"><span data-stu-id="287c5-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="287c5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287c5-118">CommonParameters</span></span>
<span data-ttu-id="287c5-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="287c5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287c5-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="287c5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287c5-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="287c5-121">INPUTS</span></span>

### <span data-ttu-id="287c5-122">Brak</span><span class="sxs-lookup"><span data-stu-id="287c5-122">None</span></span>

## <span data-ttu-id="287c5-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="287c5-123">OUTPUTS</span></span>

### <span data-ttu-id="287c5-124">Microsoft.Azure.Commands.Dosdb.Models.PSLocation</span><span class="sxs-lookup"><span data-stu-id="287c5-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="287c5-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="287c5-125">NOTES</span></span>

## <span data-ttu-id="287c5-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="287c5-126">RELATED LINKS</span></span>
