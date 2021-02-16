---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199002"
---
# <span data-ttu-id="b713c-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="b713c-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="b713c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b713c-102">SYNOPSIS</span></span>
<span data-ttu-id="b713c-103">Pobiera ustawienia przepływności odpowiadające bazom danych Sql Dla Firmy A1.</span><span class="sxs-lookup"><span data-stu-id="b713c-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="b713c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b713c-104">SYNTAX</span></span>

### <span data-ttu-id="b713c-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b713c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b713c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b713c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b713c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b713c-107">DESCRIPTION</span></span>
<span data-ttu-id="b713c-108">Polecenie **cmdlet Get-AzCosmosDBSqlDatabaseThroughput** pobiera ustawienia przepływności odpowiadające bazie danych Sql DlaSDB.</span><span class="sxs-lookup"><span data-stu-id="b713c-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="b713c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b713c-109">EXAMPLES</span></span>

### <span data-ttu-id="b713c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b713c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="b713c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b713c-111">PARAMETERS</span></span>

### <span data-ttu-id="b713c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b713c-112">-AccountName</span></span>
<span data-ttu-id="b713c-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="b713c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b713c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b713c-114">-DefaultProfile</span></span>
<span data-ttu-id="b713c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b713c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b713c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b713c-116">-InputObject</span></span>
<span data-ttu-id="b713c-117">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="b713c-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b713c-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b713c-118">-Name</span></span>
<span data-ttu-id="b713c-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b713c-119">Database name.</span></span>

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

### <span data-ttu-id="b713c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b713c-120">-ResourceGroupName</span></span>
<span data-ttu-id="b713c-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b713c-121">Name of resource group.</span></span>

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

### <span data-ttu-id="b713c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b713c-122">CommonParameters</span></span>
<span data-ttu-id="b713c-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b713c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b713c-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b713c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b713c-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b713c-125">INPUTS</span></span>

### <span data-ttu-id="b713c-126">Brak</span><span class="sxs-lookup"><span data-stu-id="b713c-126">None</span></span>

## <span data-ttu-id="b713c-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b713c-127">OUTPUTS</span></span>

### <span data-ttu-id="b713c-128">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b713c-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b713c-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b713c-129">NOTES</span></span>

## <span data-ttu-id="b713c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b713c-130">RELATED LINKS</span></span>
