---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238530"
---
# <span data-ttu-id="ec3d7-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="ec3d7-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="ec3d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec3d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ec3d7-103">Utwórz nowy obiekt lokalizacji Dla firmy Adb (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="ec3d7-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="ec3d7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ec3d7-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec3d7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ec3d7-105">DESCRIPTION</span></span>
<span data-ttu-id="ec3d7-106">Utwórz nowy obiekt lokalizacji Dla firmy Adb (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="ec3d7-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="ec3d7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ec3d7-107">EXAMPLES</span></span>

### <span data-ttu-id="ec3d7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ec3d7-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="ec3d7-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec3d7-109">PARAMETERS</span></span>

### <span data-ttu-id="ec3d7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec3d7-110">-DefaultProfile</span></span>
<span data-ttu-id="ec3d7-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec3d7-112">- FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="ec3d7-112">-FailoverPriority</span></span>
<span data-ttu-id="ec3d7-113">Priorytet trybu failover lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="ec3d7-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="ec3d7-114">-IsZoneRedundant</span></span>
<span data-ttu-id="ec3d7-115">Wartość logiczna wskazująca, czy ten region jest strefą dostępności.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="ec3d7-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="ec3d7-116">-LocationName</span></span>
<span data-ttu-id="ec3d7-117">Nazwa wartości Lokalizacja w ciągu.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="ec3d7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec3d7-118">CommonParameters</span></span>
<span data-ttu-id="ec3d7-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec3d7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec3d7-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec3d7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec3d7-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec3d7-121">INPUTS</span></span>

### <span data-ttu-id="ec3d7-122">Brak</span><span class="sxs-lookup"><span data-stu-id="ec3d7-122">None</span></span>

## <span data-ttu-id="ec3d7-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec3d7-123">OUTPUTS</span></span>

### <span data-ttu-id="ec3d7-124">Microsoft.Azure.Commands.Dosdb.Models.PSLocation</span><span class="sxs-lookup"><span data-stu-id="ec3d7-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="ec3d7-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ec3d7-125">NOTES</span></span>

## <span data-ttu-id="ec3d7-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec3d7-126">RELATED LINKS</span></span>
