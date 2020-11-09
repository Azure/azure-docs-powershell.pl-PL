---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306900"
---
# <span data-ttu-id="0bcd4-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="0bcd4-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="0bcd4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0bcd4-102">SYNOPSIS</span></span>
<span data-ttu-id="0bcd4-103">Usuwa kontener SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="0bcd4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0bcd4-104">SYNTAX</span></span>

### <span data-ttu-id="0bcd4-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0bcd4-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bcd4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bcd4-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bcd4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0bcd4-107">DESCRIPTION</span></span>
<span data-ttu-id="0bcd4-108">Polecenie cmdlet **Remove-AzCosmosDBSqlContainer** usuwa kontener SQL CosmosDB odpowiadający podanemu ResourceGroupName, AccountName, DatabaseName i kontenerze.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="0bcd4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0bcd4-109">EXAMPLES</span></span>

### <span data-ttu-id="0bcd4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0bcd4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="0bcd4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0bcd4-111">PARAMETERS</span></span>

### <span data-ttu-id="0bcd4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0bcd4-112">-AccountName</span></span>
<span data-ttu-id="0bcd4-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0bcd4-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0bcd4-114">-Confirm</span></span>
<span data-ttu-id="0bcd4-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bcd4-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0bcd4-116">-DatabaseName</span></span>
<span data-ttu-id="0bcd4-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-117">Database name.</span></span>

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

### <span data-ttu-id="0bcd4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bcd4-118">-DefaultProfile</span></span>
<span data-ttu-id="0bcd4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bcd4-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0bcd4-120">-InputObject</span></span>
<span data-ttu-id="0bcd4-121">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bcd4-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0bcd4-122">-Name</span></span>
<span data-ttu-id="0bcd4-123">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-123">Container name.</span></span>

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

### <span data-ttu-id="0bcd4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bcd4-124">-PassThru</span></span>
<span data-ttu-id="0bcd4-125">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="0bcd4-126">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="0bcd4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bcd4-127">-ResourceGroupName</span></span>
<span data-ttu-id="0bcd4-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-128">Name of resource group.</span></span>

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

### <span data-ttu-id="0bcd4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bcd4-129">-WhatIf</span></span>
<span data-ttu-id="0bcd4-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bcd4-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bcd4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bcd4-132">CommonParameters</span></span>
<span data-ttu-id="0bcd4-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bcd4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bcd4-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bcd4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bcd4-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bcd4-135">INPUTS</span></span>

### <span data-ttu-id="0bcd4-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0bcd4-136">None</span></span>

## <span data-ttu-id="0bcd4-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0bcd4-137">OUTPUTS</span></span>

### <span data-ttu-id="0bcd4-138">System. void</span><span class="sxs-lookup"><span data-stu-id="0bcd4-138">System.Void</span></span>

### <span data-ttu-id="0bcd4-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0bcd4-139">System.Boolean</span></span>

## <span data-ttu-id="0bcd4-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0bcd4-140">NOTES</span></span>

## <span data-ttu-id="0bcd4-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0bcd4-141">RELATED LINKS</span></span>
