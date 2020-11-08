---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223579"
---
# <span data-ttu-id="ae425-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="ae425-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="ae425-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae425-102">SYNOPSIS</span></span>
<span data-ttu-id="ae425-103">Usuwa kolekcję MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ae425-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="ae425-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae425-104">SYNTAX</span></span>

### <span data-ttu-id="ae425-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ae425-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae425-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae425-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae425-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ae425-107">DESCRIPTION</span></span>
<span data-ttu-id="ae425-108">Polecenie cmdlet **Remove-AzCosmosDBMongoDBCollection** usuwa kolekcję MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ae425-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="ae425-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae425-109">EXAMPLES</span></span>

### <span data-ttu-id="ae425-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae425-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="ae425-111">Polecenie cmdlet zwraca obiekt typu wartość logiczna (gdy przekazano parametr-PassThru) o wartości prawda, Jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="ae425-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="ae425-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae425-112">PARAMETERS</span></span>

### <span data-ttu-id="ae425-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ae425-113">-AccountName</span></span>
<span data-ttu-id="ae425-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="ae425-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ae425-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae425-115">-Confirm</span></span>
<span data-ttu-id="ae425-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae425-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae425-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae425-117">-DatabaseName</span></span>
<span data-ttu-id="ae425-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ae425-118">Database name.</span></span>

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

### <span data-ttu-id="ae425-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae425-119">-DefaultProfile</span></span>
<span data-ttu-id="ae425-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae425-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae425-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ae425-121">-InputObject</span></span>
<span data-ttu-id="ae425-122">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="ae425-122">Sql Container object.</span></span>

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

### <span data-ttu-id="ae425-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ae425-123">-Name</span></span>
<span data-ttu-id="ae425-124">Nazwa kolekcji.</span><span class="sxs-lookup"><span data-stu-id="ae425-124">Collection name.</span></span>

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

### <span data-ttu-id="ae425-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae425-125">-PassThru</span></span>
<span data-ttu-id="ae425-126">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="ae425-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="ae425-127">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="ae425-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="ae425-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae425-128">-ResourceGroupName</span></span>
<span data-ttu-id="ae425-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae425-129">Name of resource group.</span></span>

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

### <span data-ttu-id="ae425-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae425-130">-WhatIf</span></span>
<span data-ttu-id="ae425-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae425-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae425-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae425-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae425-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae425-133">CommonParameters</span></span>
<span data-ttu-id="ae425-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae425-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae425-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae425-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae425-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae425-136">INPUTS</span></span>

### <span data-ttu-id="ae425-137">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="ae425-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="ae425-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae425-138">OUTPUTS</span></span>

### <span data-ttu-id="ae425-139">System. void</span><span class="sxs-lookup"><span data-stu-id="ae425-139">System.Void</span></span>

### <span data-ttu-id="ae425-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae425-140">System.Boolean</span></span>

## <span data-ttu-id="ae425-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae425-141">NOTES</span></span>

## <span data-ttu-id="ae425-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae425-142">RELATED LINKS</span></span>
