---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501704"
---
# <span data-ttu-id="28e40-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="28e40-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="28e40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28e40-102">SYNOPSIS</span></span>
<span data-ttu-id="28e40-103">Usuwa kontener SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="28e40-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="28e40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28e40-104">SYNTAX</span></span>

### <span data-ttu-id="28e40-105">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="28e40-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28e40-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28e40-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28e40-107">Opis</span><span class="sxs-lookup"><span data-stu-id="28e40-107">DESCRIPTION</span></span>
<span data-ttu-id="28e40-108">Polecenie cmdlet **Remove-AzCosmosDBSqlContainer** usuwa kontener SQL CosmosDB odpowiadający podanemu ResourceGroupName, AccountName, DatabaseName i kontenerze.</span><span class="sxs-lookup"><span data-stu-id="28e40-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="28e40-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28e40-109">EXAMPLES</span></span>

### <span data-ttu-id="28e40-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="28e40-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="28e40-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28e40-111">PARAMETERS</span></span>

### <span data-ttu-id="28e40-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="28e40-112">-AccountName</span></span>
<span data-ttu-id="28e40-113">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="28e40-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="28e40-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28e40-114">-Confirm</span></span>
<span data-ttu-id="28e40-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28e40-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28e40-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="28e40-116">-DatabaseName</span></span>
<span data-ttu-id="28e40-117">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="28e40-117">Database name.</span></span>

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

### <span data-ttu-id="28e40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28e40-118">-DefaultProfile</span></span>
<span data-ttu-id="28e40-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28e40-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28e40-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="28e40-120">-InputObject</span></span>
<span data-ttu-id="28e40-121">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="28e40-121">Sql Container object.</span></span>

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

### <span data-ttu-id="28e40-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28e40-122">-Name</span></span>
<span data-ttu-id="28e40-123">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="28e40-123">Container name.</span></span>

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

### <span data-ttu-id="28e40-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28e40-124">-PassThru</span></span>
<span data-ttu-id="28e40-125">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="28e40-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="28e40-126">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="28e40-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="28e40-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28e40-127">-ResourceGroupName</span></span>
<span data-ttu-id="28e40-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="28e40-128">Name of resource group.</span></span>

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

### <span data-ttu-id="28e40-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28e40-129">-WhatIf</span></span>
<span data-ttu-id="28e40-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28e40-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28e40-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="28e40-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28e40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e40-132">CommonParameters</span></span>
<span data-ttu-id="28e40-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28e40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e40-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28e40-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e40-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28e40-135">INPUTS</span></span>

### <span data-ttu-id="28e40-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="28e40-136">None</span></span>

## <span data-ttu-id="28e40-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28e40-137">OUTPUTS</span></span>

### <span data-ttu-id="28e40-138">System. void</span><span class="sxs-lookup"><span data-stu-id="28e40-138">System.Void</span></span>

### <span data-ttu-id="28e40-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28e40-139">System.Boolean</span></span>

## <span data-ttu-id="28e40-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28e40-140">NOTES</span></span>

## <span data-ttu-id="28e40-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28e40-141">RELATED LINKS</span></span>
