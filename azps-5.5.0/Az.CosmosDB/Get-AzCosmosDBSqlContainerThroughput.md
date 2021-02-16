---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199018"
---
# <span data-ttu-id="c98a7-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="c98a7-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="c98a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c98a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c98a7-103">Pobiera ustawienia przepływności odpowiadające kontenerowi sql w formacie AADB.</span><span class="sxs-lookup"><span data-stu-id="c98a7-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="c98a7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c98a7-104">SYNTAX</span></span>

### <span data-ttu-id="c98a7-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c98a7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c98a7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c98a7-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c98a7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c98a7-107">DESCRIPTION</span></span>
<span data-ttu-id="c98a7-108">Polecenie **cmdlet Get-AzCosmosDBSqlContainerThroughput** pobiera ustawienia przepływności odpowiadające kontenerowi sql Dla firmy ADB.</span><span class="sxs-lookup"><span data-stu-id="c98a7-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="c98a7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c98a7-109">EXAMPLES</span></span>

### <span data-ttu-id="c98a7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c98a7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="c98a7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c98a7-111">PARAMETERS</span></span>

### <span data-ttu-id="c98a7-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c98a7-112">-AccountName</span></span>
<span data-ttu-id="c98a7-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="c98a7-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c98a7-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c98a7-114">-DatabaseName</span></span>
<span data-ttu-id="c98a7-115">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c98a7-115">Database name.</span></span>

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

### <span data-ttu-id="c98a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c98a7-116">-DefaultProfile</span></span>
<span data-ttu-id="c98a7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c98a7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c98a7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c98a7-118">-InputObject</span></span>
<span data-ttu-id="c98a7-119">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="c98a7-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c98a7-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c98a7-120">-Name</span></span>
<span data-ttu-id="c98a7-121">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="c98a7-121">Container name.</span></span>

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

### <span data-ttu-id="c98a7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c98a7-122">-ResourceGroupName</span></span>
<span data-ttu-id="c98a7-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c98a7-123">Name of resource group.</span></span>

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

### <span data-ttu-id="c98a7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98a7-124">CommonParameters</span></span>
<span data-ttu-id="c98a7-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c98a7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98a7-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c98a7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98a7-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c98a7-127">INPUTS</span></span>

### <span data-ttu-id="c98a7-128">Brak</span><span class="sxs-lookup"><span data-stu-id="c98a7-128">None</span></span>

## <span data-ttu-id="c98a7-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c98a7-129">OUTPUTS</span></span>

### <span data-ttu-id="c98a7-130">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c98a7-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c98a7-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c98a7-131">NOTES</span></span>

## <span data-ttu-id="c98a7-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c98a7-132">RELATED LINKS</span></span>
