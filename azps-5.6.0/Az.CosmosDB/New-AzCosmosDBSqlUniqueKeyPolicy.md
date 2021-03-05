---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: 6ef9e9b4fe2332af22bb8bdab1334096860f53ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986861"
---
# <span data-ttu-id="35506-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="35506-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="35506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35506-102">SYNOPSIS</span></span>
<span data-ttu-id="35506-103">Tworzy nowy obiekt SqlUniqueKeyPolicy SqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="35506-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="35506-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="35506-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35506-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="35506-105">DESCRIPTION</span></span>
<span data-ttu-id="35506-106">Polecenie cmdlet **New-AzCosmosDBSqlUniqueKeyPolicy** tworzy nowy obiekt typu PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="35506-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="35506-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="35506-107">EXAMPLES</span></span>

### <span data-ttu-id="35506-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35506-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="35506-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35506-109">PARAMETERS</span></span>

### <span data-ttu-id="35506-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35506-110">-DefaultProfile</span></span>
<span data-ttu-id="35506-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="35506-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35506-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="35506-112">-UniqueKey</span></span>
<span data-ttu-id="35506-113">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="35506-113">Database name.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35506-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35506-114">CommonParameters</span></span>
<span data-ttu-id="35506-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35506-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35506-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35506-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35506-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35506-117">INPUTS</span></span>

### <span data-ttu-id="35506-118">Brak</span><span class="sxs-lookup"><span data-stu-id="35506-118">None</span></span>

## <span data-ttu-id="35506-119">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35506-119">OUTPUTS</span></span>

### <span data-ttu-id="35506-120">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="35506-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="35506-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="35506-121">NOTES</span></span>

## <span data-ttu-id="35506-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35506-122">RELATED LINKS</span></span>
