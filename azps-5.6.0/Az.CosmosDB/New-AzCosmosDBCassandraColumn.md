---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 634a6a8e1e6b921703603ee7f2bfd345aa64608c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010769"
---
# <span data-ttu-id="d6464-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="d6464-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="d6464-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6464-102">SYNOPSIS</span></span>
<span data-ttu-id="d6464-103">Tworzy nową kolumnę CassandraDb.</span><span class="sxs-lookup"><span data-stu-id="d6464-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="d6464-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6464-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6464-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6464-105">DESCRIPTION</span></span>
<span data-ttu-id="d6464-106">Kolumny **New-AzCosmosDBCassandraColumn** tworzą nową kolumnę CassandraDb.</span><span class="sxs-lookup"><span data-stu-id="d6464-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="d6464-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6464-107">EXAMPLES</span></span>

### <span data-ttu-id="d6464-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6464-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="d6464-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6464-109">PARAMETERS</span></span>

### <span data-ttu-id="d6464-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6464-110">-DefaultProfile</span></span>
<span data-ttu-id="d6464-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6464-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6464-112">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d6464-112">-Name</span></span>
<span data-ttu-id="d6464-113">Nazwa kolumny Cassandra.</span><span class="sxs-lookup"><span data-stu-id="d6464-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="d6464-114">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="d6464-114">-Type</span></span>
<span data-ttu-id="d6464-115">Typ kolumny Cassandra.</span><span class="sxs-lookup"><span data-stu-id="d6464-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="d6464-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6464-116">CommonParameters</span></span>
<span data-ttu-id="d6464-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6464-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6464-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6464-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6464-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6464-119">INPUTS</span></span>

### <span data-ttu-id="d6464-120">Brak</span><span class="sxs-lookup"><span data-stu-id="d6464-120">None</span></span>

## <span data-ttu-id="d6464-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6464-121">OUTPUTS</span></span>

### <span data-ttu-id="d6464-122">Microsoft.Azure.Commands.DoceńDB.Models.PSColumn</span><span class="sxs-lookup"><span data-stu-id="d6464-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="d6464-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6464-123">NOTES</span></span>

## <span data-ttu-id="d6464-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6464-124">RELATED LINKS</span></span>
