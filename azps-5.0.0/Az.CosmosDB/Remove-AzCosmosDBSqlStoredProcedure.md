---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306888"
---
# <span data-ttu-id="90823-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="90823-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="90823-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90823-102">SYNOPSIS</span></span>
<span data-ttu-id="90823-103">Usuwa CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="90823-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="90823-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90823-104">SYNTAX</span></span>

### <span data-ttu-id="90823-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="90823-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90823-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90823-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90823-107">Opis</span><span class="sxs-lookup"><span data-stu-id="90823-107">DESCRIPTION</span></span>
<span data-ttu-id="90823-108">Polecenie cmdlet **Remove-AzCosmosDBSqlStoredProcedure** usuwa CosmosDB SQL StoredProcedure odpowiadającą podanemu ResourceGroupName, AccountName i DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="90823-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="90823-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90823-109">EXAMPLES</span></span>

### <span data-ttu-id="90823-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="90823-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="90823-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90823-111">PARAMETERS</span></span>

### <span data-ttu-id="90823-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="90823-112">-AccountName</span></span>
<span data-ttu-id="90823-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="90823-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="90823-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90823-114">-Confirm</span></span>
<span data-ttu-id="90823-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90823-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90823-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="90823-116">-ContainerName</span></span>
<span data-ttu-id="90823-117">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="90823-117">Container name.</span></span>

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

### <span data-ttu-id="90823-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="90823-118">-DatabaseName</span></span>
<span data-ttu-id="90823-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="90823-119">Database name.</span></span>

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

### <span data-ttu-id="90823-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90823-120">-DefaultProfile</span></span>
<span data-ttu-id="90823-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90823-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90823-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="90823-122">-InputObject</span></span>
<span data-ttu-id="90823-123">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="90823-123">Sql Database object.</span></span>

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

### <span data-ttu-id="90823-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90823-124">-Name</span></span>
<span data-ttu-id="90823-125">Nazwa zapisanego Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="90823-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="90823-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90823-126">-PassThru</span></span>
<span data-ttu-id="90823-127">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="90823-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="90823-128">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="90823-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="90823-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90823-129">-ResourceGroupName</span></span>
<span data-ttu-id="90823-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="90823-130">Name of resource group.</span></span>

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

### <span data-ttu-id="90823-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90823-131">-WhatIf</span></span>
<span data-ttu-id="90823-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90823-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90823-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="90823-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90823-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90823-134">CommonParameters</span></span>
<span data-ttu-id="90823-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90823-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90823-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90823-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90823-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90823-137">INPUTS</span></span>

### <span data-ttu-id="90823-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="90823-138">None</span></span>

## <span data-ttu-id="90823-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90823-139">OUTPUTS</span></span>

### <span data-ttu-id="90823-140">System. void</span><span class="sxs-lookup"><span data-stu-id="90823-140">System.Void</span></span>

### <span data-ttu-id="90823-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90823-141">System.Boolean</span></span>

## <span data-ttu-id="90823-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90823-142">NOTES</span></span>

## <span data-ttu-id="90823-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90823-143">RELATED LINKS</span></span>
