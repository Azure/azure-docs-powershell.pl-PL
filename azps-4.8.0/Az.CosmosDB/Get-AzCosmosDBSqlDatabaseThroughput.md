---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221840"
---
# <span data-ttu-id="85d7a-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="85d7a-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="85d7a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="85d7a-103">Pobiera ustawienia przepływności odpowiadające bazie danych SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="85d7a-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="85d7a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85d7a-104">SYNTAX</span></span>

### <span data-ttu-id="85d7a-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="85d7a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85d7a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85d7a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85d7a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="85d7a-107">DESCRIPTION</span></span>
<span data-ttu-id="85d7a-108">Polecenie cmdlet **Get-AzCosmosDBSqlDatabaseThroughput** pobiera ustawienia przepływności odpowiadające bazie danych CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="85d7a-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="85d7a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85d7a-109">EXAMPLES</span></span>

### <span data-ttu-id="85d7a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="85d7a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="85d7a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85d7a-111">PARAMETERS</span></span>

### <span data-ttu-id="85d7a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="85d7a-112">-AccountName</span></span>
<span data-ttu-id="85d7a-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="85d7a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="85d7a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85d7a-114">-DefaultProfile</span></span>
<span data-ttu-id="85d7a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85d7a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85d7a-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="85d7a-116">-InputObject</span></span>
<span data-ttu-id="85d7a-117">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="85d7a-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="85d7a-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85d7a-118">-Name</span></span>
<span data-ttu-id="85d7a-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="85d7a-119">Database name.</span></span>

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

### <span data-ttu-id="85d7a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85d7a-120">-ResourceGroupName</span></span>
<span data-ttu-id="85d7a-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85d7a-121">Name of resource group.</span></span>

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

### <span data-ttu-id="85d7a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85d7a-122">CommonParameters</span></span>
<span data-ttu-id="85d7a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85d7a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85d7a-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85d7a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85d7a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85d7a-125">INPUTS</span></span>

### <span data-ttu-id="85d7a-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="85d7a-126">None</span></span>

## <span data-ttu-id="85d7a-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85d7a-127">OUTPUTS</span></span>

### <span data-ttu-id="85d7a-128">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="85d7a-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="85d7a-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85d7a-129">NOTES</span></span>

## <span data-ttu-id="85d7a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85d7a-130">RELATED LINKS</span></span>
