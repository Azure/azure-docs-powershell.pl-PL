---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503804"
---
# <span data-ttu-id="28641-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="28641-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="28641-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28641-102">SYNOPSIS</span></span>
<span data-ttu-id="28641-103">Usuwa tabelę Cassandra CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="28641-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="28641-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28641-104">SYNTAX</span></span>

### <span data-ttu-id="28641-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="28641-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28641-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28641-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28641-107">Opis</span><span class="sxs-lookup"><span data-stu-id="28641-107">DESCRIPTION</span></span>
<span data-ttu-id="28641-108">**AzCosmosDBCassandraTable** usuwanie CosmosDB Cassandra tabeli.</span><span class="sxs-lookup"><span data-stu-id="28641-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="28641-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28641-109">EXAMPLES</span></span>

### <span data-ttu-id="28641-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="28641-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="28641-111">Polecenie cmdlet zwraca obiekt typu wartość logiczna (gdy przekazano parametr-PassThru) o wartości prawda, Jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="28641-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="28641-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28641-112">PARAMETERS</span></span>

### <span data-ttu-id="28641-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="28641-113">-AccountName</span></span>
<span data-ttu-id="28641-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="28641-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="28641-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28641-115">-Confirm</span></span>
<span data-ttu-id="28641-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28641-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28641-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28641-117">-DefaultProfile</span></span>
<span data-ttu-id="28641-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28641-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28641-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="28641-119">-InputObject</span></span>
<span data-ttu-id="28641-120">Obiekt tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="28641-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="28641-121">-Spacename</span><span class="sxs-lookup"><span data-stu-id="28641-121">-KeyspaceName</span></span>
<span data-ttu-id="28641-122">Cassandra nazwa obszaru.</span><span class="sxs-lookup"><span data-stu-id="28641-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="28641-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28641-123">-Name</span></span>
<span data-ttu-id="28641-124">Nazwa tabeli Cassandra.</span><span class="sxs-lookup"><span data-stu-id="28641-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="28641-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28641-125">-PassThru</span></span>
<span data-ttu-id="28641-126">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="28641-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="28641-127">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="28641-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="28641-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28641-128">-ResourceGroupName</span></span>
<span data-ttu-id="28641-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="28641-129">Name of resource group.</span></span>

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

### <span data-ttu-id="28641-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28641-130">-WhatIf</span></span>
<span data-ttu-id="28641-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28641-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28641-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="28641-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28641-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28641-133">CommonParameters</span></span>
<span data-ttu-id="28641-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28641-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28641-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28641-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28641-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28641-136">INPUTS</span></span>

### <span data-ttu-id="28641-137">Microsoft. Azure. Commands. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="28641-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="28641-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28641-138">OUTPUTS</span></span>

### <span data-ttu-id="28641-139">System. void</span><span class="sxs-lookup"><span data-stu-id="28641-139">System.Void</span></span>

### <span data-ttu-id="28641-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28641-140">System.Boolean</span></span>

## <span data-ttu-id="28641-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28641-141">NOTES</span></span>

## <span data-ttu-id="28641-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28641-142">RELATED LINKS</span></span>
