---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: 5b53c9806fa541c28b7f318f464a26e9a88104e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964513"
---
# <span data-ttu-id="67320-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="67320-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="67320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67320-102">SYNOPSIS</span></span>
<span data-ttu-id="67320-103">Zwraca listę baz danych, których właścicielem jest ten klaster, a po nich został obserwowany inny klaster.</span><span class="sxs-lookup"><span data-stu-id="67320-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="67320-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67320-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="67320-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="67320-105">DESCRIPTION</span></span>
<span data-ttu-id="67320-106">Zwraca listę baz danych, których właścicielem jest ten klaster, a po nich został obserwowany inny klaster.</span><span class="sxs-lookup"><span data-stu-id="67320-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="67320-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67320-107">EXAMPLES</span></span>

### <span data-ttu-id="67320-108">Przykład 1. Lista wszystkich obserwowanych baz danych</span><span class="sxs-lookup"><span data-stu-id="67320-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="67320-109">Powyższe polecenie zawiera listę wszystkich baz danych należących do tego klastra, po których następuje kolejny klaster.</span><span class="sxs-lookup"><span data-stu-id="67320-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="67320-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67320-110">PARAMETERS</span></span>

### <span data-ttu-id="67320-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="67320-111">-ClusterName</span></span>
<span data-ttu-id="67320-112">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="67320-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="67320-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67320-113">-DefaultProfile</span></span>
<span data-ttu-id="67320-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67320-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67320-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67320-115">-ResourceGroupName</span></span>
<span data-ttu-id="67320-116">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="67320-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="67320-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67320-117">-SubscriptionId</span></span>
<span data-ttu-id="67320-118">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="67320-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="67320-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="67320-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="67320-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67320-120">-Confirm</span></span>
<span data-ttu-id="67320-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="67320-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67320-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67320-122">-WhatIf</span></span>
<span data-ttu-id="67320-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67320-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67320-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="67320-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67320-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67320-125">CommonParameters</span></span>
<span data-ttu-id="67320-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67320-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67320-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67320-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67320-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67320-128">INPUTS</span></span>

## <span data-ttu-id="67320-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67320-129">OUTPUTS</span></span>

### <span data-ttu-id="67320-130">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="67320-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="67320-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67320-131">NOTES</span></span>

<span data-ttu-id="67320-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="67320-132">ALIASES</span></span>

## <span data-ttu-id="67320-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67320-133">RELATED LINKS</span></span>

