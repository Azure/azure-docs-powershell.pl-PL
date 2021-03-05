---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 6d0fe9565a969de19234d65378fd91a1af7a327f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015370"
---
# <span data-ttu-id="7fc86-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7fc86-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="7fc86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fc86-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc86-103">Pobiera bazę danych SqlsDB.</span><span class="sxs-lookup"><span data-stu-id="7fc86-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="7fc86-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7fc86-104">SYNTAX</span></span>

### <span data-ttu-id="7fc86-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7fc86-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fc86-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fc86-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fc86-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7fc86-107">DESCRIPTION</span></span>
<span data-ttu-id="7fc86-108">Polecenie cmdlet **Get-AzCosmosDBSqlDatabase** pobiera listę wszystkich istniejących baz danych Sql dla domeny ResourceGroupName, AccountName i otrzymuje pojedynczą bazę danych Sql dla nazwa ResourceGroupName, AccountName, DatabaseName i ContainerName.</span><span class="sxs-lookup"><span data-stu-id="7fc86-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="7fc86-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7fc86-109">EXAMPLES</span></span>

### <span data-ttu-id="7fc86-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7fc86-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="7fc86-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fc86-111">PARAMETERS</span></span>

### <span data-ttu-id="7fc86-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7fc86-112">-AccountName</span></span>
<span data-ttu-id="7fc86-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="7fc86-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7fc86-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc86-114">-DefaultProfile</span></span>
<span data-ttu-id="7fc86-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc86-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fc86-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7fc86-116">-Name</span></span>
<span data-ttu-id="7fc86-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7fc86-117">Database name.</span></span>

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

### <span data-ttu-id="7fc86-118">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="7fc86-118">-ParentObject</span></span>
<span data-ttu-id="7fc86-119">Obiekt Account (Konto)</span><span class="sxs-lookup"><span data-stu-id="7fc86-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7fc86-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fc86-120">-ResourceGroupName</span></span>
<span data-ttu-id="7fc86-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7fc86-121">Name of resource group.</span></span>

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

### <span data-ttu-id="7fc86-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc86-122">CommonParameters</span></span>
<span data-ttu-id="7fc86-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fc86-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc86-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fc86-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc86-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fc86-125">INPUTS</span></span>

### <span data-ttu-id="7fc86-126">Brak</span><span class="sxs-lookup"><span data-stu-id="7fc86-126">None</span></span>

## <span data-ttu-id="7fc86-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fc86-127">OUTPUTS</span></span>

### <span data-ttu-id="7fc86-128">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7fc86-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="7fc86-129">Microsoft.Azure.Commands.DoceńDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7fc86-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7fc86-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7fc86-130">NOTES</span></span>

## <span data-ttu-id="7fc86-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7fc86-131">RELATED LINKS</span></span>
