---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: 141c601b5a903462b15bbeb45d410db24608323f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867803"
---
# <span data-ttu-id="5afb8-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="5afb8-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="5afb8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5afb8-102">SYNOPSIS</span></span>
<span data-ttu-id="5afb8-103">Usuwa istniejącą bazę danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="5afb8-103">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="5afb8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5afb8-104">SYNTAX</span></span>

### <span data-ttu-id="5afb8-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5afb8-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5afb8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5afb8-106">ByResourceId</span></span>
```
Remove-AzKustoDatabase [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5afb8-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5afb8-107">ByInputObject</span></span>
```
Remove-AzKustoDatabase [-InputObject] <PSKustoDatabase> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5afb8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5afb8-108">DESCRIPTION</span></span>
<span data-ttu-id="5afb8-109">Usuwa istniejącą bazę danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="5afb8-109">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="5afb8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5afb8-110">EXAMPLES</span></span>

### <span data-ttu-id="5afb8-111">Przykład 1-Usuwanie istniejącej bazy danych Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="5afb8-111">Example 1 - Delete an existing Kusto database by name</span></span>

```
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase
```

<span data-ttu-id="5afb8-112">Powyższe polecenie usunie Kusto bazę danych o nazwie "mykustodatabase" w klastrze "mykustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="5afb8-112">The above command deletes the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="5afb8-113">Przykład 2 — Usuwanie istniejącej bazy danych Kusto przez potok</span><span class="sxs-lookup"><span data-stu-id="5afb8-113">Example 2 - Delete an existing Kusto database by piping</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Remove-AzKustoDatabase
```

<span data-ttu-id="5afb8-114">Powyższe polecenie pobiera bazę danych Kusto o nazwie "mykustodatabase" w klastrze "mykustocluster" w grupie zasobów "testrg" przy użyciu `Get-AzKustoDatabase` polecenia cmdlet, a następnie przekazuje wynik, aby `Remove-AzKustoDatabase` go usunąć.</span><span class="sxs-lookup"><span data-stu-id="5afb8-114">The above command gets the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Remove-AzKustoDatabase` to delete it.</span></span>

## <span data-ttu-id="5afb8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5afb8-115">PARAMETERS</span></span>

### <span data-ttu-id="5afb8-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="5afb8-116">-ClusterName</span></span>
<span data-ttu-id="5afb8-117">Nazwa klastra, w którym istnieje baza danych.</span><span class="sxs-lookup"><span data-stu-id="5afb8-117">Name of the cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5afb8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5afb8-118">-DefaultProfile</span></span>
<span data-ttu-id="5afb8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5afb8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5afb8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5afb8-120">-InputObject</span></span>
<span data-ttu-id="5afb8-121">Obiekt bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="5afb8-121">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5afb8-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5afb8-122">-Name</span></span>
<span data-ttu-id="5afb8-123">Nazwa bazy danych, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="5afb8-123">Name of database to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5afb8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5afb8-124">-PassThru</span></span>
<span data-ttu-id="5afb8-125">Zwraca, czy pomyślnie wstrzymano określoną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="5afb8-125">Return whether the specified database was successfully suspended or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5afb8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5afb8-126">-ResourceGroupName</span></span>
<span data-ttu-id="5afb8-127">Nazwa grupy zasobów, pod którą klaster istnieje.</span><span class="sxs-lookup"><span data-stu-id="5afb8-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5afb8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5afb8-128">-ResourceId</span></span>
<span data-ttu-id="5afb8-129">Identyfikator zasobu bazy danych Kusto.</span><span class="sxs-lookup"><span data-stu-id="5afb8-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5afb8-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5afb8-130">-Confirm</span></span>
<span data-ttu-id="5afb8-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5afb8-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5afb8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5afb8-132">-WhatIf</span></span>
<span data-ttu-id="5afb8-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5afb8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5afb8-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5afb8-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5afb8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5afb8-135">CommonParameters</span></span>
<span data-ttu-id="5afb8-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5afb8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5afb8-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5afb8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5afb8-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5afb8-138">INPUTS</span></span>

### <span data-ttu-id="5afb8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5afb8-139">System.String</span></span>

### <span data-ttu-id="5afb8-140">Microsoft. Azure. Commands. Kusto. models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="5afb8-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="5afb8-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5afb8-141">OUTPUTS</span></span>

### <span data-ttu-id="5afb8-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5afb8-142">System.Boolean</span></span>

## <span data-ttu-id="5afb8-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5afb8-143">NOTES</span></span>

## <span data-ttu-id="5afb8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5afb8-144">RELATED LINKS</span></span>
