---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 5bf35b43db1f1d961f24c1aa2c75c9f17c333345
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958858"
---
# <span data-ttu-id="f5c33-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="f5c33-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="f5c33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5c33-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c33-103">Pobiera ustawienia przepływności odpowiadające bazom danych Sql Dla DlaSDB.</span><span class="sxs-lookup"><span data-stu-id="f5c33-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="f5c33-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f5c33-104">SYNTAX</span></span>

### <span data-ttu-id="f5c33-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f5c33-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5c33-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5c33-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5c33-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f5c33-107">DESCRIPTION</span></span>
<span data-ttu-id="f5c33-108">Polecenie **cmdlet Get-AzCosmosDBSqlDatabaseThroughput** pobiera ustawienia przepływności odpowiadające bazie danych Sql DlaSDB.</span><span class="sxs-lookup"><span data-stu-id="f5c33-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="f5c33-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f5c33-109">EXAMPLES</span></span>

### <span data-ttu-id="f5c33-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f5c33-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="f5c33-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5c33-111">PARAMETERS</span></span>

### <span data-ttu-id="f5c33-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5c33-112">-AccountName</span></span>
<span data-ttu-id="f5c33-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="f5c33-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f5c33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c33-114">-DefaultProfile</span></span>
<span data-ttu-id="f5c33-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5c33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5c33-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5c33-116">-InputObject</span></span>
<span data-ttu-id="f5c33-117">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="f5c33-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5c33-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f5c33-118">-Name</span></span>
<span data-ttu-id="f5c33-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f5c33-119">Database name.</span></span>

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

### <span data-ttu-id="f5c33-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5c33-120">-ResourceGroupName</span></span>
<span data-ttu-id="f5c33-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f5c33-121">Name of resource group.</span></span>

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

### <span data-ttu-id="f5c33-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c33-122">CommonParameters</span></span>
<span data-ttu-id="f5c33-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5c33-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c33-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5c33-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c33-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5c33-125">INPUTS</span></span>

### <span data-ttu-id="f5c33-126">Brak</span><span class="sxs-lookup"><span data-stu-id="f5c33-126">None</span></span>

## <span data-ttu-id="f5c33-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5c33-127">OUTPUTS</span></span>

### <span data-ttu-id="f5c33-128">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f5c33-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f5c33-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f5c33-129">NOTES</span></span>

## <span data-ttu-id="f5c33-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5c33-130">RELATED LINKS</span></span>
