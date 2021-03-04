---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: d860e9f5992cb1bd8df9a3f7f14e51565412284b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975905"
---
# <span data-ttu-id="24e97-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="24e97-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="24e97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24e97-102">SYNOPSIS</span></span>
<span data-ttu-id="24e97-103">Usuwa tabelę BesandryDB.</span><span class="sxs-lookup"><span data-stu-id="24e97-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="24e97-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="24e97-104">SYNTAX</span></span>

### <span data-ttu-id="24e97-105">ByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="24e97-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24e97-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24e97-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24e97-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="24e97-107">DESCRIPTION</span></span>
<span data-ttu-id="24e97-108">Tabela **Remove-AzCosmosDBCassandraTable** usuwa tabelę CassandrasDB.</span><span class="sxs-lookup"><span data-stu-id="24e97-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="24e97-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="24e97-109">EXAMPLES</span></span>

### <span data-ttu-id="24e97-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24e97-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="24e97-111">Polecenie cmdlet zwraca obiekt typu bool(po przekazaniu wartości -PassThru), co jest prawdziwe, jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="24e97-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="24e97-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24e97-112">PARAMETERS</span></span>

### <span data-ttu-id="24e97-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24e97-113">-AccountName</span></span>
<span data-ttu-id="24e97-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="24e97-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="24e97-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24e97-115">-Confirm</span></span>
<span data-ttu-id="24e97-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="24e97-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e97-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e97-117">-DefaultProfile</span></span>
<span data-ttu-id="24e97-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="24e97-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24e97-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24e97-119">-InputObject</span></span>
<span data-ttu-id="24e97-120">Obiekt Cassandra Table.</span><span class="sxs-lookup"><span data-stu-id="24e97-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24e97-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="24e97-121">-KeyspaceName</span></span>
<span data-ttu-id="24e97-122">Nazwa klawiszy Cassandra.</span><span class="sxs-lookup"><span data-stu-id="24e97-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="24e97-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="24e97-123">-Name</span></span>
<span data-ttu-id="24e97-124">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="24e97-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="24e97-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24e97-125">-PassThru</span></span>
<span data-ttu-id="24e97-126">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="24e97-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="24e97-127">Dane wyjściowe są prawdziwe, jeśli operacja została pomyślnie i jeśli nie, zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="24e97-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="24e97-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24e97-128">-ResourceGroupName</span></span>
<span data-ttu-id="24e97-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="24e97-129">Name of resource group.</span></span>

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

### <span data-ttu-id="24e97-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e97-130">-WhatIf</span></span>
<span data-ttu-id="24e97-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24e97-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24e97-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="24e97-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24e97-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e97-133">CommonParameters</span></span>
<span data-ttu-id="24e97-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24e97-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e97-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24e97-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e97-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24e97-136">INPUTS</span></span>

### <span data-ttu-id="24e97-137">Microsoft.Azure.Commands.DoceńDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="24e97-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="24e97-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24e97-138">OUTPUTS</span></span>

### <span data-ttu-id="24e97-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="24e97-139">System.Void</span></span>

### <span data-ttu-id="24e97-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24e97-140">System.Boolean</span></span>

## <span data-ttu-id="24e97-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="24e97-141">NOTES</span></span>

## <span data-ttu-id="24e97-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24e97-142">RELATED LINKS</span></span>
