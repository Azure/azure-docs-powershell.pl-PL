---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501703"
---
# <span data-ttu-id="dd234-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="dd234-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="dd234-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd234-102">SYNOPSIS</span></span>
<span data-ttu-id="dd234-103">Usuwa CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="dd234-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="dd234-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd234-104">SYNTAX</span></span>

### <span data-ttu-id="dd234-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd234-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd234-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd234-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd234-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dd234-107">DESCRIPTION</span></span>
<span data-ttu-id="dd234-108">Polecenie cmdlet **Remove-AzCosmosDBSqlStoredProcedure** usuwa CosmosDB SQL StoredProcedure odpowiadającą podanemu ResourceGroupName, AccountName i DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="dd234-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="dd234-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd234-109">EXAMPLES</span></span>

### <span data-ttu-id="dd234-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dd234-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="dd234-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd234-111">PARAMETERS</span></span>

### <span data-ttu-id="dd234-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dd234-112">-AccountName</span></span>
<span data-ttu-id="dd234-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="dd234-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dd234-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd234-114">-Confirm</span></span>
<span data-ttu-id="dd234-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd234-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd234-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="dd234-116">-ContainerName</span></span>
<span data-ttu-id="dd234-117">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="dd234-117">Container name.</span></span>

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

### <span data-ttu-id="dd234-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd234-118">-DatabaseName</span></span>
<span data-ttu-id="dd234-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="dd234-119">Database name.</span></span>

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

### <span data-ttu-id="dd234-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd234-120">-DefaultProfile</span></span>
<span data-ttu-id="dd234-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd234-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd234-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dd234-122">-InputObject</span></span>
<span data-ttu-id="dd234-123">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="dd234-123">Sql Database object.</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd234-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd234-124">-Name</span></span>
<span data-ttu-id="dd234-125">Nazwa zapisanego Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="dd234-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="dd234-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd234-126">-PassThru</span></span>
<span data-ttu-id="dd234-127">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="dd234-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="dd234-128">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="dd234-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="dd234-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd234-129">-ResourceGroupName</span></span>
<span data-ttu-id="dd234-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd234-130">Name of resource group.</span></span>

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

### <span data-ttu-id="dd234-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd234-131">-WhatIf</span></span>
<span data-ttu-id="dd234-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd234-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd234-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dd234-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd234-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd234-134">CommonParameters</span></span>
<span data-ttu-id="dd234-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd234-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd234-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd234-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd234-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd234-137">INPUTS</span></span>

### <span data-ttu-id="dd234-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dd234-138">None</span></span>

## <span data-ttu-id="dd234-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd234-139">OUTPUTS</span></span>

### <span data-ttu-id="dd234-140">System. void</span><span class="sxs-lookup"><span data-stu-id="dd234-140">System.Void</span></span>

### <span data-ttu-id="dd234-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd234-141">System.Boolean</span></span>

## <span data-ttu-id="dd234-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd234-142">NOTES</span></span>

## <span data-ttu-id="dd234-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd234-143">RELATED LINKS</span></span>
