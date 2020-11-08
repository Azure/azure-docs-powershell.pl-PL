---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/resume-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
ms.openlocfilehash: 94e5525b1d783eea794b7e98e76e809b9d7e0f3b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050089"
---
# <span data-ttu-id="4dd35-101">Resume-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4dd35-101">Resume-AzKustoCluster</span></span>

## <span data-ttu-id="4dd35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4dd35-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd35-103">Wznawianie zawieszonego klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="4dd35-103">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="4dd35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4dd35-104">SYNTAX</span></span>

### <span data-ttu-id="4dd35-105">ByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4dd35-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzKustoCluster [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd35-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4dd35-106">ByResourceId</span></span>
```
Resume-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd35-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4dd35-107">ByInputObject</span></span>
```
Resume-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dd35-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4dd35-108">DESCRIPTION</span></span>
<span data-ttu-id="4dd35-109">Wznawianie zawieszonego klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="4dd35-109">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="4dd35-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4dd35-110">EXAMPLES</span></span>

### <span data-ttu-id="4dd35-111">Przykład 1-Wznów zawieszony klaster Kusto według nazwy</span><span class="sxs-lookup"><span data-stu-id="4dd35-111">Example 1 - Resume a suspended Kusto cluster by name</span></span>

```
PS C:\> Resume-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="4dd35-112">Powyższe polecenie wznowienie zawieszonego klastra Kusto o nazwie "mykustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="4dd35-112">The above command resumes the suspended Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="4dd35-113">Przykład 2-wznowienie zawieszonego klastra Kusto przez rurociąg</span><span class="sxs-lookup"><span data-stu-id="4dd35-113">Example 2 - Resume a suspended Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Resume-AzKustoCluster
```

<span data-ttu-id="4dd35-114">Powyższe polecenie pobiera klaster Kusto o nazwie "mykustocluster" znajdujący się w grupie zasobów "testrg" przy użyciu `Get-AzKustoCluster` polecenia cmdlet, a następnie przekazuje wynik, aby `Resume-AzKustoCluster` wznowić działanie.</span><span class="sxs-lookup"><span data-stu-id="4dd35-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Resume-AzKustoCluster` to resume it.</span></span>

## <span data-ttu-id="4dd35-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4dd35-115">PARAMETERS</span></span>

### <span data-ttu-id="4dd35-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd35-116">-DefaultProfile</span></span>
<span data-ttu-id="4dd35-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd35-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dd35-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4dd35-118">-InputObject</span></span>
<span data-ttu-id="4dd35-119">Obiekt klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="4dd35-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="4dd35-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4dd35-120">-Name</span></span>
<span data-ttu-id="4dd35-121">Nazwa klastra do wznowienia.</span><span class="sxs-lookup"><span data-stu-id="4dd35-121">Name of cluster to be resume.</span></span>

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

### <span data-ttu-id="4dd35-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dd35-122">-PassThru</span></span>
<span data-ttu-id="4dd35-123">Zwraca, czy określony klaster został pomyślnie wznowiony.</span><span class="sxs-lookup"><span data-stu-id="4dd35-123">Return whether the specified cluster was successfully resumed or not.</span></span>

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

### <span data-ttu-id="4dd35-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd35-124">-ResourceGroupName</span></span>
<span data-ttu-id="4dd35-125">Nazwa grupy zasobów, pod którą klaster istnieje.</span><span class="sxs-lookup"><span data-stu-id="4dd35-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="4dd35-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dd35-126">-ResourceId</span></span>
<span data-ttu-id="4dd35-127">Kusto identyfikator zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="4dd35-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="4dd35-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4dd35-128">-Confirm</span></span>
<span data-ttu-id="4dd35-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dd35-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dd35-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd35-130">-WhatIf</span></span>
<span data-ttu-id="4dd35-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dd35-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dd35-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4dd35-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dd35-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd35-133">CommonParameters</span></span>
<span data-ttu-id="4dd35-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd35-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd35-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dd35-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd35-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4dd35-136">INPUTS</span></span>

### <span data-ttu-id="4dd35-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4dd35-137">System.String</span></span>

### <span data-ttu-id="4dd35-138">Microsoft. Azure. Commands. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4dd35-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="4dd35-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4dd35-139">OUTPUTS</span></span>

### <span data-ttu-id="4dd35-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4dd35-140">System.Boolean</span></span>

## <span data-ttu-id="4dd35-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4dd35-141">NOTES</span></span>

## <span data-ttu-id="4dd35-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4dd35-142">RELATED LINKS</span></span>
