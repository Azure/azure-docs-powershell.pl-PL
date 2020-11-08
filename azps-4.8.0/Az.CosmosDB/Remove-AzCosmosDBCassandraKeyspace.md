---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064205"
---
# <span data-ttu-id="1961c-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="1961c-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="1961c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1961c-102">SYNOPSIS</span></span>
<span data-ttu-id="1961c-103">Usuwa Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1961c-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1961c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1961c-104">SYNTAX</span></span>

### <span data-ttu-id="1961c-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1961c-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1961c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1961c-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1961c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1961c-107">DESCRIPTION</span></span>
<span data-ttu-id="1961c-108">Polecenie cmdlet **Remove-AzCosmosDBCassandraKeyspace** usuwa istniejące CosmosDB Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="1961c-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1961c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1961c-109">EXAMPLES</span></span>

### <span data-ttu-id="1961c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1961c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="1961c-111">Polecenie cmdlet zwraca obiekt typu wartość logiczna (gdy przekazano parametr-PassThru), który ma wartość PRAWDA, Jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="1961c-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="1961c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1961c-112">PARAMETERS</span></span>

### <span data-ttu-id="1961c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1961c-113">-AccountName</span></span>
<span data-ttu-id="1961c-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="1961c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1961c-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1961c-115">-Confirm</span></span>
<span data-ttu-id="1961c-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1961c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1961c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1961c-117">-DefaultProfile</span></span>
<span data-ttu-id="1961c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1961c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1961c-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1961c-119">-InputObject</span></span>
<span data-ttu-id="1961c-120">Obiekt Cassandra Space.</span><span class="sxs-lookup"><span data-stu-id="1961c-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1961c-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1961c-121">-Name</span></span>
<span data-ttu-id="1961c-122">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="1961c-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="1961c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1961c-123">-PassThru</span></span>
<span data-ttu-id="1961c-124">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="1961c-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="1961c-125">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="1961c-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="1961c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1961c-126">-ResourceGroupName</span></span>
<span data-ttu-id="1961c-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1961c-127">Name of resource group.</span></span>

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

### <span data-ttu-id="1961c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1961c-128">-WhatIf</span></span>
<span data-ttu-id="1961c-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1961c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1961c-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1961c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1961c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1961c-131">CommonParameters</span></span>
<span data-ttu-id="1961c-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1961c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1961c-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1961c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1961c-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1961c-134">INPUTS</span></span>

### <span data-ttu-id="1961c-135">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="1961c-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="1961c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1961c-136">OUTPUTS</span></span>

### <span data-ttu-id="1961c-137">System. void</span><span class="sxs-lookup"><span data-stu-id="1961c-137">System.Void</span></span>

### <span data-ttu-id="1961c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1961c-138">System.Boolean</span></span>

## <span data-ttu-id="1961c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1961c-139">NOTES</span></span>

## <span data-ttu-id="1961c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1961c-140">RELATED LINKS</span></span>
