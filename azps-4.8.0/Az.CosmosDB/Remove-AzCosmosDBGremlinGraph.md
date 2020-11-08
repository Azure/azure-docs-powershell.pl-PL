---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 560fcaa33e635eefd4ba94c5c7cbd05cba1cc304
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221824"
---
# <span data-ttu-id="64f8c-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="64f8c-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="64f8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64f8c-102">SYNOPSIS</span></span>
<span data-ttu-id="64f8c-103">Usuwa wykres CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="64f8c-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="64f8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64f8c-104">SYNTAX</span></span>

### <span data-ttu-id="64f8c-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="64f8c-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64f8c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64f8c-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64f8c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="64f8c-107">DESCRIPTION</span></span>
<span data-ttu-id="64f8c-108">Polecenie cmdlet **Remove-AzCosmosDBGremlinGraph** usuwa CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="64f8c-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="64f8c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64f8c-109">EXAMPLES</span></span>

### <span data-ttu-id="64f8c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="64f8c-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="64f8c-111">Polecenie cmdlet zwraca obiekt typu wartość logiczna (gdy przekazano parametr-PassThru) o wartości prawda, Jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="64f8c-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="64f8c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64f8c-112">PARAMETERS</span></span>

### <span data-ttu-id="64f8c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="64f8c-113">-AccountName</span></span>
<span data-ttu-id="64f8c-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="64f8c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="64f8c-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64f8c-115">-Confirm</span></span>
<span data-ttu-id="64f8c-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64f8c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64f8c-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="64f8c-117">-DatabaseName</span></span>
<span data-ttu-id="64f8c-118">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="64f8c-118">Database name.</span></span>

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

### <span data-ttu-id="64f8c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f8c-119">-DefaultProfile</span></span>
<span data-ttu-id="64f8c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64f8c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64f8c-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="64f8c-121">-InputObject</span></span>
<span data-ttu-id="64f8c-122">Obiekt wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="64f8c-122">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64f8c-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64f8c-123">-Name</span></span>
<span data-ttu-id="64f8c-124">Nazwa wykresu Gremlin.</span><span class="sxs-lookup"><span data-stu-id="64f8c-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="64f8c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64f8c-125">-PassThru</span></span>
<span data-ttu-id="64f8c-126">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="64f8c-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="64f8c-127">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="64f8c-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="64f8c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64f8c-128">-ResourceGroupName</span></span>
<span data-ttu-id="64f8c-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="64f8c-129">Name of resource group.</span></span>

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

### <span data-ttu-id="64f8c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64f8c-130">-WhatIf</span></span>
<span data-ttu-id="64f8c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64f8c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64f8c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64f8c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64f8c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f8c-133">CommonParameters</span></span>
<span data-ttu-id="64f8c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64f8c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f8c-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64f8c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f8c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64f8c-136">INPUTS</span></span>

### <span data-ttu-id="64f8c-137">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="64f8c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="64f8c-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64f8c-138">OUTPUTS</span></span>

### <span data-ttu-id="64f8c-139">System. void</span><span class="sxs-lookup"><span data-stu-id="64f8c-139">System.Void</span></span>

### <span data-ttu-id="64f8c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64f8c-140">System.Boolean</span></span>

## <span data-ttu-id="64f8c-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64f8c-141">NOTES</span></span>

## <span data-ttu-id="64f8c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64f8c-142">RELATED LINKS</span></span>
