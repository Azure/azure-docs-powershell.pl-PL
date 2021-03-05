---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 28b616315913ae70722b5a600d4b10879c7b8334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986910"
---
# <span data-ttu-id="24cf1-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="24cf1-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="24cf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="24cf1-103">Pobiera wyzwalacz języka SQL DossDB.</span><span class="sxs-lookup"><span data-stu-id="24cf1-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="24cf1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="24cf1-104">SYNTAX</span></span>

### <span data-ttu-id="24cf1-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="24cf1-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24cf1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24cf1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24cf1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="24cf1-107">DESCRIPTION</span></span>
<span data-ttu-id="24cf1-108">Polecenie cmdlet **Get-AzCosmosDBSqlTrigger** pobiera listę wszystkich istniejących wyzwalaczy sql dla aleji ResourceGroupName, AccountName, DatabaseName i ContainerName oraz otrzymuje jeden wyzwalacz sql dla danej nazwy ResourceGroupName, AccountName, DatabaseName, ContainerName i TriggerName.</span><span class="sxs-lookup"><span data-stu-id="24cf1-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="24cf1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="24cf1-109">EXAMPLES</span></span>

### <span data-ttu-id="24cf1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24cf1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="24cf1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24cf1-111">PARAMETERS</span></span>

### <span data-ttu-id="24cf1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24cf1-112">-AccountName</span></span>
<span data-ttu-id="24cf1-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="24cf1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="24cf1-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="24cf1-114">-ContainerName</span></span>
<span data-ttu-id="24cf1-115">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="24cf1-115">Container name.</span></span>

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

### <span data-ttu-id="24cf1-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="24cf1-116">-DatabaseName</span></span>
<span data-ttu-id="24cf1-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="24cf1-117">Database name.</span></span>

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

### <span data-ttu-id="24cf1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cf1-118">-DefaultProfile</span></span>
<span data-ttu-id="24cf1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="24cf1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24cf1-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="24cf1-120">-Name</span></span>
<span data-ttu-id="24cf1-121">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="24cf1-121">Trigger name.</span></span>

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

### <span data-ttu-id="24cf1-122">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="24cf1-122">-ParentObject</span></span>
<span data-ttu-id="24cf1-123">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="24cf1-123">Sql Container object.</span></span>

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

### <span data-ttu-id="24cf1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24cf1-124">-ResourceGroupName</span></span>
<span data-ttu-id="24cf1-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="24cf1-125">Name of resource group.</span></span>

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

### <span data-ttu-id="24cf1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cf1-126">CommonParameters</span></span>
<span data-ttu-id="24cf1-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24cf1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cf1-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24cf1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cf1-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24cf1-129">INPUTS</span></span>

### <span data-ttu-id="24cf1-130">Brak</span><span class="sxs-lookup"><span data-stu-id="24cf1-130">None</span></span>

## <span data-ttu-id="24cf1-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24cf1-131">OUTPUTS</span></span>

### <span data-ttu-id="24cf1-132">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="24cf1-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="24cf1-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="24cf1-133">NOTES</span></span>

## <span data-ttu-id="24cf1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24cf1-134">RELATED LINKS</span></span>
