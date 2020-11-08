---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1af202573ff4b783756b8884707922c64ffcf953
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049520"
---
# <span data-ttu-id="155ff-101">Set-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="155ff-101">Set-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="155ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="155ff-102">SYNOPSIS</span></span>
<span data-ttu-id="155ff-103">Umożliwia utworzenie nowej lub zaktualizowanie istniejącej bazy danych programu SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="155ff-103">Creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="155ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="155ff-104">SYNTAX</span></span>

### <span data-ttu-id="155ff-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="155ff-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="155ff-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="155ff-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="155ff-107">Opis</span><span class="sxs-lookup"><span data-stu-id="155ff-107">DESCRIPTION</span></span>
<span data-ttu-id="155ff-108">Polecenie cmdlet **Set-AzCosmosDBSqlDatabase** umożliwia utworzenie nowej lub zaktualizowanie istniejącej bazy danych SQL programu CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="155ff-108">The **Set-AzCosmosDBSqlDatabase** cmdlet creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="155ff-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="155ff-109">EXAMPLES</span></span>

### <span data-ttu-id="155ff-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="155ff-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName}-Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
SqlDatabaseGetResultsId :
_rid                    :
_ts                     :
_etag                   :
_colls                  :
_users                  :
```

## <span data-ttu-id="155ff-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="155ff-111">PARAMETERS</span></span>

### <span data-ttu-id="155ff-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="155ff-112">-AccountName</span></span>
<span data-ttu-id="155ff-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="155ff-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="155ff-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="155ff-114">-Confirm</span></span>
<span data-ttu-id="155ff-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="155ff-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="155ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="155ff-116">-DefaultProfile</span></span>
<span data-ttu-id="155ff-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="155ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="155ff-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="155ff-118">-InputObject</span></span>
<span data-ttu-id="155ff-119">Obiekt konta CosmosDB</span><span class="sxs-lookup"><span data-stu-id="155ff-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="155ff-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="155ff-120">-Name</span></span>
<span data-ttu-id="155ff-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="155ff-121">Database name.</span></span>

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

### <span data-ttu-id="155ff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="155ff-122">-ResourceGroupName</span></span>
<span data-ttu-id="155ff-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="155ff-123">Name of resource group.</span></span>

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

### <span data-ttu-id="155ff-124">-Produktywność</span><span class="sxs-lookup"><span data-stu-id="155ff-124">-Throughput</span></span>
<span data-ttu-id="155ff-125">Przepływność bazy danych SQL (RU/s).</span><span class="sxs-lookup"><span data-stu-id="155ff-125">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="155ff-126">Wartość domyślna to 400.</span><span class="sxs-lookup"><span data-stu-id="155ff-126">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="155ff-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="155ff-127">-WhatIf</span></span>
<span data-ttu-id="155ff-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="155ff-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="155ff-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="155ff-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="155ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="155ff-130">CommonParameters</span></span>
<span data-ttu-id="155ff-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="155ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="155ff-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="155ff-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="155ff-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="155ff-133">INPUTS</span></span>

### <span data-ttu-id="155ff-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="155ff-134">None</span></span>

## <span data-ttu-id="155ff-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="155ff-135">OUTPUTS</span></span>

### <span data-ttu-id="155ff-136">Microsoft. Azure. Commands. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="155ff-136">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="155ff-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="155ff-137">NOTES</span></span>

## <span data-ttu-id="155ff-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="155ff-138">RELATED LINKS</span></span>
