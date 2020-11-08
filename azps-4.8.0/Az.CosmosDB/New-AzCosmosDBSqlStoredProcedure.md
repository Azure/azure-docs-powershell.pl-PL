---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062838"
---
# <span data-ttu-id="72660-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="72660-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="72660-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72660-102">SYNOPSIS</span></span>
<span data-ttu-id="72660-103">Tworzy nowy CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="72660-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="72660-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72660-104">SYNTAX</span></span>

### <span data-ttu-id="72660-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="72660-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72660-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72660-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72660-107">Opis</span><span class="sxs-lookup"><span data-stu-id="72660-107">DESCRIPTION</span></span>
<span data-ttu-id="72660-108">Tworzy nowy CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="72660-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="72660-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72660-109">EXAMPLES</span></span>

### <span data-ttu-id="72660-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="72660-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="72660-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72660-111">PARAMETERS</span></span>

### <span data-ttu-id="72660-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="72660-112">-AccountName</span></span>
<span data-ttu-id="72660-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="72660-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="72660-114">-Body</span><span class="sxs-lookup"><span data-stu-id="72660-114">-Body</span></span>
<span data-ttu-id="72660-115">Treść procedury składowanej.</span><span class="sxs-lookup"><span data-stu-id="72660-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="72660-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72660-116">-Confirm</span></span>
<span data-ttu-id="72660-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72660-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72660-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="72660-118">-ContainerName</span></span>
<span data-ttu-id="72660-119">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="72660-119">Container name.</span></span>

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

### <span data-ttu-id="72660-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="72660-120">-DatabaseName</span></span>
<span data-ttu-id="72660-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="72660-121">Database name.</span></span>

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

### <span data-ttu-id="72660-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72660-122">-DefaultProfile</span></span>
<span data-ttu-id="72660-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72660-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72660-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72660-124">-Name</span></span>
<span data-ttu-id="72660-125">Nazwa zapisanego Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="72660-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="72660-126">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="72660-126">-ParentObject</span></span>
<span data-ttu-id="72660-127">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="72660-127">Sql Container object.</span></span>

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

### <span data-ttu-id="72660-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72660-128">-ResourceGroupName</span></span>
<span data-ttu-id="72660-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="72660-129">Name of resource group.</span></span>

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

### <span data-ttu-id="72660-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72660-130">-WhatIf</span></span>
<span data-ttu-id="72660-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72660-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72660-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72660-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72660-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72660-133">CommonParameters</span></span>
<span data-ttu-id="72660-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72660-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72660-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72660-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72660-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72660-136">INPUTS</span></span>

### <span data-ttu-id="72660-137">Microsoft. Azure. Commands. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="72660-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="72660-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72660-138">OUTPUTS</span></span>

### <span data-ttu-id="72660-139">Microsoft. Azure. Commands. CosmosDB. models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="72660-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="72660-140">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="72660-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="72660-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72660-141">NOTES</span></span>

## <span data-ttu-id="72660-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72660-142">RELATED LINKS</span></span>
