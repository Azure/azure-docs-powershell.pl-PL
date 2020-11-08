---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 5c3150e2bdb81c8864116bc521b9f07f2ea43e1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064204"
---
# <span data-ttu-id="e5a15-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="e5a15-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="e5a15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5a15-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a15-103">Usuwa bazę danych programu CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="e5a15-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e5a15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5a15-104">SYNTAX</span></span>

### <span data-ttu-id="e5a15-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5a15-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5a15-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5a15-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5a15-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e5a15-107">DESCRIPTION</span></span>
<span data-ttu-id="e5a15-108">Polecenie cmdlet **Remove-AzCosmosDBGremlinDatabase** usuwa CosmosDB Gremlin Database.</span><span class="sxs-lookup"><span data-stu-id="e5a15-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e5a15-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5a15-109">EXAMPLES</span></span>

### <span data-ttu-id="e5a15-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5a15-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="e5a15-111">Polecenie cmdlet zwraca obiekt typu wartość logiczna (gdy przekazano parametr-PassThru) o wartości prawda, Jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="e5a15-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="e5a15-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5a15-112">PARAMETERS</span></span>

### <span data-ttu-id="e5a15-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e5a15-113">-AccountName</span></span>
<span data-ttu-id="e5a15-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e5a15-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e5a15-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5a15-115">-Confirm</span></span>
<span data-ttu-id="e5a15-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5a15-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a15-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a15-117">-DefaultProfile</span></span>
<span data-ttu-id="e5a15-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a15-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5a15-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e5a15-119">-InputObject</span></span>
<span data-ttu-id="e5a15-120">Obiekt bazy danych Gremlin.</span><span class="sxs-lookup"><span data-stu-id="e5a15-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a15-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e5a15-121">-Name</span></span>
<span data-ttu-id="e5a15-122">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e5a15-122">Database name.</span></span>

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

### <span data-ttu-id="e5a15-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5a15-123">-PassThru</span></span>
<span data-ttu-id="e5a15-124">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="e5a15-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="e5a15-125">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="e5a15-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="e5a15-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5a15-126">-ResourceGroupName</span></span>
<span data-ttu-id="e5a15-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e5a15-127">Name of resource group.</span></span>

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

### <span data-ttu-id="e5a15-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a15-128">-WhatIf</span></span>
<span data-ttu-id="e5a15-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5a15-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5a15-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e5a15-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a15-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a15-131">CommonParameters</span></span>
<span data-ttu-id="e5a15-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5a15-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a15-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5a15-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a15-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5a15-134">INPUTS</span></span>

### <span data-ttu-id="e5a15-135">Microsoft. Azure. Commands. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e5a15-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="e5a15-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5a15-136">OUTPUTS</span></span>

### <span data-ttu-id="e5a15-137">System. void</span><span class="sxs-lookup"><span data-stu-id="e5a15-137">System.Void</span></span>

### <span data-ttu-id="e5a15-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5a15-138">System.Boolean</span></span>

## <span data-ttu-id="e5a15-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5a15-139">NOTES</span></span>

## <span data-ttu-id="e5a15-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5a15-140">RELATED LINKS</span></span>
