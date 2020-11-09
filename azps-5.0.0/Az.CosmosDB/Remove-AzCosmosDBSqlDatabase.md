---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306894"
---
# <span data-ttu-id="d9adf-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d9adf-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="d9adf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9adf-102">SYNOPSIS</span></span>
<span data-ttu-id="d9adf-103">Usuwa bazę danych SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d9adf-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="d9adf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9adf-104">SYNTAX</span></span>

### <span data-ttu-id="d9adf-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9adf-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9adf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9adf-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9adf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d9adf-107">DESCRIPTION</span></span>
<span data-ttu-id="d9adf-108">Polecenie cmdlet **Remove-AzCosmosDBSqlDatabase** usuwa CosmosDB bazę danych SQL odpowiadającą danemu ResourceGroupName, AccountName i DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="d9adf-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="d9adf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9adf-109">EXAMPLES</span></span>

### <span data-ttu-id="d9adf-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9adf-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="d9adf-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9adf-111">PARAMETERS</span></span>

### <span data-ttu-id="d9adf-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d9adf-112">-AccountName</span></span>
<span data-ttu-id="d9adf-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="d9adf-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d9adf-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9adf-114">-Confirm</span></span>
<span data-ttu-id="d9adf-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9adf-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9adf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9adf-116">-DefaultProfile</span></span>
<span data-ttu-id="d9adf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9adf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9adf-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d9adf-118">-InputObject</span></span>
<span data-ttu-id="d9adf-119">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d9adf-119">Sql Database object.</span></span>

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

### <span data-ttu-id="d9adf-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d9adf-120">-Name</span></span>
<span data-ttu-id="d9adf-121">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d9adf-121">Database name.</span></span>

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

### <span data-ttu-id="d9adf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9adf-122">-PassThru</span></span>
<span data-ttu-id="d9adf-123">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="d9adf-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="d9adf-124">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="d9adf-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="d9adf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9adf-125">-ResourceGroupName</span></span>
<span data-ttu-id="d9adf-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9adf-126">Name of resource group.</span></span>

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

### <span data-ttu-id="d9adf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9adf-127">-WhatIf</span></span>
<span data-ttu-id="d9adf-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9adf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9adf-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d9adf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9adf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9adf-130">CommonParameters</span></span>
<span data-ttu-id="d9adf-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9adf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9adf-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9adf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9adf-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9adf-133">INPUTS</span></span>

### <span data-ttu-id="d9adf-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d9adf-134">None</span></span>

## <span data-ttu-id="d9adf-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9adf-135">OUTPUTS</span></span>

### <span data-ttu-id="d9adf-136">System. void</span><span class="sxs-lookup"><span data-stu-id="d9adf-136">System.Void</span></span>

### <span data-ttu-id="d9adf-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9adf-137">System.Boolean</span></span>

## <span data-ttu-id="d9adf-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9adf-138">NOTES</span></span>

## <span data-ttu-id="d9adf-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9adf-139">RELATED LINKS</span></span>
