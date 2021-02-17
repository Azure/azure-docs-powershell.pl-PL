---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177298"
---
# <span data-ttu-id="7d8ae-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="7d8ae-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="7d8ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8ae-103">Tworzy nowy schemat Cassandrydy Omyłka.</span><span class="sxs-lookup"><span data-stu-id="7d8ae-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="7d8ae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7d8ae-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d8ae-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7d8ae-105">DESCRIPTION</span></span>
<span data-ttu-id="7d8ae-106">**New-AzCosmosDBCassandraSchema** tworzy nowy schemat Cassandradrydydydb.</span><span class="sxs-lookup"><span data-stu-id="7d8ae-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="7d8ae-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7d8ae-107">EXAMPLES</span></span>

### <span data-ttu-id="7d8ae-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7d8ae-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="7d8ae-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d8ae-109">PARAMETERS</span></span>

### <span data-ttu-id="7d8ae-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="7d8ae-110">-ClusterKey</span></span>
<span data-ttu-id="7d8ae-111">Tablica obiektów PSClusterKey.</span><span class="sxs-lookup"><span data-stu-id="7d8ae-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="7d8ae-112">- Kolumna</span><span class="sxs-lookup"><span data-stu-id="7d8ae-112">-Column</span></span>
<span data-ttu-id="7d8ae-113">Obiekt PSColumn.</span><span class="sxs-lookup"><span data-stu-id="7d8ae-113">PSColumn object.</span></span>

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

### <span data-ttu-id="7d8ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8ae-114">-DefaultProfile</span></span>
<span data-ttu-id="7d8ae-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8ae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d8ae-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="7d8ae-116">-PartitionKey</span></span>
<span data-ttu-id="7d8ae-117">Tablica ciągów zawierających klawisze partycji.</span><span class="sxs-lookup"><span data-stu-id="7d8ae-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="7d8ae-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8ae-118">CommonParameters</span></span>
<span data-ttu-id="7d8ae-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d8ae-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8ae-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d8ae-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8ae-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d8ae-121">INPUTS</span></span>

### <span data-ttu-id="7d8ae-122">Brak</span><span class="sxs-lookup"><span data-stu-id="7d8ae-122">None</span></span>

## <span data-ttu-id="7d8ae-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d8ae-123">OUTPUTS</span></span>

### <span data-ttu-id="7d8ae-124">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="7d8ae-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="7d8ae-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7d8ae-125">NOTES</span></span>

## <span data-ttu-id="7d8ae-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d8ae-126">RELATED LINKS</span></span>
