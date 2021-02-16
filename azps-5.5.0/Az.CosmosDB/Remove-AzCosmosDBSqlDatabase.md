---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238470"
---
# <span data-ttu-id="4f738-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4f738-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="4f738-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f738-102">SYNOPSIS</span></span>
<span data-ttu-id="4f738-103">Usuwa bazę danych Sql Dla firmy Adb.</span><span class="sxs-lookup"><span data-stu-id="4f738-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="4f738-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4f738-104">SYNTAX</span></span>

### <span data-ttu-id="4f738-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f738-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f738-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f738-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f738-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4f738-107">DESCRIPTION</span></span>
<span data-ttu-id="4f738-108">Polecenie cmdlet **Remove-AzCosmosDBSqlDatabase** usuwa bazę danych SqlsDb, która odpowiada podanej nazwie ResourceGroupName, AccountName i DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="4f738-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="4f738-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4f738-109">EXAMPLES</span></span>

### <span data-ttu-id="4f738-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4f738-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="4f738-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f738-111">PARAMETERS</span></span>

### <span data-ttu-id="4f738-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4f738-112">-AccountName</span></span>
<span data-ttu-id="4f738-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="4f738-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4f738-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4f738-114">-Confirm</span></span>
<span data-ttu-id="4f738-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4f738-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f738-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f738-116">-DefaultProfile</span></span>
<span data-ttu-id="4f738-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f738-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f738-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f738-118">-InputObject</span></span>
<span data-ttu-id="4f738-119">Obiekt Sql Database.</span><span class="sxs-lookup"><span data-stu-id="4f738-119">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f738-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4f738-120">-Name</span></span>
<span data-ttu-id="4f738-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4f738-121">Database name.</span></span>

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

### <span data-ttu-id="4f738-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f738-122">-PassThru</span></span>
<span data-ttu-id="4f738-123">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="4f738-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="4f738-124">Dane wyjściowe są prawdziwe, jeśli operacja została pomyślnie i jeśli nie, zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="4f738-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="4f738-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f738-125">-ResourceGroupName</span></span>
<span data-ttu-id="4f738-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4f738-126">Name of resource group.</span></span>

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

### <span data-ttu-id="4f738-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f738-127">-WhatIf</span></span>
<span data-ttu-id="4f738-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f738-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f738-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4f738-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f738-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f738-130">CommonParameters</span></span>
<span data-ttu-id="4f738-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f738-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f738-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f738-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f738-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f738-133">INPUTS</span></span>

### <span data-ttu-id="4f738-134">Brak</span><span class="sxs-lookup"><span data-stu-id="4f738-134">None</span></span>

## <span data-ttu-id="4f738-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4f738-135">OUTPUTS</span></span>

### <span data-ttu-id="4f738-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="4f738-136">System.Void</span></span>

### <span data-ttu-id="4f738-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f738-137">System.Boolean</span></span>

## <span data-ttu-id="4f738-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4f738-138">NOTES</span></span>

## <span data-ttu-id="4f738-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f738-139">RELATED LINKS</span></span>
