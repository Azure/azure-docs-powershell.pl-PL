---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500794"
---
# <span data-ttu-id="5ff03-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5ff03-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="5ff03-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ff03-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff03-103">Umożliwia utworzenie lub zaktualizowanie istniejącej reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5ff03-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="5ff03-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ff03-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5ff03-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ff03-105">DESCRIPTION</span></span>
<span data-ttu-id="5ff03-106">Umożliwia utworzenie lub zaktualizowanie istniejącej reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5ff03-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="5ff03-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ff03-107">EXAMPLES</span></span>

### <span data-ttu-id="5ff03-108">Przykład 1. Tworzenie reguły sieci wirtualnej dla MariaDB</span><span class="sxs-lookup"><span data-stu-id="5ff03-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="5ff03-109">To polecenie tworzy regułę sieci wirtualnej dla MariaDB.</span><span class="sxs-lookup"><span data-stu-id="5ff03-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="5ff03-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ff03-110">PARAMETERS</span></span>

### <span data-ttu-id="5ff03-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ff03-111">-AsJob</span></span>
<span data-ttu-id="5ff03-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="5ff03-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5ff03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff03-113">-DefaultProfile</span></span>
<span data-ttu-id="5ff03-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff03-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ff03-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ff03-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="5ff03-116">Tworzenie reguły zapory przed włączeniem punktu końcowego usługi VNET w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5ff03-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="5ff03-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ff03-117">-Name</span></span>
<span data-ttu-id="5ff03-118">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5ff03-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff03-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5ff03-119">-NoWait</span></span>
<span data-ttu-id="5ff03-120">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="5ff03-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5ff03-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ff03-121">-PassThru</span></span>
<span data-ttu-id="5ff03-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="5ff03-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5ff03-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ff03-123">-ResourceGroupName</span></span>
<span data-ttu-id="5ff03-124">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="5ff03-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5ff03-125">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="5ff03-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5ff03-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5ff03-126">-ServerName</span></span>
<span data-ttu-id="5ff03-127">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="5ff03-127">The name of the server.</span></span>

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

### <span data-ttu-id="5ff03-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5ff03-128">-SubnetId</span></span>
<span data-ttu-id="5ff03-129">Identyfikator zasobu ARM podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5ff03-129">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff03-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5ff03-130">-SubscriptionId</span></span>
<span data-ttu-id="5ff03-131">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff03-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff03-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ff03-132">-Confirm</span></span>
<span data-ttu-id="5ff03-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ff03-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff03-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff03-134">-WhatIf</span></span>
<span data-ttu-id="5ff03-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ff03-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ff03-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ff03-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ff03-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff03-137">CommonParameters</span></span>
<span data-ttu-id="5ff03-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ff03-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff03-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ff03-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff03-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ff03-140">INPUTS</span></span>

## <span data-ttu-id="5ff03-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ff03-141">OUTPUTS</span></span>

### <span data-ttu-id="5ff03-142">Microsoft. Azure. PowerShell. polecenia. MariaDb. models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5ff03-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="5ff03-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ff03-143">NOTES</span></span>

<span data-ttu-id="5ff03-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="5ff03-144">ALIASES</span></span>

## <span data-ttu-id="5ff03-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ff03-145">RELATED LINKS</span></span>

