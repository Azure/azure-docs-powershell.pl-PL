---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307140"
---
# <span data-ttu-id="cf6d5-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="cf6d5-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="cf6d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf6d5-102">SYNOPSIS</span></span>
<span data-ttu-id="cf6d5-103">Tworzy nowy klucz klastra Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="cf6d5-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="cf6d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf6d5-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf6d5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cf6d5-105">DESCRIPTION</span></span>
<span data-ttu-id="cf6d5-106">**Nowy-AzCosmosDBCassandraClusterKey** tworzy nowy klucz klastra CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="cf6d5-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="cf6d5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf6d5-107">EXAMPLES</span></span>

### <span data-ttu-id="cf6d5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cf6d5-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="cf6d5-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf6d5-109">PARAMETERS</span></span>

### <span data-ttu-id="cf6d5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf6d5-110">-DefaultProfile</span></span>
<span data-ttu-id="cf6d5-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf6d5-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf6d5-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cf6d5-112">-Name</span></span>
<span data-ttu-id="cf6d5-113">Nazwa klucza klastra usługi Cassandra.</span><span class="sxs-lookup"><span data-stu-id="cf6d5-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="cf6d5-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="cf6d5-114">-OrderBy</span></span>
<span data-ttu-id="cf6d5-115">Zamawianie klucza klastra Cassandra.</span><span class="sxs-lookup"><span data-stu-id="cf6d5-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="cf6d5-116">Możliwe wartości są następujące: "ASC", "DESC"</span><span class="sxs-lookup"><span data-stu-id="cf6d5-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="cf6d5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf6d5-117">CommonParameters</span></span>
<span data-ttu-id="cf6d5-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf6d5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf6d5-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf6d5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf6d5-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf6d5-120">INPUTS</span></span>

### <span data-ttu-id="cf6d5-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cf6d5-121">None</span></span>

## <span data-ttu-id="cf6d5-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf6d5-122">OUTPUTS</span></span>

### <span data-ttu-id="cf6d5-123">Microsoft. Azure. Commands. CosmosDB. models. PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="cf6d5-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="cf6d5-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf6d5-124">NOTES</span></span>

## <span data-ttu-id="cf6d5-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf6d5-125">RELATED LINKS</span></span>
