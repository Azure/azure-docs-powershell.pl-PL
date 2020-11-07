---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/resume-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
ms.openlocfilehash: 6b60a4e55bb1f127a1d7da9042e29e5469162af4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867788"
---
# <span data-ttu-id="90d87-101">Resume-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="90d87-101">Resume-AzKustoCluster</span></span>

## <span data-ttu-id="90d87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90d87-102">SYNOPSIS</span></span>
<span data-ttu-id="90d87-103">Wznów działanie klastra programu suspeneded Kusto.</span><span class="sxs-lookup"><span data-stu-id="90d87-103">Resume a suspeneded Kusto cluster.</span></span>

## <span data-ttu-id="90d87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90d87-104">SYNTAX</span></span>

### <span data-ttu-id="90d87-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="90d87-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzKustoCluster [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90d87-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="90d87-106">ByResourceId</span></span>
```
Resume-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90d87-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="90d87-107">ByInputObject</span></span>
```
Resume-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90d87-108">Opis</span><span class="sxs-lookup"><span data-stu-id="90d87-108">DESCRIPTION</span></span>
<span data-ttu-id="90d87-109">Wznów działanie klastra programu suspeneded Kusto.</span><span class="sxs-lookup"><span data-stu-id="90d87-109">Resume a suspeneded Kusto cluster.</span></span>

## <span data-ttu-id="90d87-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90d87-110">EXAMPLES</span></span>

### <span data-ttu-id="90d87-111">Przykład 1-Wznów zawieszony klaster Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="90d87-111">Example 1 - Resume a suspended Kusto cluster by name</span></span>

```
PS C:\> Resume-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="90d87-112">Powyższe polecenie wznowienie zawieszonego klastra Kusto o nazwie "mykustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="90d87-112">The above command resumes the suspended Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="90d87-113">Przykład 2-wznowienie zawieszonego klastra Kusto przez rurociąg</span><span class="sxs-lookup"><span data-stu-id="90d87-113">Example 2 - Resume a suspended Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Resume-AzKustoCluster
```

<span data-ttu-id="90d87-114">Powyższe polecenie pobiera klaster Kusto o nazwie "mykustocluster" znajdujący się w grupie zasobów "testrg" przy użyciu `Get-AzKustoCluster` polecenia cmdlet, a następnie przekazuje wynik, aby `Resume-AzKustoCluster` wznowić działanie.</span><span class="sxs-lookup"><span data-stu-id="90d87-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Resume-AzKustoCluster` to resume it.</span></span>

## <span data-ttu-id="90d87-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90d87-115">PARAMETERS</span></span>

### <span data-ttu-id="90d87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d87-116">-DefaultProfile</span></span>
<span data-ttu-id="90d87-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90d87-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90d87-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="90d87-118">-InputObject</span></span>
<span data-ttu-id="90d87-119">Obiekt klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="90d87-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="90d87-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90d87-120">-Name</span></span>
<span data-ttu-id="90d87-121">Nazwa klastra do wznowienia.</span><span class="sxs-lookup"><span data-stu-id="90d87-121">Name of cluster to be resume.</span></span>

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

### <span data-ttu-id="90d87-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90d87-122">-PassThru</span></span>
<span data-ttu-id="90d87-123">Zwraca, czy określony klaster został pomyślnie wznowiony.</span><span class="sxs-lookup"><span data-stu-id="90d87-123">Return whether the specified cluster was successfully resumed or not.</span></span>

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

### <span data-ttu-id="90d87-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90d87-124">-ResourceGroupName</span></span>
<span data-ttu-id="90d87-125">Nazwa grupy zasobów, pod którą klaster istnieje.</span><span class="sxs-lookup"><span data-stu-id="90d87-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d87-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90d87-126">-ResourceId</span></span>
<span data-ttu-id="90d87-127">Kusto identyfikator zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="90d87-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="90d87-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90d87-128">-Confirm</span></span>
<span data-ttu-id="90d87-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90d87-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90d87-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90d87-130">-WhatIf</span></span>
<span data-ttu-id="90d87-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90d87-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90d87-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="90d87-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90d87-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d87-133">CommonParameters</span></span>
<span data-ttu-id="90d87-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90d87-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d87-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90d87-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d87-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90d87-136">INPUTS</span></span>

### <span data-ttu-id="90d87-137">System. String</span><span class="sxs-lookup"><span data-stu-id="90d87-137">System.String</span></span>

### <span data-ttu-id="90d87-138">Microsoft. Azure. Commands. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="90d87-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="90d87-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90d87-139">OUTPUTS</span></span>

### <span data-ttu-id="90d87-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90d87-140">System.Boolean</span></span>

## <span data-ttu-id="90d87-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90d87-141">NOTES</span></span>

## <span data-ttu-id="90d87-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90d87-142">RELATED LINKS</span></span>
