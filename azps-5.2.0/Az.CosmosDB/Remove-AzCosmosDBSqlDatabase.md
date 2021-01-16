---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351538"
---
# <span data-ttu-id="6148e-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6148e-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="6148e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6148e-102">SYNOPSIS</span></span>
<span data-ttu-id="6148e-103">Usuwa bazę danych SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6148e-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="6148e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6148e-104">SYNTAX</span></span>

### <span data-ttu-id="6148e-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6148e-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6148e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6148e-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6148e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6148e-107">DESCRIPTION</span></span>
<span data-ttu-id="6148e-108">Polecenie cmdlet **Remove-AzCosmosDBSqlDatabase** usuwa CosmosDB bazę danych SQL odpowiadającą danemu ResourceGroupName, AccountName i DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="6148e-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="6148e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6148e-109">EXAMPLES</span></span>

### <span data-ttu-id="6148e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6148e-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="6148e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6148e-111">PARAMETERS</span></span>

### <span data-ttu-id="6148e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6148e-112">-AccountName</span></span>
<span data-ttu-id="6148e-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="6148e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6148e-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6148e-114">-Confirm</span></span>
<span data-ttu-id="6148e-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6148e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6148e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6148e-116">-DefaultProfile</span></span>
<span data-ttu-id="6148e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6148e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6148e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6148e-118">-InputObject</span></span>
<span data-ttu-id="6148e-119">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6148e-119">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6148e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6148e-120">-Name</span></span>
<span data-ttu-id="6148e-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6148e-121">Database name.</span></span>

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

### <span data-ttu-id="6148e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6148e-122">-PassThru</span></span>
<span data-ttu-id="6148e-123">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="6148e-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="6148e-124">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="6148e-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="6148e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6148e-125">-ResourceGroupName</span></span>
<span data-ttu-id="6148e-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6148e-126">Name of resource group.</span></span>

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

### <span data-ttu-id="6148e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6148e-127">-WhatIf</span></span>
<span data-ttu-id="6148e-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6148e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6148e-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6148e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6148e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6148e-130">CommonParameters</span></span>
<span data-ttu-id="6148e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6148e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6148e-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6148e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6148e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6148e-133">INPUTS</span></span>

### <span data-ttu-id="6148e-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6148e-134">None</span></span>

## <span data-ttu-id="6148e-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6148e-135">OUTPUTS</span></span>

### <span data-ttu-id="6148e-136">System. void</span><span class="sxs-lookup"><span data-stu-id="6148e-136">System.Void</span></span>

### <span data-ttu-id="6148e-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6148e-137">System.Boolean</span></span>

## <span data-ttu-id="6148e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6148e-138">NOTES</span></span>

## <span data-ttu-id="6148e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6148e-139">RELATED LINKS</span></span>
