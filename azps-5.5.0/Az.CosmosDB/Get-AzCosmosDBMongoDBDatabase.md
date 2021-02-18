---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181394"
---
# <span data-ttu-id="fb837-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="fb837-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="fb837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb837-102">SYNOPSIS</span></span>
<span data-ttu-id="fb837-103">Pobiera bazę danych DoSDB MongoDB</span><span class="sxs-lookup"><span data-stu-id="fb837-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="fb837-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fb837-104">SYNTAX</span></span>

### <span data-ttu-id="fb837-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="fb837-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb837-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb837-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb837-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fb837-107">DESCRIPTION</span></span>
<span data-ttu-id="fb837-108">Polecenie **cmdlet Get-AzCosmosDBMongoDBDatabase** pobiera bazę danych DosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="fb837-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="fb837-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fb837-109">EXAMPLES</span></span>

### <span data-ttu-id="fb837-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb837-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="fb837-111">Obiekt zasobu _rid, _ts, _etag właściwości.</span><span class="sxs-lookup"><span data-stu-id="fb837-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="fb837-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb837-112">PARAMETERS</span></span>

### <span data-ttu-id="fb837-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fb837-113">-AccountName</span></span>
<span data-ttu-id="fb837-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="fb837-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fb837-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb837-115">-DefaultProfile</span></span>
<span data-ttu-id="fb837-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb837-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb837-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fb837-117">-Name</span></span>
<span data-ttu-id="fb837-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fb837-118">Database name.</span></span>

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

### <span data-ttu-id="fb837-119">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="fb837-119">-ParentObject</span></span>
<span data-ttu-id="fb837-120">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="fb837-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fb837-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb837-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb837-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb837-122">Name of resource group.</span></span>

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

### <span data-ttu-id="fb837-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb837-123">CommonParameters</span></span>
<span data-ttu-id="fb837-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb837-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb837-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb837-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb837-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb837-126">INPUTS</span></span>

### <span data-ttu-id="fb837-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="fb837-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="fb837-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb837-128">OUTPUTS</span></span>

### <span data-ttu-id="fb837-129">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="fb837-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="fb837-130">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="fb837-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fb837-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fb837-131">NOTES</span></span>

## <span data-ttu-id="fb837-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb837-132">RELATED LINKS</span></span>
