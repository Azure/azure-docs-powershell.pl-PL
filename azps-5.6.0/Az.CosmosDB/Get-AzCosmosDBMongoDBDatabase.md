---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 0dfcffe55eb3214f4be9d6ccfb34231d1c9ea50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994470"
---
# <span data-ttu-id="56a84-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="56a84-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="56a84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56a84-102">SYNOPSIS</span></span>
<span data-ttu-id="56a84-103">Pobiera bazę danych MongoDB</span><span class="sxs-lookup"><span data-stu-id="56a84-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="56a84-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="56a84-104">SYNTAX</span></span>

### <span data-ttu-id="56a84-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="56a84-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56a84-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56a84-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56a84-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="56a84-107">DESCRIPTION</span></span>
<span data-ttu-id="56a84-108">Polecenie **cmdlet Get-AzCosmosDBMongoDBDatabase** pobiera bazę danych DosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="56a84-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="56a84-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="56a84-109">EXAMPLES</span></span>

### <span data-ttu-id="56a84-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="56a84-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="56a84-111">Obiekt zasobu _rid, _ts, _etag właściwości.</span><span class="sxs-lookup"><span data-stu-id="56a84-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="56a84-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56a84-112">PARAMETERS</span></span>

### <span data-ttu-id="56a84-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="56a84-113">-AccountName</span></span>
<span data-ttu-id="56a84-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="56a84-114">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56a84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56a84-115">-DefaultProfile</span></span>
<span data-ttu-id="56a84-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="56a84-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56a84-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="56a84-117">-Name</span></span>
<span data-ttu-id="56a84-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="56a84-118">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56a84-119">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="56a84-119">-ParentObject</span></span>
<span data-ttu-id="56a84-120">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="56a84-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56a84-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56a84-121">-ResourceGroupName</span></span>
<span data-ttu-id="56a84-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="56a84-122">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56a84-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56a84-123">CommonParameters</span></span>
<span data-ttu-id="56a84-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56a84-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56a84-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56a84-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56a84-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56a84-126">INPUTS</span></span>

### <span data-ttu-id="56a84-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="56a84-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="56a84-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56a84-128">OUTPUTS</span></span>

### <span data-ttu-id="56a84-129">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="56a84-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="56a84-130">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="56a84-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="56a84-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="56a84-131">NOTES</span></span>

## <span data-ttu-id="56a84-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56a84-132">RELATED LINKS</span></span>
