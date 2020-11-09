---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306865"
---
# <span data-ttu-id="67ae7-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="67ae7-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="67ae7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="67ae7-103">Usuwa CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="67ae7-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="67ae7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67ae7-104">SYNTAX</span></span>

### <span data-ttu-id="67ae7-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="67ae7-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67ae7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67ae7-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67ae7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="67ae7-107">DESCRIPTION</span></span>
<span data-ttu-id="67ae7-108">Polecenie cmdlet **Remove-AzCosmosDBSqlUserDefinedFunction** usuwa CosmosDB SQL UserDefinedFunction odpowiadającą podanemu ResourceGroupName, AccountName i DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="67ae7-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="67ae7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67ae7-109">EXAMPLES</span></span>

### <span data-ttu-id="67ae7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67ae7-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="67ae7-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67ae7-111">PARAMETERS</span></span>

### <span data-ttu-id="67ae7-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="67ae7-112">-AccountName</span></span>
<span data-ttu-id="67ae7-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="67ae7-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="67ae7-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67ae7-114">-Confirm</span></span>
<span data-ttu-id="67ae7-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67ae7-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67ae7-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="67ae7-116">-ContainerName</span></span>
<span data-ttu-id="67ae7-117">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="67ae7-117">Container name.</span></span>

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

### <span data-ttu-id="67ae7-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="67ae7-118">-DatabaseName</span></span>
<span data-ttu-id="67ae7-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="67ae7-119">Database name.</span></span>

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

### <span data-ttu-id="67ae7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ae7-120">-DefaultProfile</span></span>
<span data-ttu-id="67ae7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="67ae7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ae7-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="67ae7-122">-InputObject</span></span>
<span data-ttu-id="67ae7-123">Obiekt funkcji zdefiniowanej przez użytkownika SQL</span><span class="sxs-lookup"><span data-stu-id="67ae7-123">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67ae7-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="67ae7-124">-Name</span></span>
<span data-ttu-id="67ae7-125">Nazwa funkcji zdefiniowana przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="67ae7-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="67ae7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67ae7-126">-PassThru</span></span>
<span data-ttu-id="67ae7-127">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="67ae7-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="67ae7-128">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="67ae7-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="67ae7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ae7-129">-ResourceGroupName</span></span>
<span data-ttu-id="67ae7-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="67ae7-130">Name of resource group.</span></span>

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

### <span data-ttu-id="67ae7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67ae7-131">-WhatIf</span></span>
<span data-ttu-id="67ae7-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67ae7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67ae7-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="67ae7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67ae7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ae7-134">CommonParameters</span></span>
<span data-ttu-id="67ae7-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ae7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ae7-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67ae7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ae7-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67ae7-137">INPUTS</span></span>

### <span data-ttu-id="67ae7-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="67ae7-138">None</span></span>

## <span data-ttu-id="67ae7-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67ae7-139">OUTPUTS</span></span>

### <span data-ttu-id="67ae7-140">System. void</span><span class="sxs-lookup"><span data-stu-id="67ae7-140">System.Void</span></span>

### <span data-ttu-id="67ae7-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67ae7-141">System.Boolean</span></span>

## <span data-ttu-id="67ae7-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67ae7-142">NOTES</span></span>

## <span data-ttu-id="67ae7-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67ae7-143">RELATED LINKS</span></span>
