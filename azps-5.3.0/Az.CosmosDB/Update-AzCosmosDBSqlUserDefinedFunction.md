---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503772"
---
# <span data-ttu-id="2c89b-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="2c89b-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="2c89b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c89b-102">SYNOPSIS</span></span>
<span data-ttu-id="2c89b-103">Aktualizuje CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="2c89b-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="2c89b-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejące UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="2c89b-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="2c89b-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c89b-105">SYNTAX</span></span>

### <span data-ttu-id="2c89b-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2c89b-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c89b-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c89b-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c89b-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c89b-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c89b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2c89b-109">DESCRIPTION</span></span>
<span data-ttu-id="2c89b-110">Aktualizuje CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="2c89b-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="2c89b-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejące UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="2c89b-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="2c89b-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c89b-112">EXAMPLES</span></span>

### <span data-ttu-id="2c89b-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2c89b-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="2c89b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c89b-114">PARAMETERS</span></span>

### <span data-ttu-id="2c89b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2c89b-115">-AccountName</span></span>
<span data-ttu-id="2c89b-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2c89b-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2c89b-117">-Body</span><span class="sxs-lookup"><span data-stu-id="2c89b-117">-Body</span></span>
<span data-ttu-id="2c89b-118">Treść funkcji zdefiniowanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2c89b-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="2c89b-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c89b-119">-Confirm</span></span>
<span data-ttu-id="2c89b-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c89b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c89b-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="2c89b-121">-ContainerName</span></span>
<span data-ttu-id="2c89b-122">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="2c89b-122">Container name.</span></span>

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

### <span data-ttu-id="2c89b-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2c89b-123">-DatabaseName</span></span>
<span data-ttu-id="2c89b-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2c89b-124">Database name.</span></span>

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

### <span data-ttu-id="2c89b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c89b-125">-DefaultProfile</span></span>
<span data-ttu-id="2c89b-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c89b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c89b-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2c89b-127">-InputObject</span></span>
<span data-ttu-id="2c89b-128">Obiekt funkcji zdefiniowanej przez użytkownika SQL</span><span class="sxs-lookup"><span data-stu-id="2c89b-128">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="2c89b-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c89b-129">-Name</span></span>
<span data-ttu-id="2c89b-130">Nazwa funkcji zdefiniowana przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2c89b-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="2c89b-131">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="2c89b-131">-ParentObject</span></span>
<span data-ttu-id="2c89b-132">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="2c89b-132">Sql Container object.</span></span>

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

### <span data-ttu-id="2c89b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c89b-133">-ResourceGroupName</span></span>
<span data-ttu-id="2c89b-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2c89b-134">Name of resource group.</span></span>

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

### <span data-ttu-id="2c89b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c89b-135">-WhatIf</span></span>
<span data-ttu-id="2c89b-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c89b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c89b-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2c89b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c89b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c89b-138">CommonParameters</span></span>
<span data-ttu-id="2c89b-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c89b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c89b-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c89b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c89b-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c89b-141">INPUTS</span></span>

### <span data-ttu-id="2c89b-142">Microsoft. Azure. Commands. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="2c89b-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="2c89b-143">Microsoft. Azure. Commands. CosmosDB. models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="2c89b-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="2c89b-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c89b-144">OUTPUTS</span></span>

### <span data-ttu-id="2c89b-145">Microsoft. Azure. Commands. CosmosDB. models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="2c89b-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="2c89b-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="2c89b-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="2c89b-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c89b-147">NOTES</span></span>

## <span data-ttu-id="2c89b-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c89b-148">RELATED LINKS</span></span>
