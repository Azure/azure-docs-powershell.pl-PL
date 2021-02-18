---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181219"
---
# <span data-ttu-id="b53a4-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="b53a4-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="b53a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b53a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b53a4-103">Aktualizuje składnię Sql StoredProcedure dla firmy Dosdb.</span><span class="sxs-lookup"><span data-stu-id="b53a4-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="b53a4-104">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą usługę StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="b53a4-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="b53a4-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b53a4-105">SYNTAX</span></span>

### <span data-ttu-id="b53a4-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b53a4-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b53a4-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b53a4-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b53a4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b53a4-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b53a4-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b53a4-109">DESCRIPTION</span></span>
<span data-ttu-id="b53a4-110">Aktualizuje składnię Sql StoredProcedure dla firmy Dosdb.</span><span class="sxs-lookup"><span data-stu-id="b53a4-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="b53a4-111">Wykonuje operację poprawiania po stronie klienta, odczytując istniejącą usługę StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="b53a4-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="b53a4-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b53a4-112">EXAMPLES</span></span>

### <span data-ttu-id="b53a4-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b53a4-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="b53a4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b53a4-114">PARAMETERS</span></span>

### <span data-ttu-id="b53a4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b53a4-115">-AccountName</span></span>
<span data-ttu-id="b53a4-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="b53a4-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b53a4-117">— Treść</span><span class="sxs-lookup"><span data-stu-id="b53a4-117">-Body</span></span>
<span data-ttu-id="b53a4-118">Treść procedury składowanej.</span><span class="sxs-lookup"><span data-stu-id="b53a4-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="b53a4-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b53a4-119">-Confirm</span></span>
<span data-ttu-id="b53a4-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b53a4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b53a4-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b53a4-121">-ContainerName</span></span>
<span data-ttu-id="b53a4-122">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="b53a4-122">Container name.</span></span>

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

### <span data-ttu-id="b53a4-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b53a4-123">-DatabaseName</span></span>
<span data-ttu-id="b53a4-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b53a4-124">Database name.</span></span>

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

### <span data-ttu-id="b53a4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b53a4-125">-DefaultProfile</span></span>
<span data-ttu-id="b53a4-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b53a4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b53a4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b53a4-127">-InputObject</span></span>
<span data-ttu-id="b53a4-128">Obiekt Sql Stored Procedure</span><span class="sxs-lookup"><span data-stu-id="b53a4-128">Sql Stored Procedure Object</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b53a4-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b53a4-129">-Name</span></span>
<span data-ttu-id="b53a4-130">Przechowywana nazwa Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="b53a4-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="b53a4-131">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="b53a4-131">-ParentObject</span></span>
<span data-ttu-id="b53a4-132">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="b53a4-132">Sql Container object.</span></span>

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

### <span data-ttu-id="b53a4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b53a4-133">-ResourceGroupName</span></span>
<span data-ttu-id="b53a4-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b53a4-134">Name of resource group.</span></span>

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

### <span data-ttu-id="b53a4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b53a4-135">-WhatIf</span></span>
<span data-ttu-id="b53a4-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b53a4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b53a4-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b53a4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b53a4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b53a4-138">CommonParameters</span></span>
<span data-ttu-id="b53a4-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b53a4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b53a4-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b53a4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b53a4-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b53a4-141">INPUTS</span></span>

### <span data-ttu-id="b53a4-142">Microsoft.Azure.Commands.DokowaniaDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="b53a4-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="b53a4-143">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="b53a4-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="b53a4-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b53a4-144">OUTPUTS</span></span>

### <span data-ttu-id="b53a4-145">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="b53a4-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="b53a4-146">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="b53a4-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="b53a4-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b53a4-147">NOTES</span></span>

## <span data-ttu-id="b53a4-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b53a4-148">RELATED LINKS</span></span>
