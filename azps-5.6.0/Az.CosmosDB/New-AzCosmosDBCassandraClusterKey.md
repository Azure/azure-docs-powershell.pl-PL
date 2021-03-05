---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: 9afcffc281c48e0235c814b352e65ae47e5f4337
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009745"
---
# <span data-ttu-id="cadb5-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="cadb5-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="cadb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cadb5-102">SYNOPSIS</span></span>
<span data-ttu-id="cadb5-103">Tworzy nowy klucz klasterowy CassandraDb.</span><span class="sxs-lookup"><span data-stu-id="cadb5-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="cadb5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cadb5-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cadb5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cadb5-105">DESCRIPTION</span></span>
<span data-ttu-id="cadb5-106">Klucz **klasterowy New-AzCosmosDBCassandraClusterKey** tworzy nowy klucz klastrów Dosdb Cassandra.</span><span class="sxs-lookup"><span data-stu-id="cadb5-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="cadb5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cadb5-107">EXAMPLES</span></span>

### <span data-ttu-id="cadb5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cadb5-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="cadb5-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cadb5-109">PARAMETERS</span></span>

### <span data-ttu-id="cadb5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cadb5-110">-DefaultProfile</span></span>
<span data-ttu-id="cadb5-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cadb5-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cadb5-112">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cadb5-112">-Name</span></span>
<span data-ttu-id="cadb5-113">Nazwa klawisza klastrowego Cassandra.</span><span class="sxs-lookup"><span data-stu-id="cadb5-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="cadb5-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="cadb5-114">-OrderBy</span></span>
<span data-ttu-id="cadb5-115">Ordering of Cassandra Cluster key.</span><span class="sxs-lookup"><span data-stu-id="cadb5-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="cadb5-116">Możliwe wartości: "Asc", "Desc"</span><span class="sxs-lookup"><span data-stu-id="cadb5-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="cadb5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cadb5-117">CommonParameters</span></span>
<span data-ttu-id="cadb5-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cadb5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cadb5-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cadb5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cadb5-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cadb5-120">INPUTS</span></span>

### <span data-ttu-id="cadb5-121">Brak</span><span class="sxs-lookup"><span data-stu-id="cadb5-121">None</span></span>

## <span data-ttu-id="cadb5-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cadb5-122">OUTPUTS</span></span>

### <span data-ttu-id="cadb5-123">Microsoft.Azure.Commands.DoceńDB.Models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="cadb5-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="cadb5-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cadb5-124">NOTES</span></span>

## <span data-ttu-id="cadb5-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cadb5-125">RELATED LINKS</span></span>
