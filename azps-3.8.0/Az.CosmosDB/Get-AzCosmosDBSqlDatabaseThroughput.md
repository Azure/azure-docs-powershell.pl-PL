---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 9ba9c092f021041f1a56626a79e07b369b694d5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049528"
---
# <span data-ttu-id="a4476-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="a4476-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="a4476-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4476-102">SYNOPSIS</span></span>
<span data-ttu-id="a4476-103">Pobiera ustawienia przepływności odpowiadające bazie danych SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a4476-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="a4476-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4476-104">SYNTAX</span></span>

### <span data-ttu-id="a4476-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a4476-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4476-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4476-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4476-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a4476-107">DESCRIPTION</span></span>
<span data-ttu-id="a4476-108">Polecenie cmdlet **Get-AzCosmosDBSqlDatabaseThroughput** pobiera ustawienia przepływności odpowiadające bazie danych CosmosDB SQL.</span><span class="sxs-lookup"><span data-stu-id="a4476-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="a4476-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4476-109">EXAMPLES</span></span>

### <span data-ttu-id="a4476-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4476-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="a4476-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4476-111">PARAMETERS</span></span>

### <span data-ttu-id="a4476-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a4476-112">-AccountName</span></span>
<span data-ttu-id="a4476-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="a4476-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a4476-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4476-114">-DefaultProfile</span></span>
<span data-ttu-id="a4476-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4476-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4476-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a4476-116">-InputObject</span></span>
<span data-ttu-id="a4476-117">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="a4476-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4476-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4476-118">-Name</span></span>
<span data-ttu-id="a4476-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a4476-119">Database name.</span></span>

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

### <span data-ttu-id="a4476-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4476-120">-ResourceGroupName</span></span>
<span data-ttu-id="a4476-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4476-121">Name of resource group.</span></span>

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

### <span data-ttu-id="a4476-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4476-122">CommonParameters</span></span>
<span data-ttu-id="a4476-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4476-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4476-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4476-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4476-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4476-125">INPUTS</span></span>

### <span data-ttu-id="a4476-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a4476-126">None</span></span>

## <span data-ttu-id="a4476-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4476-127">OUTPUTS</span></span>

### <span data-ttu-id="a4476-128">Microsoft. Azure. Commands. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a4476-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a4476-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4476-129">NOTES</span></span>

## <span data-ttu-id="a4476-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4476-130">RELATED LINKS</span></span>
