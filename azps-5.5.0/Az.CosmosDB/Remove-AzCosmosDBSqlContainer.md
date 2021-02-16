---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238499"
---
# <span data-ttu-id="9c56b-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="9c56b-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="9c56b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c56b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c56b-103">Usuwa kontener sql Dla firmy Adb.</span><span class="sxs-lookup"><span data-stu-id="9c56b-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="9c56b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9c56b-104">SYNTAX</span></span>

### <span data-ttu-id="9c56b-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9c56b-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c56b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c56b-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c56b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9c56b-107">DESCRIPTION</span></span>
<span data-ttu-id="9c56b-108">Polecenie cmdlet **Remove-AzCosmosDBSqlContainer** usuwa kontener sql Dosdb odpowiadający podanej nazwie ResourceGroupName, AccountName, DatabaseName i ContainerName.</span><span class="sxs-lookup"><span data-stu-id="9c56b-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="9c56b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9c56b-109">EXAMPLES</span></span>

### <span data-ttu-id="9c56b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c56b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="9c56b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c56b-111">PARAMETERS</span></span>

### <span data-ttu-id="9c56b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9c56b-112">-AccountName</span></span>
<span data-ttu-id="9c56b-113">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="9c56b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9c56b-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c56b-114">-Confirm</span></span>
<span data-ttu-id="9c56b-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9c56b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c56b-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9c56b-116">-DatabaseName</span></span>
<span data-ttu-id="9c56b-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="9c56b-117">Database name.</span></span>

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

### <span data-ttu-id="9c56b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c56b-118">-DefaultProfile</span></span>
<span data-ttu-id="9c56b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c56b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c56b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c56b-120">-InputObject</span></span>
<span data-ttu-id="9c56b-121">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="9c56b-121">Sql Container object.</span></span>

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

### <span data-ttu-id="9c56b-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9c56b-122">-Name</span></span>
<span data-ttu-id="9c56b-123">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="9c56b-123">Container name.</span></span>

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

### <span data-ttu-id="9c56b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c56b-124">-PassThru</span></span>
<span data-ttu-id="9c56b-125">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="9c56b-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="9c56b-126">Wynik jest prawdziwy, jeśli operacja powiodła się, a w przypadku jej wystąpienia zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="9c56b-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="9c56b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c56b-127">-ResourceGroupName</span></span>
<span data-ttu-id="9c56b-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9c56b-128">Name of resource group.</span></span>

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

### <span data-ttu-id="9c56b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c56b-129">-WhatIf</span></span>
<span data-ttu-id="9c56b-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c56b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c56b-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9c56b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c56b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c56b-132">CommonParameters</span></span>
<span data-ttu-id="9c56b-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c56b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c56b-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c56b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c56b-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c56b-135">INPUTS</span></span>

### <span data-ttu-id="9c56b-136">Brak</span><span class="sxs-lookup"><span data-stu-id="9c56b-136">None</span></span>

## <span data-ttu-id="9c56b-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c56b-137">OUTPUTS</span></span>

### <span data-ttu-id="9c56b-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="9c56b-138">System.Void</span></span>

### <span data-ttu-id="9c56b-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9c56b-139">System.Boolean</span></span>

## <span data-ttu-id="9c56b-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9c56b-140">NOTES</span></span>

## <span data-ttu-id="9c56b-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c56b-141">RELATED LINKS</span></span>
