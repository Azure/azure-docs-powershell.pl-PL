---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238460"
---
# <span data-ttu-id="b5b6a-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="b5b6a-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="b5b6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b6a-103">Usuwa aprocedure sql storedprocedure z bazy danych ADB.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="b5b6a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b5b6a-104">SYNTAX</span></span>

### <span data-ttu-id="b5b6a-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5b6a-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5b6a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5b6a-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5b6a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b5b6a-107">DESCRIPTION</span></span>
<span data-ttu-id="b5b6a-108">Polecenie cmdlet **Remove-AzCosmosDBSqlStoredProcedure** usuwa składnię OSDB Sql StoredProcedure odpowiadającą podanej nazwie ResourceGroupName, AccountName i DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="b5b6a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b5b6a-109">EXAMPLES</span></span>

### <span data-ttu-id="b5b6a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b5b6a-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="b5b6a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5b6a-111">PARAMETERS</span></span>

### <span data-ttu-id="b5b6a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b5b6a-112">-AccountName</span></span>
<span data-ttu-id="b5b6a-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b5b6a-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5b6a-114">-Confirm</span></span>
<span data-ttu-id="b5b6a-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5b6a-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b5b6a-116">-ContainerName</span></span>
<span data-ttu-id="b5b6a-117">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-117">Container name.</span></span>

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

### <span data-ttu-id="b5b6a-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b5b6a-118">-DatabaseName</span></span>
<span data-ttu-id="b5b6a-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-119">Database name.</span></span>

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

### <span data-ttu-id="b5b6a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b6a-120">-DefaultProfile</span></span>
<span data-ttu-id="b5b6a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5b6a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5b6a-122">-InputObject</span></span>
<span data-ttu-id="b5b6a-123">Obiekt Sql Database.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-123">Sql Database object.</span></span>

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

### <span data-ttu-id="b5b6a-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b5b6a-124">-Name</span></span>
<span data-ttu-id="b5b6a-125">Przechowywana nazwa Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="b5b6a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5b6a-126">-PassThru</span></span>
<span data-ttu-id="b5b6a-127">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="b5b6a-128">Wynik jest prawdziwy, jeśli operacja powiodła się, a w przypadku jej wystąpienia zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b6a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b6a-129">-ResourceGroupName</span></span>
<span data-ttu-id="b5b6a-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-130">Name of resource group.</span></span>

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

### <span data-ttu-id="b5b6a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5b6a-131">-WhatIf</span></span>
<span data-ttu-id="b5b6a-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5b6a-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5b6a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b6a-134">CommonParameters</span></span>
<span data-ttu-id="b5b6a-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b6a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b6a-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5b6a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b6a-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5b6a-137">INPUTS</span></span>

### <span data-ttu-id="b5b6a-138">Brak</span><span class="sxs-lookup"><span data-stu-id="b5b6a-138">None</span></span>

## <span data-ttu-id="b5b6a-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5b6a-139">OUTPUTS</span></span>

### <span data-ttu-id="b5b6a-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="b5b6a-140">System.Void</span></span>

### <span data-ttu-id="b5b6a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5b6a-141">System.Boolean</span></span>

## <span data-ttu-id="b5b6a-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b5b6a-142">NOTES</span></span>

## <span data-ttu-id="b5b6a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5b6a-143">RELATED LINKS</span></span>
