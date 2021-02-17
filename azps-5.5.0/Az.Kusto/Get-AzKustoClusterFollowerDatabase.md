---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: ecc811e98545816e69f7baa6fc96ea92fbeb43d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185283"
---
# <span data-ttu-id="10510-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="10510-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="10510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10510-102">SYNOPSIS</span></span>
<span data-ttu-id="10510-103">Zwraca listę baz danych, które są własnością tego klastra, a następnie są obserwowane przez inny klaster.</span><span class="sxs-lookup"><span data-stu-id="10510-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="10510-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10510-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="10510-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="10510-105">DESCRIPTION</span></span>
<span data-ttu-id="10510-106">Zwraca listę baz danych, których właścicielem jest ten klaster, a po nich został obserwowany inny klaster.</span><span class="sxs-lookup"><span data-stu-id="10510-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="10510-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10510-107">EXAMPLES</span></span>

### <span data-ttu-id="10510-108">Przykład 1. Lista wszystkich obserwowanych baz danych</span><span class="sxs-lookup"><span data-stu-id="10510-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="10510-109">Powyższe polecenie zawiera listę wszystkich baz danych należących do tego klastra, po których następuje kolejny klaster.</span><span class="sxs-lookup"><span data-stu-id="10510-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="10510-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10510-110">PARAMETERS</span></span>

### <span data-ttu-id="10510-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="10510-111">-ClusterName</span></span>
<span data-ttu-id="10510-112">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="10510-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="10510-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10510-113">-DefaultProfile</span></span>
<span data-ttu-id="10510-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10510-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10510-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10510-115">-ResourceGroupName</span></span>
<span data-ttu-id="10510-116">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="10510-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="10510-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10510-117">-SubscriptionId</span></span>
<span data-ttu-id="10510-118">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="10510-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="10510-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="10510-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="10510-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10510-120">-Confirm</span></span>
<span data-ttu-id="10510-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="10510-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10510-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10510-122">-WhatIf</span></span>
<span data-ttu-id="10510-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10510-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10510-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="10510-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10510-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10510-125">CommonParameters</span></span>
<span data-ttu-id="10510-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10510-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10510-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10510-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10510-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10510-128">INPUTS</span></span>

## <span data-ttu-id="10510-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10510-129">OUTPUTS</span></span>

### <span data-ttu-id="10510-130">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="10510-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="10510-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10510-131">NOTES</span></span>

<span data-ttu-id="10510-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="10510-132">ALIASES</span></span>

## <span data-ttu-id="10510-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10510-133">RELATED LINKS</span></span>

