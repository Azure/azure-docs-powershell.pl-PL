---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 8ad074cf40074032fbab46cab6ee6c6c290eb2ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185275"
---
# <span data-ttu-id="4e606-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="4e606-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="4e606-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e606-102">SYNOPSIS</span></span>
<span data-ttu-id="4e606-103">Zwraca listę rozszerzeń językowych, które mogą być uruchamiane w zapytaniach KQL.</span><span class="sxs-lookup"><span data-stu-id="4e606-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="4e606-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4e606-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e606-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4e606-105">DESCRIPTION</span></span>
<span data-ttu-id="4e606-106">Zwraca listę rozszerzeń językowych, które mogą być uruchamiane w zapytaniach KQL.</span><span class="sxs-lookup"><span data-stu-id="4e606-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="4e606-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4e606-107">EXAMPLES</span></span>

### <span data-ttu-id="4e606-108">Przykład 1. Lista wszystkich rozszerzeń językowych ustawionych dla klastrów</span><span class="sxs-lookup"><span data-stu-id="4e606-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="4e606-109">Powyższe polecenie zwraca listę rozszerzeń językowych, które można uruchamiać w zapytaniach KQL.</span><span class="sxs-lookup"><span data-stu-id="4e606-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="4e606-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e606-110">PARAMETERS</span></span>

### <span data-ttu-id="4e606-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4e606-111">-ClusterName</span></span>
<span data-ttu-id="4e606-112">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e606-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4e606-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e606-113">-DefaultProfile</span></span>
<span data-ttu-id="4e606-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e606-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e606-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e606-115">-ResourceGroupName</span></span>
<span data-ttu-id="4e606-116">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e606-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4e606-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e606-117">-SubscriptionId</span></span>
<span data-ttu-id="4e606-118">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4e606-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4e606-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="4e606-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4e606-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4e606-120">-Confirm</span></span>
<span data-ttu-id="4e606-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4e606-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e606-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e606-122">-WhatIf</span></span>
<span data-ttu-id="4e606-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e606-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e606-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4e606-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e606-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e606-125">CommonParameters</span></span>
<span data-ttu-id="4e606-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e606-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e606-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e606-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e606-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e606-128">INPUTS</span></span>

## <span data-ttu-id="4e606-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e606-129">OUTPUTS</span></span>

### <span data-ttu-id="4e606-130">Microsoft.Azure.PowerShell.cmdlet.Kusto.Models.Api20200918.ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="4e606-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension</span></span>

## <span data-ttu-id="4e606-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4e606-131">NOTES</span></span>

<span data-ttu-id="4e606-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4e606-132">ALIASES</span></span>

## <span data-ttu-id="4e606-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e606-133">RELATED LINKS</span></span>

