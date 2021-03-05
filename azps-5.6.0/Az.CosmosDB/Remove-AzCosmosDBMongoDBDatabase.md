---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: aa5934de20812a8f8a5ebf76c4b23e01cb59d2b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995688"
---
# <span data-ttu-id="036af-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="036af-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="036af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="036af-102">SYNOPSIS</span></span>
<span data-ttu-id="036af-103">Usuwa bazę danych ADB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="036af-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="036af-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="036af-104">SYNTAX</span></span>

### <span data-ttu-id="036af-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="036af-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="036af-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="036af-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="036af-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="036af-107">DESCRIPTION</span></span>
<span data-ttu-id="036af-108">Polecenie **cmdlet Remove-AzCosmosDBMongoDBDatabase** usuwa bazę danych ADB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="036af-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="036af-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="036af-109">EXAMPLES</span></span>

### <span data-ttu-id="036af-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="036af-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="036af-111">Polecenie cmdlet zwraca obiekt typu bool(po przekazaniu wartości -PassThru), co jest prawdziwe, jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="036af-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="036af-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="036af-112">PARAMETERS</span></span>

### <span data-ttu-id="036af-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="036af-113">-AccountName</span></span>
<span data-ttu-id="036af-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="036af-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="036af-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="036af-115">-Confirm</span></span>
<span data-ttu-id="036af-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="036af-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="036af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="036af-117">-DefaultProfile</span></span>
<span data-ttu-id="036af-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="036af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="036af-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="036af-119">-InputObject</span></span>
<span data-ttu-id="036af-120">Obiekt Bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="036af-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="036af-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="036af-121">-Name</span></span>
<span data-ttu-id="036af-122">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="036af-122">Database name.</span></span>

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

### <span data-ttu-id="036af-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="036af-123">-PassThru</span></span>
<span data-ttu-id="036af-124">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="036af-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="036af-125">Dane wyjściowe są prawdziwe, jeśli operacja została pomyślnie i jeśli nie, zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="036af-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="036af-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="036af-126">-ResourceGroupName</span></span>
<span data-ttu-id="036af-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="036af-127">Name of resource group.</span></span>

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

### <span data-ttu-id="036af-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="036af-128">-WhatIf</span></span>
<span data-ttu-id="036af-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="036af-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="036af-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="036af-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="036af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="036af-131">CommonParameters</span></span>
<span data-ttu-id="036af-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="036af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="036af-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="036af-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="036af-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="036af-134">INPUTS</span></span>

### <span data-ttu-id="036af-135">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="036af-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="036af-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="036af-136">OUTPUTS</span></span>

### <span data-ttu-id="036af-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="036af-137">System.Void</span></span>

### <span data-ttu-id="036af-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="036af-138">System.Boolean</span></span>

## <span data-ttu-id="036af-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="036af-139">NOTES</span></span>

## <span data-ttu-id="036af-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="036af-140">RELATED LINKS</span></span>
