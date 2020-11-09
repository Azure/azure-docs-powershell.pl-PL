---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307135"
---
# <span data-ttu-id="ec61e-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="ec61e-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="ec61e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec61e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec61e-103">Tworzy nową kolumnę Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ec61e-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="ec61e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec61e-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec61e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ec61e-105">DESCRIPTION</span></span>
<span data-ttu-id="ec61e-106">**Nowy-AzCosmosDBCassandraColumn** tworzy nową CosmosDB Cassandra Column.</span><span class="sxs-lookup"><span data-stu-id="ec61e-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="ec61e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec61e-107">EXAMPLES</span></span>

### <span data-ttu-id="ec61e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ec61e-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="ec61e-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec61e-109">PARAMETERS</span></span>

### <span data-ttu-id="ec61e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec61e-110">-DefaultProfile</span></span>
<span data-ttu-id="ec61e-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec61e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec61e-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ec61e-112">-Name</span></span>
<span data-ttu-id="ec61e-113">Nazwa kolumny Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ec61e-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="ec61e-114">-Type</span><span class="sxs-lookup"><span data-stu-id="ec61e-114">-Type</span></span>
<span data-ttu-id="ec61e-115">Typ kolumny Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ec61e-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="ec61e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec61e-116">CommonParameters</span></span>
<span data-ttu-id="ec61e-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec61e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec61e-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec61e-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec61e-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec61e-119">INPUTS</span></span>

### <span data-ttu-id="ec61e-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ec61e-120">None</span></span>

## <span data-ttu-id="ec61e-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec61e-121">OUTPUTS</span></span>

### <span data-ttu-id="ec61e-122">Microsoft. Azure. Commands. CosmosDB. models. PSColumn</span><span class="sxs-lookup"><span data-stu-id="ec61e-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="ec61e-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec61e-123">NOTES</span></span>

## <span data-ttu-id="ec61e-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec61e-124">RELATED LINKS</span></span>
