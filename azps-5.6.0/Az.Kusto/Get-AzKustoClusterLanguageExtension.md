---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 85c69786c75ea809fa5ffaea754ae444479673dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964474"
---
# <span data-ttu-id="d3da4-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="d3da4-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="d3da4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3da4-102">SYNOPSIS</span></span>
<span data-ttu-id="d3da4-103">Zwraca listę rozszerzeń językowych, które mogą być uruchamiane w zapytaniach KQL.</span><span class="sxs-lookup"><span data-stu-id="d3da4-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="d3da4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3da4-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d3da4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3da4-105">DESCRIPTION</span></span>
<span data-ttu-id="d3da4-106">Zwraca listę rozszerzeń językowych, które mogą być uruchamiane w zapytaniach KQL.</span><span class="sxs-lookup"><span data-stu-id="d3da4-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="d3da4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3da4-107">EXAMPLES</span></span>

### <span data-ttu-id="d3da4-108">Przykład 1. Lista wszystkich rozszerzeń językowych ustawionych dla klastrów</span><span class="sxs-lookup"><span data-stu-id="d3da4-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="d3da4-109">Powyższe polecenie zwraca listę rozszerzeń językowych, które można uruchamiać w zapytaniach KQL.</span><span class="sxs-lookup"><span data-stu-id="d3da4-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="d3da4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3da4-110">PARAMETERS</span></span>

### <span data-ttu-id="d3da4-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d3da4-111">-ClusterName</span></span>
<span data-ttu-id="d3da4-112">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="d3da4-112">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3da4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3da4-113">-DefaultProfile</span></span>
<span data-ttu-id="d3da4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3da4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3da4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3da4-115">-ResourceGroupName</span></span>
<span data-ttu-id="d3da4-116">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="d3da4-116">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3da4-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3da4-117">-SubscriptionId</span></span>
<span data-ttu-id="d3da4-118">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d3da4-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d3da4-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d3da4-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3da4-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3da4-120">-Confirm</span></span>
<span data-ttu-id="d3da4-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d3da4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3da4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3da4-122">-WhatIf</span></span>
<span data-ttu-id="d3da4-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3da4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3da4-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d3da4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3da4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3da4-125">CommonParameters</span></span>
<span data-ttu-id="d3da4-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3da4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3da4-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3da4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3da4-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3da4-128">INPUTS</span></span>

## <span data-ttu-id="d3da4-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3da4-129">OUTPUTS</span></span>

### <span data-ttu-id="d3da4-130">Microsoft.Azure.PowerShell.cmdlet.Kusto.Models.Api20200918.ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="d3da4-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension</span></span>

## <span data-ttu-id="d3da4-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3da4-131">NOTES</span></span>

<span data-ttu-id="d3da4-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d3da4-132">ALIASES</span></span>

## <span data-ttu-id="d3da4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3da4-133">RELATED LINKS</span></span>

