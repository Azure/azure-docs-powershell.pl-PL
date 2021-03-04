---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 8a717b15268090a7e5ea356c49b11d9aba1ab009
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977153"
---
# <span data-ttu-id="65796-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="65796-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="65796-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65796-102">SYNOPSIS</span></span>
<span data-ttu-id="65796-103">Aktualizuje składnię Sql StoredProcedure dla firmy MicrosoftDB.</span><span class="sxs-lookup"><span data-stu-id="65796-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="65796-104">Wykonuje operację poprawki po stronie klienta, odczytując istniejącą usługę StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="65796-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="65796-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="65796-105">SYNTAX</span></span>

### <span data-ttu-id="65796-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="65796-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65796-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65796-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65796-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65796-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65796-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="65796-109">DESCRIPTION</span></span>
<span data-ttu-id="65796-110">Aktualizuje składnię Sql StoredProcedure dla firmy MicrosoftDB.</span><span class="sxs-lookup"><span data-stu-id="65796-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="65796-111">Wykonuje operację poprawki po stronie klienta, odczytując istniejącą usługę StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="65796-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="65796-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="65796-112">EXAMPLES</span></span>

### <span data-ttu-id="65796-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="65796-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="65796-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65796-114">PARAMETERS</span></span>

### <span data-ttu-id="65796-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="65796-115">-AccountName</span></span>
<span data-ttu-id="65796-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="65796-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="65796-117">— Treść</span><span class="sxs-lookup"><span data-stu-id="65796-117">-Body</span></span>
<span data-ttu-id="65796-118">Treść procedury składowanej.</span><span class="sxs-lookup"><span data-stu-id="65796-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="65796-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65796-119">-Confirm</span></span>
<span data-ttu-id="65796-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="65796-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65796-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="65796-121">-ContainerName</span></span>
<span data-ttu-id="65796-122">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="65796-122">Container name.</span></span>

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

### <span data-ttu-id="65796-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="65796-123">-DatabaseName</span></span>
<span data-ttu-id="65796-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="65796-124">Database name.</span></span>

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

### <span data-ttu-id="65796-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65796-125">-DefaultProfile</span></span>
<span data-ttu-id="65796-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="65796-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65796-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65796-127">-InputObject</span></span>
<span data-ttu-id="65796-128">Obiekt Sql Stored Procedure</span><span class="sxs-lookup"><span data-stu-id="65796-128">Sql Stored Procedure Object</span></span>

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

### <span data-ttu-id="65796-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="65796-129">-Name</span></span>
<span data-ttu-id="65796-130">Przechowywana nazwa Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="65796-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="65796-131">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="65796-131">-ParentObject</span></span>
<span data-ttu-id="65796-132">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="65796-132">Sql Container object.</span></span>

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

### <span data-ttu-id="65796-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65796-133">-ResourceGroupName</span></span>
<span data-ttu-id="65796-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="65796-134">Name of resource group.</span></span>

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

### <span data-ttu-id="65796-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65796-135">-WhatIf</span></span>
<span data-ttu-id="65796-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65796-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65796-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="65796-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65796-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65796-138">CommonParameters</span></span>
<span data-ttu-id="65796-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65796-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65796-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65796-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65796-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65796-141">INPUTS</span></span>

### <span data-ttu-id="65796-142">Microsoft.Azure.Commands.DokowaniaDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="65796-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="65796-143">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="65796-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="65796-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65796-144">OUTPUTS</span></span>

### <span data-ttu-id="65796-145">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="65796-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="65796-146">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="65796-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="65796-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="65796-147">NOTES</span></span>

## <span data-ttu-id="65796-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65796-148">RELATED LINKS</span></span>
