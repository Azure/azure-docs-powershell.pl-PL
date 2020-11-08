---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064224"
---
# <span data-ttu-id="0da4d-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="0da4d-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="0da4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0da4d-102">SYNOPSIS</span></span>
<span data-ttu-id="0da4d-103">Tworzy nową kolumnę Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0da4d-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="0da4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0da4d-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0da4d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0da4d-105">DESCRIPTION</span></span>
<span data-ttu-id="0da4d-106">**Nowy-AzCosmosDBCassandraColumn** tworzy nową CosmosDB Cassandra Column.</span><span class="sxs-lookup"><span data-stu-id="0da4d-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="0da4d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0da4d-107">EXAMPLES</span></span>

### <span data-ttu-id="0da4d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0da4d-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="0da4d-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0da4d-109">PARAMETERS</span></span>

### <span data-ttu-id="0da4d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da4d-110">-DefaultProfile</span></span>
<span data-ttu-id="0da4d-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0da4d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0da4d-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0da4d-112">-Name</span></span>
<span data-ttu-id="0da4d-113">Nazwa kolumny Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0da4d-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="0da4d-114">-Type</span><span class="sxs-lookup"><span data-stu-id="0da4d-114">-Type</span></span>
<span data-ttu-id="0da4d-115">Typ kolumny Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0da4d-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="0da4d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da4d-116">CommonParameters</span></span>
<span data-ttu-id="0da4d-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da4d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da4d-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0da4d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da4d-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0da4d-119">INPUTS</span></span>

### <span data-ttu-id="0da4d-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0da4d-120">None</span></span>

## <span data-ttu-id="0da4d-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0da4d-121">OUTPUTS</span></span>

### <span data-ttu-id="0da4d-122">Microsoft. Azure. Commands. CosmosDB. models. PSColumn</span><span class="sxs-lookup"><span data-stu-id="0da4d-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="0da4d-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0da4d-123">NOTES</span></span>

## <span data-ttu-id="0da4d-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0da4d-124">RELATED LINKS</span></span>
