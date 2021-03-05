---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: d1f4e4c5c48e33a1b3c2ac882b0c561bb50f9bed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009697"
---
# <span data-ttu-id="1a983-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="1a983-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="1a983-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a983-102">SYNOPSIS</span></span>
<span data-ttu-id="1a983-103">Aktualizacja funkcji UserDefinedFunction języka Sql Dla języka Sql.</span><span class="sxs-lookup"><span data-stu-id="1a983-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="1a983-104">Wykonuje operację poprawki po stronie klienta, czytając istniejącą funkcję UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="1a983-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="1a983-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1a983-105">SYNTAX</span></span>

### <span data-ttu-id="1a983-106">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1a983-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a983-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a983-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a983-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a983-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a983-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="1a983-109">DESCRIPTION</span></span>
<span data-ttu-id="1a983-110">Aktualizacja funkcji UserDefinedFunction języka Sql Dla języka Sql.</span><span class="sxs-lookup"><span data-stu-id="1a983-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="1a983-111">Wykonuje operację poprawki po stronie klienta, czytając istniejącą funkcję UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="1a983-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="1a983-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1a983-112">EXAMPLES</span></span>

### <span data-ttu-id="1a983-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1a983-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="1a983-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a983-114">PARAMETERS</span></span>

### <span data-ttu-id="1a983-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1a983-115">-AccountName</span></span>
<span data-ttu-id="1a983-116">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="1a983-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1a983-117">— Treść</span><span class="sxs-lookup"><span data-stu-id="1a983-117">-Body</span></span>
<span data-ttu-id="1a983-118">Treść funkcji zdefiniowanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1a983-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="1a983-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a983-119">-Confirm</span></span>
<span data-ttu-id="1a983-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1a983-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a983-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1a983-121">-ContainerName</span></span>
<span data-ttu-id="1a983-122">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="1a983-122">Container name.</span></span>

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

### <span data-ttu-id="1a983-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1a983-123">-DatabaseName</span></span>
<span data-ttu-id="1a983-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1a983-124">Database name.</span></span>

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

### <span data-ttu-id="1a983-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a983-125">-DefaultProfile</span></span>
<span data-ttu-id="1a983-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a983-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a983-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a983-127">-InputObject</span></span>
<span data-ttu-id="1a983-128">Obiekt funkcji zdefiniowany przez użytkownika sql</span><span class="sxs-lookup"><span data-stu-id="1a983-128">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="1a983-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1a983-129">-Name</span></span>
<span data-ttu-id="1a983-130">Nazwa funkcji zdefiniowanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1a983-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="1a983-131">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="1a983-131">-ParentObject</span></span>
<span data-ttu-id="1a983-132">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="1a983-132">Sql Container object.</span></span>

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

### <span data-ttu-id="1a983-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a983-133">-ResourceGroupName</span></span>
<span data-ttu-id="1a983-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1a983-134">Name of resource group.</span></span>

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

### <span data-ttu-id="1a983-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a983-135">-WhatIf</span></span>
<span data-ttu-id="1a983-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a983-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a983-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1a983-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a983-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a983-138">CommonParameters</span></span>
<span data-ttu-id="1a983-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a983-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a983-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a983-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a983-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a983-141">INPUTS</span></span>

### <span data-ttu-id="1a983-142">Microsoft.Azure.Commands.DokowaniaDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="1a983-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="1a983-143">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="1a983-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="1a983-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a983-144">OUTPUTS</span></span>

### <span data-ttu-id="1a983-145">Microsoft.Azure.Commands.DoceńDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="1a983-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="1a983-146">Microsoft.Azure.Commands.Dosdb.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="1a983-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="1a983-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1a983-147">NOTES</span></span>

## <span data-ttu-id="1a983-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a983-148">RELATED LINKS</span></span>
