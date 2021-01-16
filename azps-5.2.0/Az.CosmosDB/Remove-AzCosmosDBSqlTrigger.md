---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 8aca11c8ce56c42842e96fa1e3623979612ffec7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357007"
---
# <span data-ttu-id="c2c4c-101">Remove-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="c2c4c-101">Remove-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="c2c4c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c4c-103">Usuwa wyzwalacz SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-103">Deletes the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="c2c4c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2c4c-104">SYNTAX</span></span>

### <span data-ttu-id="c2c4c-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2c4c-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c4c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2c4c-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -InputObject <PSSqlTriggerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2c4c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c2c4c-107">DESCRIPTION</span></span>
<span data-ttu-id="c2c4c-108">Polecenie cmdlet **Remove-AzCosmosDBSqlTrigger** usuwa wyzwalacz SQL CosmosDB odpowiadający podanemu ResourceGroupName, AccountName i DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-108">The **Remove-AzCosmosDBSqlTrigger** cmdlet deletes the CosmosDB Sql Trigger corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="c2c4c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2c4c-109">EXAMPLES</span></span>

### <span data-ttu-id="c2c4c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2c4c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlTrigger -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {triggerName}
```

## <span data-ttu-id="c2c4c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2c4c-111">PARAMETERS</span></span>

### <span data-ttu-id="c2c4c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2c4c-112">-AccountName</span></span>
<span data-ttu-id="c2c4c-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c2c4c-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2c4c-114">-Confirm</span></span>
<span data-ttu-id="c2c4c-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2c4c-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c2c4c-116">-ContainerName</span></span>
<span data-ttu-id="c2c4c-117">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-117">Container name.</span></span>

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

### <span data-ttu-id="c2c4c-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2c4c-118">-DatabaseName</span></span>
<span data-ttu-id="c2c4c-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-119">Database name.</span></span>

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

### <span data-ttu-id="c2c4c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c4c-120">-DefaultProfile</span></span>
<span data-ttu-id="c2c4c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2c4c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2c4c-122">-InputObject</span></span>
<span data-ttu-id="c2c4c-123">Obiekt wyzwalacza SQL</span><span class="sxs-lookup"><span data-stu-id="c2c4c-123">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c4c-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2c4c-124">-Name</span></span>
<span data-ttu-id="c2c4c-125">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-125">Trigger name.</span></span>

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

### <span data-ttu-id="c2c4c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2c4c-126">-PassThru</span></span>
<span data-ttu-id="c2c4c-127">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="c2c4c-128">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="c2c4c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c4c-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2c4c-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-130">Name of resource group.</span></span>

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

### <span data-ttu-id="c2c4c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2c4c-131">-WhatIf</span></span>
<span data-ttu-id="c2c4c-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2c4c-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2c4c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c4c-134">CommonParameters</span></span>
<span data-ttu-id="c2c4c-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2c4c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c4c-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2c4c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c4c-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2c4c-137">INPUTS</span></span>

### <span data-ttu-id="c2c4c-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c2c4c-138">None</span></span>

## <span data-ttu-id="c2c4c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2c4c-139">OUTPUTS</span></span>

### <span data-ttu-id="c2c4c-140">System. void</span><span class="sxs-lookup"><span data-stu-id="c2c4c-140">System.Void</span></span>

### <span data-ttu-id="c2c4c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2c4c-141">System.Boolean</span></span>

## <span data-ttu-id="c2c4c-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2c4c-142">NOTES</span></span>

## <span data-ttu-id="c2c4c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2c4c-143">RELATED LINKS</span></span>
