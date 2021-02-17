---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177235"
---
# <span data-ttu-id="8c081-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="8c081-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="8c081-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c081-102">SYNOPSIS</span></span>
<span data-ttu-id="8c081-103">Usuwa kolekcję ZakonuDb MongoDB.</span><span class="sxs-lookup"><span data-stu-id="8c081-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="8c081-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c081-104">SYNTAX</span></span>

### <span data-ttu-id="8c081-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8c081-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c081-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c081-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c081-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c081-107">DESCRIPTION</span></span>
<span data-ttu-id="8c081-108">Polecenie **cmdlet Remove-AzCosmosDBMongoDBCollection** usuwa kolekcjęDomdówDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="8c081-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="8c081-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c081-109">EXAMPLES</span></span>

### <span data-ttu-id="8c081-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8c081-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="8c081-111">Polecenie cmdlet zwraca obiekt typu bool(po przekazaniu wartości -PassThru), co jest prawdziwe, jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="8c081-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="8c081-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c081-112">PARAMETERS</span></span>

### <span data-ttu-id="8c081-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8c081-113">-AccountName</span></span>
<span data-ttu-id="8c081-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="8c081-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8c081-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c081-115">-Confirm</span></span>
<span data-ttu-id="8c081-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8c081-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c081-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8c081-117">-DatabaseName</span></span>
<span data-ttu-id="8c081-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8c081-118">Database name.</span></span>

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

### <span data-ttu-id="8c081-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c081-119">-DefaultProfile</span></span>
<span data-ttu-id="8c081-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c081-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c081-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c081-121">-InputObject</span></span>
<span data-ttu-id="8c081-122">Obiekt Sql Container.</span><span class="sxs-lookup"><span data-stu-id="8c081-122">Sql Container object.</span></span>

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

### <span data-ttu-id="8c081-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8c081-123">-Name</span></span>
<span data-ttu-id="8c081-124">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="8c081-124">Collection name.</span></span>

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

### <span data-ttu-id="8c081-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c081-125">-PassThru</span></span>
<span data-ttu-id="8c081-126">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="8c081-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="8c081-127">Wynik jest prawdziwy, jeśli operacja powiodła się, a w przypadku jej wystąpienia zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="8c081-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="8c081-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c081-128">-ResourceGroupName</span></span>
<span data-ttu-id="8c081-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c081-129">Name of resource group.</span></span>

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

### <span data-ttu-id="8c081-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c081-130">-WhatIf</span></span>
<span data-ttu-id="8c081-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c081-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c081-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8c081-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c081-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c081-133">CommonParameters</span></span>
<span data-ttu-id="8c081-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c081-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c081-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c081-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c081-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c081-136">INPUTS</span></span>

### <span data-ttu-id="8c081-137">Microsoft.Azure.Commands.DoceńDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="8c081-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="8c081-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c081-138">OUTPUTS</span></span>

### <span data-ttu-id="8c081-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="8c081-139">System.Void</span></span>

### <span data-ttu-id="8c081-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8c081-140">System.Boolean</span></span>

## <span data-ttu-id="8c081-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c081-141">NOTES</span></span>

## <span data-ttu-id="8c081-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c081-142">RELATED LINKS</span></span>
