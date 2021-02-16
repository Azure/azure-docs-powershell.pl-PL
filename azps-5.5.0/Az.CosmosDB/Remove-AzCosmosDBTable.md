---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ab8f0367f932a96d6296b5e6174bc3b6bbb651f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238430"
---
# <span data-ttu-id="667cc-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="667cc-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="667cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="667cc-102">SYNOPSIS</span></span>
<span data-ttu-id="667cc-103">Usuwa tabelę AniaDB.</span><span class="sxs-lookup"><span data-stu-id="667cc-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="667cc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="667cc-104">SYNTAX</span></span>

### <span data-ttu-id="667cc-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="667cc-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667cc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="667cc-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="667cc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="667cc-107">DESCRIPTION</span></span>
<span data-ttu-id="667cc-108">Polecenie **cmdlet Remove-AzCosmosDBTable** usuwa tabelę GrysDB.</span><span class="sxs-lookup"><span data-stu-id="667cc-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="667cc-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="667cc-109">EXAMPLES</span></span>

### <span data-ttu-id="667cc-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="667cc-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="667cc-111">Polecenie cmdlet zwraca obiekt typu bool(po przekazaniu wartości -PassThru), co jest prawdziwe, jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="667cc-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="667cc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="667cc-112">PARAMETERS</span></span>

### <span data-ttu-id="667cc-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="667cc-113">-AccountName</span></span>
<span data-ttu-id="667cc-114">Nazwa konta bazy danych Wsad.</span><span class="sxs-lookup"><span data-stu-id="667cc-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="667cc-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="667cc-115">-Confirm</span></span>
<span data-ttu-id="667cc-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="667cc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="667cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667cc-117">-DefaultProfile</span></span>
<span data-ttu-id="667cc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="667cc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="667cc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="667cc-119">-InputObject</span></span>
<span data-ttu-id="667cc-120">Obiekt Sql Database.</span><span class="sxs-lookup"><span data-stu-id="667cc-120">Sql Database object.</span></span>

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

### <span data-ttu-id="667cc-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="667cc-121">-Name</span></span>
<span data-ttu-id="667cc-122">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="667cc-122">Name of the Table.</span></span>

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

### <span data-ttu-id="667cc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="667cc-123">-PassThru</span></span>
<span data-ttu-id="667cc-124">Wartość True (Prawda), jeśli użytkownik chce otrzymać dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="667cc-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="667cc-125">Dane wyjściowe są prawdziwe, jeśli operacja została pomyślnie i jeśli nie, zostanie wygenerowany błąd.</span><span class="sxs-lookup"><span data-stu-id="667cc-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="667cc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667cc-126">-ResourceGroupName</span></span>
<span data-ttu-id="667cc-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="667cc-127">Name of resource group.</span></span>

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

### <span data-ttu-id="667cc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="667cc-128">-WhatIf</span></span>
<span data-ttu-id="667cc-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="667cc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="667cc-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="667cc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="667cc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667cc-131">CommonParameters</span></span>
<span data-ttu-id="667cc-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="667cc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667cc-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="667cc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667cc-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="667cc-134">INPUTS</span></span>

### <span data-ttu-id="667cc-135">Microsoft.Azure.Commands.Dosdb.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="667cc-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="667cc-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="667cc-136">OUTPUTS</span></span>

### <span data-ttu-id="667cc-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="667cc-137">System.Void</span></span>

### <span data-ttu-id="667cc-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="667cc-138">System.Boolean</span></span>

## <span data-ttu-id="667cc-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="667cc-139">NOTES</span></span>

## <span data-ttu-id="667cc-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="667cc-140">RELATED LINKS</span></span>
