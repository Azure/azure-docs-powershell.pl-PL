---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: ab64359e8db417c3c87a49a773fe56c3dcc5334b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957434"
---
# <span data-ttu-id="4236e-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="4236e-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="4236e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4236e-102">SYNOPSIS</span></span>
<span data-ttu-id="4236e-103">Usuwa kontener sql Dla firmy Adb.</span><span class="sxs-lookup"><span data-stu-id="4236e-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="4236e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4236e-104">SYNTAX</span></span>

### <span data-ttu-id="4236e-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="4236e-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4236e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4236e-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4236e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4236e-107">DESCRIPTION</span></span>
<span data-ttu-id="4236e-108">Polecenie cmdlet **Remove-AzCosmosDBSqlContainer** usuwa kontener sql Dosdb odpowiadający podanej nazwie ResourceGroupName, AccountName, DatabaseName i ContainerName.</span><span class="sxs-lookup"><span data-stu-id="4236e-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="4236e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4236e-109">EXAMPLES</span></span>

### <span data-ttu-id="4236e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4236e-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="4236e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4236e-111">PARAMETERS</span></span>

### <span data-ttu-id="4236e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4236e-112">-AccountName</span></span>
<span data-ttu-id="4236e-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="4236e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4236e-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4236e-114">-Confirm</span></span>
<span data-ttu-id="4236e-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4236e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4236e-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4236e-116">-DatabaseName</span></span>
<span data-ttu-id="4236e-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4236e-117">Database name.</span></span>

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

### <span data-ttu-id="4236e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4236e-118">-DefaultProfile</span></span>
<span data-ttu-id="4236e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4236e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4236e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4236e-120">-InputObject</span></span>
<span data-ttu-id="4236e-121">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="4236e-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4236e-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4236e-122">-Name</span></span>
<span data-ttu-id="4236e-123">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="4236e-123">Container name.</span></span>

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

### <span data-ttu-id="4236e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4236e-124">-PassThru</span></span>
<span data-ttu-id="4236e-125">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="4236e-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="4236e-126">Dane wyjściowe są prawdziwe, jeśli operacja została pomyślnie i jeśli nie, zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="4236e-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="4236e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4236e-127">-ResourceGroupName</span></span>
<span data-ttu-id="4236e-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4236e-128">Name of resource group.</span></span>

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

### <span data-ttu-id="4236e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4236e-129">-WhatIf</span></span>
<span data-ttu-id="4236e-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4236e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4236e-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4236e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4236e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4236e-132">CommonParameters</span></span>
<span data-ttu-id="4236e-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4236e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4236e-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4236e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4236e-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4236e-135">INPUTS</span></span>

### <span data-ttu-id="4236e-136">Brak</span><span class="sxs-lookup"><span data-stu-id="4236e-136">None</span></span>

## <span data-ttu-id="4236e-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4236e-137">OUTPUTS</span></span>

### <span data-ttu-id="4236e-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="4236e-138">System.Void</span></span>

### <span data-ttu-id="4236e-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4236e-139">System.Boolean</span></span>

## <span data-ttu-id="4236e-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4236e-140">NOTES</span></span>

## <span data-ttu-id="4236e-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4236e-141">RELATED LINKS</span></span>
