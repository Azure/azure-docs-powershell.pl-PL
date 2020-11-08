---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052583"
---
# <span data-ttu-id="88c87-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="88c87-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="88c87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88c87-102">SYNOPSIS</span></span>
<span data-ttu-id="88c87-103">Usuwa bazę danych programu CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="88c87-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="88c87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88c87-104">SYNTAX</span></span>

### <span data-ttu-id="88c87-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="88c87-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88c87-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88c87-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88c87-107">Opis</span><span class="sxs-lookup"><span data-stu-id="88c87-107">DESCRIPTION</span></span>
<span data-ttu-id="88c87-108">Polecenie cmdlet **Remove-AzCosmosDBMongoDBDatabase** usuwa CosmosDB MongoDB Database.</span><span class="sxs-lookup"><span data-stu-id="88c87-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="88c87-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88c87-109">EXAMPLES</span></span>

### <span data-ttu-id="88c87-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88c87-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="88c87-111">Polecenie cmdlet zwraca obiekt typu wartość logiczna (gdy przekazano parametr-PassThru) o wartości prawda, Jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="88c87-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="88c87-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88c87-112">PARAMETERS</span></span>

### <span data-ttu-id="88c87-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="88c87-113">-AccountName</span></span>
<span data-ttu-id="88c87-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="88c87-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="88c87-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88c87-115">-Confirm</span></span>
<span data-ttu-id="88c87-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88c87-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88c87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88c87-117">-DefaultProfile</span></span>
<span data-ttu-id="88c87-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88c87-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88c87-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="88c87-119">-InputObject</span></span>
<span data-ttu-id="88c87-120">Obiekt bazy danych Mongo.</span><span class="sxs-lookup"><span data-stu-id="88c87-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88c87-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88c87-121">-Name</span></span>
<span data-ttu-id="88c87-122">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="88c87-122">Database name.</span></span>

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

### <span data-ttu-id="88c87-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88c87-123">-PassThru</span></span>
<span data-ttu-id="88c87-124">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="88c87-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="88c87-125">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="88c87-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="88c87-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88c87-126">-ResourceGroupName</span></span>
<span data-ttu-id="88c87-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="88c87-127">Name of resource group.</span></span>

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

### <span data-ttu-id="88c87-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88c87-128">-WhatIf</span></span>
<span data-ttu-id="88c87-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88c87-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88c87-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88c87-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88c87-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c87-131">CommonParameters</span></span>
<span data-ttu-id="88c87-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88c87-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c87-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88c87-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c87-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88c87-134">INPUTS</span></span>

### <span data-ttu-id="88c87-135">Microsoft. Azure. Commands. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="88c87-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="88c87-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88c87-136">OUTPUTS</span></span>

### <span data-ttu-id="88c87-137">System. void</span><span class="sxs-lookup"><span data-stu-id="88c87-137">System.Void</span></span>

### <span data-ttu-id="88c87-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88c87-138">System.Boolean</span></span>

## <span data-ttu-id="88c87-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88c87-139">NOTES</span></span>

## <span data-ttu-id="88c87-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88c87-140">RELATED LINKS</span></span>
