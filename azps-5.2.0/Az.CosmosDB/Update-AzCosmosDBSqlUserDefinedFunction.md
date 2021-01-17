---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345397"
---
# <span data-ttu-id="0fd8e-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="0fd8e-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="0fd8e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0fd8e-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd8e-103">Aktualizuje CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="0fd8e-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejące UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="0fd8e-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0fd8e-105">SYNTAX</span></span>

### <span data-ttu-id="0fd8e-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0fd8e-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fd8e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fd8e-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0fd8e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fd8e-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fd8e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="0fd8e-109">DESCRIPTION</span></span>
<span data-ttu-id="0fd8e-110">Aktualizuje CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="0fd8e-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejące UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="0fd8e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0fd8e-112">EXAMPLES</span></span>

### <span data-ttu-id="0fd8e-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0fd8e-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="0fd8e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0fd8e-114">PARAMETERS</span></span>

### <span data-ttu-id="0fd8e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0fd8e-115">-AccountName</span></span>
<span data-ttu-id="0fd8e-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0fd8e-117">-Body</span><span class="sxs-lookup"><span data-stu-id="0fd8e-117">-Body</span></span>
<span data-ttu-id="0fd8e-118">Treść funkcji zdefiniowanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-118">The body of the User Defined Function.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd8e-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0fd8e-119">-Confirm</span></span>
<span data-ttu-id="0fd8e-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fd8e-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="0fd8e-121">-ContainerName</span></span>
<span data-ttu-id="0fd8e-122">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-122">Container name.</span></span>

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

### <span data-ttu-id="0fd8e-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0fd8e-123">-DatabaseName</span></span>
<span data-ttu-id="0fd8e-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-124">Database name.</span></span>

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

### <span data-ttu-id="0fd8e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd8e-125">-DefaultProfile</span></span>
<span data-ttu-id="0fd8e-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fd8e-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0fd8e-127">-InputObject</span></span>
<span data-ttu-id="0fd8e-128">Obiekt funkcji zdefiniowanej przez użytkownika SQL</span><span class="sxs-lookup"><span data-stu-id="0fd8e-128">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="0fd8e-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0fd8e-129">-Name</span></span>
<span data-ttu-id="0fd8e-130">Nazwa funkcji zdefiniowana przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-130">User Defined Function Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd8e-131">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="0fd8e-131">-ParentObject</span></span>
<span data-ttu-id="0fd8e-132">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-132">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd8e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fd8e-133">-ResourceGroupName</span></span>
<span data-ttu-id="0fd8e-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-134">Name of resource group.</span></span>

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

### <span data-ttu-id="0fd8e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fd8e-135">-WhatIf</span></span>
<span data-ttu-id="0fd8e-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fd8e-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fd8e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd8e-138">CommonParameters</span></span>
<span data-ttu-id="0fd8e-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fd8e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd8e-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fd8e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd8e-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fd8e-141">INPUTS</span></span>

### <span data-ttu-id="0fd8e-142">Microsoft. Azure. Commands. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="0fd8e-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="0fd8e-143">Microsoft. Azure. Commands. CosmosDB. models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="0fd8e-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="0fd8e-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0fd8e-144">OUTPUTS</span></span>

### <span data-ttu-id="0fd8e-145">Microsoft. Azure. Commands. CosmosDB. models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="0fd8e-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="0fd8e-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="0fd8e-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="0fd8e-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0fd8e-147">NOTES</span></span>

## <span data-ttu-id="0fd8e-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fd8e-148">RELATED LINKS</span></span>
