---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6631cad83260a935f2849391941ec0cf6514b188
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049526"
---
# <span data-ttu-id="2febb-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="2febb-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="2febb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2febb-102">SYNOPSIS</span></span>
<span data-ttu-id="2febb-103">Pobiera wyzwalacz SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2febb-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="2febb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2febb-104">SYNTAX</span></span>

### <span data-ttu-id="2febb-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2febb-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2febb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2febb-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2febb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2febb-107">DESCRIPTION</span></span>
<span data-ttu-id="2febb-108">Polecenie cmdlet **Get-AzCosmosDBSqlTrigger** pobiera listę wszystkich istniejących wyzwalaczy SQL CosmosDB dla danego ResourceGroupName, AccountName, DatabaseName oraz ContainerName i pobiera jeden wyzwalacz CosmosDB SQL dla danego elementu ResourceGroupName, AccountName, DatabaseName, ContainerName i triggername.</span><span class="sxs-lookup"><span data-stu-id="2febb-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="2febb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2febb-109">EXAMPLES</span></span>

### <span data-ttu-id="2febb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2febb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="2febb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2febb-111">PARAMETERS</span></span>

### <span data-ttu-id="2febb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2febb-112">-AccountName</span></span>
<span data-ttu-id="2febb-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2febb-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2febb-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="2febb-114">-ContainerName</span></span>
<span data-ttu-id="2febb-115">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="2febb-115">Container name.</span></span>

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

### <span data-ttu-id="2febb-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2febb-116">-DatabaseName</span></span>
<span data-ttu-id="2febb-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2febb-117">Database name.</span></span>

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

### <span data-ttu-id="2febb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2febb-118">-DefaultProfile</span></span>
<span data-ttu-id="2febb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2febb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2febb-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2febb-120">-InputObject</span></span>
<span data-ttu-id="2febb-121">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="2febb-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2febb-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2febb-122">-Name</span></span>
<span data-ttu-id="2febb-123">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="2febb-123">Trigger name.</span></span>

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

### <span data-ttu-id="2febb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2febb-124">-ResourceGroupName</span></span>
<span data-ttu-id="2febb-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2febb-125">Name of resource group.</span></span>

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

### <span data-ttu-id="2febb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2febb-126">CommonParameters</span></span>
<span data-ttu-id="2febb-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2febb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2febb-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2febb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2febb-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2febb-129">INPUTS</span></span>

### <span data-ttu-id="2febb-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2febb-130">None</span></span>

## <span data-ttu-id="2febb-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2febb-131">OUTPUTS</span></span>

### <span data-ttu-id="2febb-132">Microsoft. Azure. Commands. CosmosDB. models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="2febb-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="2febb-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2febb-133">NOTES</span></span>

## <span data-ttu-id="2febb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2febb-134">RELATED LINKS</span></span>
