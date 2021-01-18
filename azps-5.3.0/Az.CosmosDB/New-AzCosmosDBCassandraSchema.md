---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501744"
---
# <span data-ttu-id="c2be9-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="c2be9-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="c2be9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2be9-102">SYNOPSIS</span></span>
<span data-ttu-id="c2be9-103">Tworzy nowy schemat Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c2be9-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="c2be9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2be9-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2be9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2be9-105">DESCRIPTION</span></span>
<span data-ttu-id="c2be9-106">**Nowy-AzCosmosDBCassandraSchema** tworzy nowy CosmosDB Cassandra Schema.</span><span class="sxs-lookup"><span data-stu-id="c2be9-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="c2be9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2be9-107">EXAMPLES</span></span>

### <span data-ttu-id="c2be9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2be9-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="c2be9-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2be9-109">PARAMETERS</span></span>

### <span data-ttu-id="c2be9-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="c2be9-110">-ClusterKey</span></span>
<span data-ttu-id="c2be9-111">Tablica obiektów PSClusterKey.</span><span class="sxs-lookup"><span data-stu-id="c2be9-111">Array of PSClusterKey objects.</span></span>

```yaml
Type: PSClusterKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2be9-112">-Kolumnowy</span><span class="sxs-lookup"><span data-stu-id="c2be9-112">-Column</span></span>
<span data-ttu-id="c2be9-113">Obiekt PSColumn.</span><span class="sxs-lookup"><span data-stu-id="c2be9-113">PSColumn object.</span></span>

```yaml
Type: PSColumn[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2be9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2be9-114">-DefaultProfile</span></span>
<span data-ttu-id="c2be9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2be9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2be9-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="c2be9-116">-PartitionKey</span></span>
<span data-ttu-id="c2be9-117">Tablica ciągów zawierająca klucze partycji.</span><span class="sxs-lookup"><span data-stu-id="c2be9-117">Array of strings containing Partition Keys.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2be9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2be9-118">CommonParameters</span></span>
<span data-ttu-id="c2be9-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2be9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2be9-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2be9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2be9-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2be9-121">INPUTS</span></span>

### <span data-ttu-id="c2be9-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c2be9-122">None</span></span>

## <span data-ttu-id="c2be9-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2be9-123">OUTPUTS</span></span>

### <span data-ttu-id="c2be9-124">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="c2be9-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="c2be9-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2be9-125">NOTES</span></span>

## <span data-ttu-id="c2be9-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2be9-126">RELATED LINKS</span></span>
