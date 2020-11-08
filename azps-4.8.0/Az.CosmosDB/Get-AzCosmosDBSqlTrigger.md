---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94224060"
---
# <span data-ttu-id="5a2ad-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="5a2ad-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="5a2ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="5a2ad-103">Pobiera wyzwalacz SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5a2ad-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="5a2ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a2ad-104">SYNTAX</span></span>

### <span data-ttu-id="5a2ad-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a2ad-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a2ad-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a2ad-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a2ad-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5a2ad-107">DESCRIPTION</span></span>
<span data-ttu-id="5a2ad-108">Polecenie cmdlet **Get-AzCosmosDBSqlTrigger** pobiera listę wszystkich istniejących wyzwalaczy SQL CosmosDB dla danego ResourceGroupName, AccountName, DatabaseName oraz ContainerName i pobiera jeden wyzwalacz CosmosDB SQL dla danego elementu ResourceGroupName, AccountName, DatabaseName, ContainerName i triggername.</span><span class="sxs-lookup"><span data-stu-id="5a2ad-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="5a2ad-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a2ad-109">EXAMPLES</span></span>

### <span data-ttu-id="5a2ad-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a2ad-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="5a2ad-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a2ad-111">PARAMETERS</span></span>

### <span data-ttu-id="5a2ad-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5a2ad-112">-AccountName</span></span>
<span data-ttu-id="5a2ad-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="5a2ad-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5a2ad-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="5a2ad-114">-ContainerName</span></span>
<span data-ttu-id="5a2ad-115">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="5a2ad-115">Container name.</span></span>

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

### <span data-ttu-id="5a2ad-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a2ad-116">-DatabaseName</span></span>
<span data-ttu-id="5a2ad-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="5a2ad-117">Database name.</span></span>

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

### <span data-ttu-id="5a2ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a2ad-118">-DefaultProfile</span></span>
<span data-ttu-id="5a2ad-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a2ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a2ad-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5a2ad-120">-Name</span></span>
<span data-ttu-id="5a2ad-121">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5a2ad-121">Trigger name.</span></span>

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

### <span data-ttu-id="5a2ad-122">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="5a2ad-122">-ParentObject</span></span>
<span data-ttu-id="5a2ad-123">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="5a2ad-123">Sql Container object.</span></span>

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

### <span data-ttu-id="5a2ad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a2ad-124">-ResourceGroupName</span></span>
<span data-ttu-id="5a2ad-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5a2ad-125">Name of resource group.</span></span>

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

### <span data-ttu-id="5a2ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a2ad-126">CommonParameters</span></span>
<span data-ttu-id="5a2ad-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a2ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a2ad-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a2ad-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a2ad-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a2ad-129">INPUTS</span></span>

### <span data-ttu-id="5a2ad-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5a2ad-130">None</span></span>

## <span data-ttu-id="5a2ad-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a2ad-131">OUTPUTS</span></span>

### <span data-ttu-id="5a2ad-132">Microsoft. Azure. Commands. CosmosDB. models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="5a2ad-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="5a2ad-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a2ad-133">NOTES</span></span>

## <span data-ttu-id="5a2ad-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a2ad-134">RELATED LINKS</span></span>
