---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/suspend-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
ms.openlocfilehash: 17c730fb65e50aeeff33e616b7be596745d67ac0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050088"
---
# <span data-ttu-id="d64fe-101">Suspend-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d64fe-101">Suspend-AzKustoCluster</span></span>

## <span data-ttu-id="d64fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d64fe-102">SYNOPSIS</span></span>
<span data-ttu-id="d64fe-103">Zawieszanie istniejącego klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="d64fe-103">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="d64fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d64fe-104">SYNTAX</span></span>

### <span data-ttu-id="d64fe-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d64fe-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d64fe-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d64fe-106">ByResourceId</span></span>
```
Suspend-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d64fe-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d64fe-107">ByInputObject</span></span>
```
Suspend-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d64fe-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d64fe-108">DESCRIPTION</span></span>
<span data-ttu-id="d64fe-109">Zawieszanie istniejącego klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="d64fe-109">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="d64fe-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d64fe-110">EXAMPLES</span></span>

### <span data-ttu-id="d64fe-111">Przykład 1-wstrzymywanie istniejącego klastra Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="d64fe-111">Example 1 - Suspend an existing Kusto cluster by name</span></span>

```
PS C:\> Suspend-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="d64fe-112">Powyższe polecenie zawiesza klaster Kusto o nazwie "mykustocluster" znaleziony w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="d64fe-112">The above command suspends the Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="d64fe-113">Przykład 2 — zawieszanie istniejącego klastra Kusto za pomocą połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="d64fe-113">Example 2 - Suspend an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Suspend-AzKustoCluster
```

<span data-ttu-id="d64fe-114">Powyższe polecenie pobiera klaster Kusto o nazwie "mykustocluster" znajdujący się w grupie zasobów "testrg" przy użyciu `Get-AzKustoCluster` polecenia cmdlet, a następnie przekazuje wynik, aby `Suspend-AzKustoCluster` go wstrzymać.</span><span class="sxs-lookup"><span data-stu-id="d64fe-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Suspend-AzKustoCluster` to suspend it.</span></span>

## <span data-ttu-id="d64fe-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d64fe-115">PARAMETERS</span></span>

### <span data-ttu-id="d64fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d64fe-116">-DefaultProfile</span></span>
<span data-ttu-id="d64fe-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d64fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d64fe-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d64fe-118">-InputObject</span></span>
<span data-ttu-id="d64fe-119">Obiekt klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="d64fe-119">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d64fe-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d64fe-120">-Name</span></span>
<span data-ttu-id="d64fe-121">Nazwa klastra, który ma zostać zawieszony.</span><span class="sxs-lookup"><span data-stu-id="d64fe-121">Name of cluster to be suspend.</span></span>

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

### <span data-ttu-id="d64fe-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d64fe-122">-PassThru</span></span>
<span data-ttu-id="d64fe-123">Zwraca, czy określony klaster został pomyślnie zawieszony, czy nie.</span><span class="sxs-lookup"><span data-stu-id="d64fe-123">Return whether the specified cluster was successfully suspended or not.</span></span>

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

### <span data-ttu-id="d64fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d64fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="d64fe-125">Nazwa grupy zasobów, pod którą klaster istnieje.</span><span class="sxs-lookup"><span data-stu-id="d64fe-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="d64fe-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d64fe-126">-ResourceId</span></span>
<span data-ttu-id="d64fe-127">Kusto identyfikator zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="d64fe-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="d64fe-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d64fe-128">-Confirm</span></span>
<span data-ttu-id="d64fe-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d64fe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d64fe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d64fe-130">-WhatIf</span></span>
<span data-ttu-id="d64fe-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d64fe-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d64fe-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d64fe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d64fe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64fe-133">CommonParameters</span></span>
<span data-ttu-id="d64fe-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d64fe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64fe-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d64fe-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64fe-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d64fe-136">INPUTS</span></span>

### <span data-ttu-id="d64fe-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d64fe-137">System.String</span></span>

### <span data-ttu-id="d64fe-138">Microsoft. Azure. Commands. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d64fe-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="d64fe-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d64fe-139">OUTPUTS</span></span>

### <span data-ttu-id="d64fe-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d64fe-140">System.Boolean</span></span>

## <span data-ttu-id="d64fe-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d64fe-141">NOTES</span></span>

## <span data-ttu-id="d64fe-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d64fe-142">RELATED LINKS</span></span>
