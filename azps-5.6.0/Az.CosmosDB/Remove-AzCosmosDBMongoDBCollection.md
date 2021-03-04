---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1b4d205460992843e6801ecee13605effb351b77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958842"
---
# <span data-ttu-id="d379b-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="d379b-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="d379b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d379b-102">SYNOPSIS</span></span>
<span data-ttu-id="d379b-103">Usuwa kolekcję ZakonuDb MongoDB.</span><span class="sxs-lookup"><span data-stu-id="d379b-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="d379b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d379b-104">SYNTAX</span></span>

### <span data-ttu-id="d379b-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d379b-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d379b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d379b-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d379b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d379b-107">DESCRIPTION</span></span>
<span data-ttu-id="d379b-108">Polecenie **cmdlet Remove-AzCosmosDBMongoDBCollection** usuwa kolekcję Bazy danych MongoDB.</span><span class="sxs-lookup"><span data-stu-id="d379b-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="d379b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d379b-109">EXAMPLES</span></span>

### <span data-ttu-id="d379b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d379b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="d379b-111">Polecenie cmdlet zwraca obiekt typu bool(po przekazaniu wartości -PassThru), co jest prawdziwe, jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="d379b-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="d379b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d379b-112">PARAMETERS</span></span>

### <span data-ttu-id="d379b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d379b-113">-AccountName</span></span>
<span data-ttu-id="d379b-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="d379b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d379b-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d379b-115">-Confirm</span></span>
<span data-ttu-id="d379b-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d379b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d379b-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d379b-117">-DatabaseName</span></span>
<span data-ttu-id="d379b-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d379b-118">Database name.</span></span>

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

### <span data-ttu-id="d379b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d379b-119">-DefaultProfile</span></span>
<span data-ttu-id="d379b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d379b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d379b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d379b-121">-InputObject</span></span>
<span data-ttu-id="d379b-122">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="d379b-122">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d379b-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d379b-123">-Name</span></span>
<span data-ttu-id="d379b-124">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="d379b-124">Collection name.</span></span>

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

### <span data-ttu-id="d379b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d379b-125">-PassThru</span></span>
<span data-ttu-id="d379b-126">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="d379b-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="d379b-127">Dane wyjściowe są prawdziwe, jeśli operacja została pomyślnie i jeśli nie, zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="d379b-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="d379b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d379b-128">-ResourceGroupName</span></span>
<span data-ttu-id="d379b-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d379b-129">Name of resource group.</span></span>

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

### <span data-ttu-id="d379b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d379b-130">-WhatIf</span></span>
<span data-ttu-id="d379b-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d379b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d379b-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d379b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d379b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d379b-133">CommonParameters</span></span>
<span data-ttu-id="d379b-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d379b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d379b-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d379b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d379b-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d379b-136">INPUTS</span></span>

### <span data-ttu-id="d379b-137">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="d379b-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="d379b-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d379b-138">OUTPUTS</span></span>

### <span data-ttu-id="d379b-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="d379b-139">System.Void</span></span>

### <span data-ttu-id="d379b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d379b-140">System.Boolean</span></span>

## <span data-ttu-id="d379b-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d379b-141">NOTES</span></span>

## <span data-ttu-id="d379b-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d379b-142">RELATED LINKS</span></span>
