---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ab8f0367f932a96d6296b5e6174bc3b6bbb651f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503795"
---
# <span data-ttu-id="af68a-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="af68a-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="af68a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af68a-102">SYNOPSIS</span></span>
<span data-ttu-id="af68a-103">Usuwa tabelę CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="af68a-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="af68a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af68a-104">SYNTAX</span></span>

### <span data-ttu-id="af68a-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af68a-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af68a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af68a-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af68a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="af68a-107">DESCRIPTION</span></span>
<span data-ttu-id="af68a-108">Polecenie cmdlet **Remove-AzCosmosDBTable** usuwa tabelę CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="af68a-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="af68a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af68a-109">EXAMPLES</span></span>

### <span data-ttu-id="af68a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="af68a-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="af68a-111">Polecenie cmdlet zwraca obiekt typu wartość logiczna (gdy przekazano parametr-PassThru) o wartości prawda, Jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="af68a-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="af68a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af68a-112">PARAMETERS</span></span>

### <span data-ttu-id="af68a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="af68a-113">-AccountName</span></span>
<span data-ttu-id="af68a-114">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="af68a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="af68a-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af68a-115">-Confirm</span></span>
<span data-ttu-id="af68a-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af68a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af68a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af68a-117">-DefaultProfile</span></span>
<span data-ttu-id="af68a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af68a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af68a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="af68a-119">-InputObject</span></span>
<span data-ttu-id="af68a-120">Obiekt bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="af68a-120">Sql Database object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af68a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af68a-121">-Name</span></span>
<span data-ttu-id="af68a-122">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="af68a-122">Name of the Table.</span></span>

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

### <span data-ttu-id="af68a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af68a-123">-PassThru</span></span>
<span data-ttu-id="af68a-124">Na wartość PRAWDA, jeśli użytkownik chce odebrać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="af68a-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="af68a-125">Wynik ma wartość PRAWDA, jeśli operacja zakończyła się powodzeniem, w przeciwnym razie jest zwracany błąd.</span><span class="sxs-lookup"><span data-stu-id="af68a-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="af68a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af68a-126">-ResourceGroupName</span></span>
<span data-ttu-id="af68a-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="af68a-127">Name of resource group.</span></span>

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

### <span data-ttu-id="af68a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af68a-128">-WhatIf</span></span>
<span data-ttu-id="af68a-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af68a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af68a-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="af68a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af68a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af68a-131">CommonParameters</span></span>
<span data-ttu-id="af68a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af68a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af68a-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af68a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af68a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af68a-134">INPUTS</span></span>

### <span data-ttu-id="af68a-135">Microsoft. Azure. Commands. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="af68a-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="af68a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af68a-136">OUTPUTS</span></span>

### <span data-ttu-id="af68a-137">System. void</span><span class="sxs-lookup"><span data-stu-id="af68a-137">System.Void</span></span>

### <span data-ttu-id="af68a-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af68a-138">System.Boolean</span></span>

## <span data-ttu-id="af68a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af68a-139">NOTES</span></span>

## <span data-ttu-id="af68a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af68a-140">RELATED LINKS</span></span>
