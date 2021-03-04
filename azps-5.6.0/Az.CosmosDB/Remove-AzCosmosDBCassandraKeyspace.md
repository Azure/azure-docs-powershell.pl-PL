---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 849f716787c01c5810af74c37e97bbdb0bd2ef13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954753"
---
# <span data-ttu-id="8907e-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="8907e-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="8907e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8907e-102">SYNOPSIS</span></span>
<span data-ttu-id="8907e-103">Usuwa spację cassandra (Cassandra Keyspace).</span><span class="sxs-lookup"><span data-stu-id="8907e-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="8907e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8907e-104">SYNTAX</span></span>

### <span data-ttu-id="8907e-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8907e-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8907e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8907e-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8907e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8907e-107">DESCRIPTION</span></span>
<span data-ttu-id="8907e-108">Polecenie **cmdlet Remove-AzCosmosDBCassandraKeyspace** usuwa istniejącą spację Cassandra Keyspace bazy DanychDb.</span><span class="sxs-lookup"><span data-stu-id="8907e-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="8907e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8907e-109">EXAMPLES</span></span>

### <span data-ttu-id="8907e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8907e-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="8907e-111">Polecenie cmdlet zwraca obiekt typu bool(po przekazaniu wartości -PassThru), co jest prawdziwe, jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="8907e-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="8907e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8907e-112">PARAMETERS</span></span>

### <span data-ttu-id="8907e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8907e-113">-AccountName</span></span>
<span data-ttu-id="8907e-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="8907e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8907e-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8907e-115">-Confirm</span></span>
<span data-ttu-id="8907e-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8907e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8907e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8907e-117">-DefaultProfile</span></span>
<span data-ttu-id="8907e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8907e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8907e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8907e-119">-InputObject</span></span>
<span data-ttu-id="8907e-120">Obiekt Cassandra Keyspace.</span><span class="sxs-lookup"><span data-stu-id="8907e-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="8907e-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8907e-121">-Name</span></span>
<span data-ttu-id="8907e-122">Nazwa klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="8907e-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="8907e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8907e-123">-PassThru</span></span>
<span data-ttu-id="8907e-124">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="8907e-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="8907e-125">Dane wyjściowe są prawdziwe, jeśli operacja została pomyślnie i jeśli nie, zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="8907e-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="8907e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8907e-126">-ResourceGroupName</span></span>
<span data-ttu-id="8907e-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8907e-127">Name of resource group.</span></span>

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

### <span data-ttu-id="8907e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8907e-128">-WhatIf</span></span>
<span data-ttu-id="8907e-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8907e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8907e-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8907e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8907e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8907e-131">CommonParameters</span></span>
<span data-ttu-id="8907e-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8907e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8907e-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8907e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8907e-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8907e-134">INPUTS</span></span>

### <span data-ttu-id="8907e-135">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="8907e-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="8907e-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8907e-136">OUTPUTS</span></span>

### <span data-ttu-id="8907e-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="8907e-137">System.Void</span></span>

### <span data-ttu-id="8907e-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8907e-138">System.Boolean</span></span>

## <span data-ttu-id="8907e-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8907e-139">NOTES</span></span>

## <span data-ttu-id="8907e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8907e-140">RELATED LINKS</span></span>
