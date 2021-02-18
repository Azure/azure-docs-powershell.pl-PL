---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181218"
---
# <span data-ttu-id="8dff8-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="8dff8-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="8dff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dff8-102">SYNOPSIS</span></span>
<span data-ttu-id="8dff8-103">Aktualizacja funkcji UserDefinedFunction języka Sql Dla systemu WindowsDB.</span><span class="sxs-lookup"><span data-stu-id="8dff8-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="8dff8-104">Wykonuje operację poprawiania po stronie klienta, czytając istniejącą funkcję UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="8dff8-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="8dff8-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8dff8-105">SYNTAX</span></span>

### <span data-ttu-id="8dff8-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8dff8-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dff8-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dff8-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8dff8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dff8-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dff8-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="8dff8-109">DESCRIPTION</span></span>
<span data-ttu-id="8dff8-110">Aktualizacja funkcji UserDefinedFunction języka Sql Dla systemu WindowsDB.</span><span class="sxs-lookup"><span data-stu-id="8dff8-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="8dff8-111">Wykonuje operację poprawiania po stronie klienta, czytając istniejącą funkcję UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="8dff8-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="8dff8-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8dff8-112">EXAMPLES</span></span>

### <span data-ttu-id="8dff8-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8dff8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="8dff8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dff8-114">PARAMETERS</span></span>

### <span data-ttu-id="8dff8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8dff8-115">-AccountName</span></span>
<span data-ttu-id="8dff8-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="8dff8-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8dff8-117">— Treść</span><span class="sxs-lookup"><span data-stu-id="8dff8-117">-Body</span></span>
<span data-ttu-id="8dff8-118">Treść funkcji zdefiniowanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8dff8-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="8dff8-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8dff8-119">-Confirm</span></span>
<span data-ttu-id="8dff8-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8dff8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dff8-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8dff8-121">-ContainerName</span></span>
<span data-ttu-id="8dff8-122">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="8dff8-122">Container name.</span></span>

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

### <span data-ttu-id="8dff8-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8dff8-123">-DatabaseName</span></span>
<span data-ttu-id="8dff8-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8dff8-124">Database name.</span></span>

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

### <span data-ttu-id="8dff8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dff8-125">-DefaultProfile</span></span>
<span data-ttu-id="8dff8-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8dff8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dff8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dff8-127">-InputObject</span></span>
<span data-ttu-id="8dff8-128">Obiekt funkcji zdefiniowany przez użytkownika sql</span><span class="sxs-lookup"><span data-stu-id="8dff8-128">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dff8-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8dff8-129">-Name</span></span>
<span data-ttu-id="8dff8-130">Nazwa funkcji zdefiniowanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8dff8-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="8dff8-131">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="8dff8-131">-ParentObject</span></span>
<span data-ttu-id="8dff8-132">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="8dff8-132">Sql Container object.</span></span>

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

### <span data-ttu-id="8dff8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dff8-133">-ResourceGroupName</span></span>
<span data-ttu-id="8dff8-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8dff8-134">Name of resource group.</span></span>

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

### <span data-ttu-id="8dff8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dff8-135">-WhatIf</span></span>
<span data-ttu-id="8dff8-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dff8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dff8-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8dff8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dff8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dff8-138">CommonParameters</span></span>
<span data-ttu-id="8dff8-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dff8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dff8-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8dff8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dff8-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8dff8-141">INPUTS</span></span>

### <span data-ttu-id="8dff8-142">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="8dff8-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="8dff8-143">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="8dff8-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="8dff8-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8dff8-144">OUTPUTS</span></span>

### <span data-ttu-id="8dff8-145">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="8dff8-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="8dff8-146">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="8dff8-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="8dff8-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8dff8-147">NOTES</span></span>

## <span data-ttu-id="8dff8-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8dff8-148">RELATED LINKS</span></span>
