---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372920"
---
# <span data-ttu-id="df7f5-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="df7f5-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="df7f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df7f5-102">SYNOPSIS</span></span>
<span data-ttu-id="df7f5-103">Aktualizuje CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="df7f5-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="df7f5-104">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejące StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="df7f5-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="df7f5-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df7f5-105">SYNTAX</span></span>

### <span data-ttu-id="df7f5-106">ByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df7f5-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df7f5-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df7f5-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df7f5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df7f5-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df7f5-109">Opis</span><span class="sxs-lookup"><span data-stu-id="df7f5-109">DESCRIPTION</span></span>
<span data-ttu-id="df7f5-110">Aktualizuje CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="df7f5-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="df7f5-111">Wykonuje operację nadania poprawki po stronie klienta, odczytując istniejące StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="df7f5-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="df7f5-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df7f5-112">EXAMPLES</span></span>

### <span data-ttu-id="df7f5-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="df7f5-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="df7f5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df7f5-114">PARAMETERS</span></span>

### <span data-ttu-id="df7f5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="df7f5-115">-AccountName</span></span>
<span data-ttu-id="df7f5-116">Nazwa konta bazy danych Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="df7f5-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="df7f5-117">-Body</span><span class="sxs-lookup"><span data-stu-id="df7f5-117">-Body</span></span>
<span data-ttu-id="df7f5-118">Treść procedury składowanej.</span><span class="sxs-lookup"><span data-stu-id="df7f5-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="df7f5-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df7f5-119">-Confirm</span></span>
<span data-ttu-id="df7f5-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df7f5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df7f5-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="df7f5-121">-ContainerName</span></span>
<span data-ttu-id="df7f5-122">Nazwa kontenera.</span><span class="sxs-lookup"><span data-stu-id="df7f5-122">Container name.</span></span>

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

### <span data-ttu-id="df7f5-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="df7f5-123">-DatabaseName</span></span>
<span data-ttu-id="df7f5-124">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="df7f5-124">Database name.</span></span>

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

### <span data-ttu-id="df7f5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7f5-125">-DefaultProfile</span></span>
<span data-ttu-id="df7f5-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df7f5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df7f5-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="df7f5-127">-InputObject</span></span>
<span data-ttu-id="df7f5-128">Obiekt procedury składowanej SQL</span><span class="sxs-lookup"><span data-stu-id="df7f5-128">Sql Stored Procedure Object</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df7f5-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df7f5-129">-Name</span></span>
<span data-ttu-id="df7f5-130">Nazwa zapisanego Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="df7f5-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="df7f5-131">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="df7f5-131">-ParentObject</span></span>
<span data-ttu-id="df7f5-132">Obiekt kontenera SQL.</span><span class="sxs-lookup"><span data-stu-id="df7f5-132">Sql Container object.</span></span>

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

### <span data-ttu-id="df7f5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df7f5-133">-ResourceGroupName</span></span>
<span data-ttu-id="df7f5-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df7f5-134">Name of resource group.</span></span>

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

### <span data-ttu-id="df7f5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df7f5-135">-WhatIf</span></span>
<span data-ttu-id="df7f5-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df7f5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df7f5-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="df7f5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df7f5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7f5-138">CommonParameters</span></span>
<span data-ttu-id="df7f5-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df7f5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7f5-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df7f5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7f5-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df7f5-141">INPUTS</span></span>

### <span data-ttu-id="df7f5-142">Microsoft. Azure. Commands. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="df7f5-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="df7f5-143">Microsoft. Azure. Commands. CosmosDB. models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="df7f5-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="df7f5-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df7f5-144">OUTPUTS</span></span>

### <span data-ttu-id="df7f5-145">Microsoft. Azure. Commands. CosmosDB. models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="df7f5-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="df7f5-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="df7f5-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="df7f5-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df7f5-147">NOTES</span></span>

## <span data-ttu-id="df7f5-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df7f5-148">RELATED LINKS</span></span>
