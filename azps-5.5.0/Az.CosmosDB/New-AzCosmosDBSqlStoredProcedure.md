---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196771"
---
# <span data-ttu-id="a3523-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="a3523-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="a3523-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3523-102">SYNOPSIS</span></span>
<span data-ttu-id="a3523-103">Tworzy nową bazę danych adb sql storedprocedure.</span><span class="sxs-lookup"><span data-stu-id="a3523-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="a3523-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a3523-104">SYNTAX</span></span>

### <span data-ttu-id="a3523-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a3523-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3523-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3523-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3523-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a3523-107">DESCRIPTION</span></span>
<span data-ttu-id="a3523-108">Tworzy nową bazę danych ADB Sql StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="a3523-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="a3523-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a3523-109">EXAMPLES</span></span>

### <span data-ttu-id="a3523-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a3523-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="a3523-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3523-111">PARAMETERS</span></span>

### <span data-ttu-id="a3523-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a3523-112">-AccountName</span></span>
<span data-ttu-id="a3523-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="a3523-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a3523-114">— Treść</span><span class="sxs-lookup"><span data-stu-id="a3523-114">-Body</span></span>
<span data-ttu-id="a3523-115">Treść procedury składowanej.</span><span class="sxs-lookup"><span data-stu-id="a3523-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="a3523-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3523-116">-Confirm</span></span>
<span data-ttu-id="a3523-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a3523-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3523-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a3523-118">-ContainerName</span></span>
<span data-ttu-id="a3523-119">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="a3523-119">Container name.</span></span>

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

### <span data-ttu-id="a3523-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a3523-120">-DatabaseName</span></span>
<span data-ttu-id="a3523-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a3523-121">Database name.</span></span>

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

### <span data-ttu-id="a3523-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3523-122">-DefaultProfile</span></span>
<span data-ttu-id="a3523-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3523-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3523-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a3523-124">-Name</span></span>
<span data-ttu-id="a3523-125">Przechowywana nazwa Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="a3523-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="a3523-126">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="a3523-126">-ParentObject</span></span>
<span data-ttu-id="a3523-127">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="a3523-127">Sql Container object.</span></span>

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

### <span data-ttu-id="a3523-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3523-128">-ResourceGroupName</span></span>
<span data-ttu-id="a3523-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a3523-129">Name of resource group.</span></span>

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

### <span data-ttu-id="a3523-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3523-130">-WhatIf</span></span>
<span data-ttu-id="a3523-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3523-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3523-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a3523-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3523-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3523-133">CommonParameters</span></span>
<span data-ttu-id="a3523-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3523-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3523-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3523-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3523-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3523-136">INPUTS</span></span>

### <span data-ttu-id="a3523-137">Microsoft.Azure.Commands.DokowaniaDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="a3523-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="a3523-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3523-138">OUTPUTS</span></span>

### <span data-ttu-id="a3523-139">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="a3523-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="a3523-140">Microsoft.Azure.Commands.Dosdb.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="a3523-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="a3523-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a3523-141">NOTES</span></span>

## <span data-ttu-id="a3523-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3523-142">RELATED LINKS</span></span>
