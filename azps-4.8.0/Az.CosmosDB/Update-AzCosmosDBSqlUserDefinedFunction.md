---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223152"
---
# <span data-ttu-id="a2bca-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="a2bca-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="a2bca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2bca-102">SYNOPSIS</span></span>
<span data-ttu-id="a2bca-103">Aktualizuje CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="a2bca-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="a2bca-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejące UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="a2bca-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="a2bca-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2bca-105">SYNTAX</span></span>

### <span data-ttu-id="a2bca-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a2bca-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2bca-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2bca-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2bca-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2bca-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2bca-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a2bca-109">DESCRIPTION</span></span>
<span data-ttu-id="a2bca-110">Aktualizuje CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="a2bca-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="a2bca-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejące UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="a2bca-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="a2bca-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2bca-112">EXAMPLES</span></span>

### <span data-ttu-id="a2bca-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a2bca-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="a2bca-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2bca-114">PARAMETERS</span></span>

### <span data-ttu-id="a2bca-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a2bca-115">-AccountName</span></span>
<span data-ttu-id="a2bca-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="a2bca-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a2bca-117">-Body</span><span class="sxs-lookup"><span data-stu-id="a2bca-117">-Body</span></span>
<span data-ttu-id="a2bca-118">Treść funkcji zdefiniowanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a2bca-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="a2bca-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a2bca-119">-Confirm</span></span>
<span data-ttu-id="a2bca-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2bca-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2bca-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a2bca-121">-ContainerName</span></span>
<span data-ttu-id="a2bca-122">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="a2bca-122">Container name.</span></span>

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

### <span data-ttu-id="a2bca-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2bca-123">-DatabaseName</span></span>
<span data-ttu-id="a2bca-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a2bca-124">Database name.</span></span>

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

### <span data-ttu-id="a2bca-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2bca-125">-DefaultProfile</span></span>
<span data-ttu-id="a2bca-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2bca-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2bca-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a2bca-127">-InputObject</span></span>
<span data-ttu-id="a2bca-128">Obiekt funkcji zdefiniowanej przez użytkownika SQL</span><span class="sxs-lookup"><span data-stu-id="a2bca-128">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="a2bca-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a2bca-129">-Name</span></span>
<span data-ttu-id="a2bca-130">Nazwa funkcji zdefiniowana przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a2bca-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="a2bca-131">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="a2bca-131">-ParentObject</span></span>
<span data-ttu-id="a2bca-132">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="a2bca-132">Sql Container object.</span></span>

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

### <span data-ttu-id="a2bca-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2bca-133">-ResourceGroupName</span></span>
<span data-ttu-id="a2bca-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a2bca-134">Name of resource group.</span></span>

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

### <span data-ttu-id="a2bca-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2bca-135">-WhatIf</span></span>
<span data-ttu-id="a2bca-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2bca-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2bca-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a2bca-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2bca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2bca-138">CommonParameters</span></span>
<span data-ttu-id="a2bca-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2bca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2bca-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2bca-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2bca-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2bca-141">INPUTS</span></span>

### <span data-ttu-id="a2bca-142">Microsoft. Azure. Commands. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="a2bca-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="a2bca-143">Microsoft. Azure. Commands. CosmosDB. models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="a2bca-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="a2bca-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2bca-144">OUTPUTS</span></span>

### <span data-ttu-id="a2bca-145">Microsoft. Azure. Commands. CosmosDB. models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="a2bca-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="a2bca-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="a2bca-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="a2bca-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2bca-147">NOTES</span></span>

## <span data-ttu-id="a2bca-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2bca-148">RELATED LINKS</span></span>
