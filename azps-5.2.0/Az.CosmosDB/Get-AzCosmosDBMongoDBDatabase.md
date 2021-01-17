---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322252"
---
# <span data-ttu-id="21c68-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="21c68-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="21c68-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21c68-102">SYNOPSIS</span></span>
<span data-ttu-id="21c68-103">Pobiera bazę danych MongoDB CosmosDB</span><span class="sxs-lookup"><span data-stu-id="21c68-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="21c68-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21c68-104">SYNTAX</span></span>

### <span data-ttu-id="21c68-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="21c68-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21c68-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21c68-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21c68-107">Opis</span><span class="sxs-lookup"><span data-stu-id="21c68-107">DESCRIPTION</span></span>
<span data-ttu-id="21c68-108">Polecenie cmdlet **Get-AzCosmosDBMongoDBDatabase** pobiera bazę danych CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="21c68-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="21c68-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21c68-109">EXAMPLES</span></span>

### <span data-ttu-id="21c68-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21c68-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="21c68-111">Obiekt zasobu zawiera _rid, _ts, właściwości _etag.</span><span class="sxs-lookup"><span data-stu-id="21c68-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="21c68-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21c68-112">PARAMETERS</span></span>

### <span data-ttu-id="21c68-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="21c68-113">-AccountName</span></span>
<span data-ttu-id="21c68-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="21c68-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="21c68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c68-115">-DefaultProfile</span></span>
<span data-ttu-id="21c68-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21c68-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21c68-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21c68-117">-Name</span></span>
<span data-ttu-id="21c68-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="21c68-118">Database name.</span></span>

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

### <span data-ttu-id="21c68-119">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="21c68-119">-ParentObject</span></span>
<span data-ttu-id="21c68-120">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="21c68-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="21c68-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c68-121">-ResourceGroupName</span></span>
<span data-ttu-id="21c68-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21c68-122">Name of resource group.</span></span>

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

### <span data-ttu-id="21c68-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c68-123">CommonParameters</span></span>
<span data-ttu-id="21c68-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21c68-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c68-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21c68-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c68-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21c68-126">INPUTS</span></span>

### <span data-ttu-id="21c68-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="21c68-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="21c68-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21c68-128">OUTPUTS</span></span>

### <span data-ttu-id="21c68-129">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="21c68-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="21c68-130">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="21c68-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="21c68-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21c68-131">NOTES</span></span>

## <span data-ttu-id="21c68-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21c68-132">RELATED LINKS</span></span>
