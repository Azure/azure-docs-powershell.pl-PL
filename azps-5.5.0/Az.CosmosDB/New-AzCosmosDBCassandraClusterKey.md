---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177299"
---
# <span data-ttu-id="afd18-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="afd18-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="afd18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afd18-102">SYNOPSIS</span></span>
<span data-ttu-id="afd18-103">Tworzy nowy klucz klasterowy CassandraDb.</span><span class="sxs-lookup"><span data-stu-id="afd18-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="afd18-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="afd18-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afd18-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="afd18-105">DESCRIPTION</span></span>
<span data-ttu-id="afd18-106">Klucz **klasterowy New-AzCosmosDBCassandraClusterKey** tworzy nowy klucz klastrów Dosdb Cassandra.</span><span class="sxs-lookup"><span data-stu-id="afd18-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="afd18-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="afd18-107">EXAMPLES</span></span>

### <span data-ttu-id="afd18-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="afd18-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="afd18-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afd18-109">PARAMETERS</span></span>

### <span data-ttu-id="afd18-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd18-110">-DefaultProfile</span></span>
<span data-ttu-id="afd18-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="afd18-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afd18-112">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="afd18-112">-Name</span></span>
<span data-ttu-id="afd18-113">Nazwa klucza klastrów Cassandra.</span><span class="sxs-lookup"><span data-stu-id="afd18-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="afd18-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="afd18-114">-OrderBy</span></span>
<span data-ttu-id="afd18-115">Ordering of Cassandra Cluster key.</span><span class="sxs-lookup"><span data-stu-id="afd18-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="afd18-116">Możliwe wartości: "Asc", "Desc"</span><span class="sxs-lookup"><span data-stu-id="afd18-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="afd18-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd18-117">CommonParameters</span></span>
<span data-ttu-id="afd18-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afd18-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd18-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afd18-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd18-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afd18-120">INPUTS</span></span>

### <span data-ttu-id="afd18-121">Brak</span><span class="sxs-lookup"><span data-stu-id="afd18-121">None</span></span>

## <span data-ttu-id="afd18-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afd18-122">OUTPUTS</span></span>

### <span data-ttu-id="afd18-123">Microsoft.Azure.Commands.DoceńDB.Models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="afd18-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="afd18-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="afd18-124">NOTES</span></span>

## <span data-ttu-id="afd18-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afd18-125">RELATED LINKS</span></span>
