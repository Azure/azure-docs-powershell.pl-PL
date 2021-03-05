---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: a13b0a936eeecd1d7a18b18bb8878b79225da030
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013361"
---
# <span data-ttu-id="4daf6-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="4daf6-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="4daf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4daf6-102">SYNOPSIS</span></span>
<span data-ttu-id="4daf6-103">Tworzy monitor SAP dla określonej subskrypcji, grupy zasobów i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="4daf6-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="4daf6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4daf6-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4daf6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4daf6-105">DESCRIPTION</span></span>
<span data-ttu-id="4daf6-106">Tworzy monitor SAP dla określonej subskrypcji, grupy zasobów i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="4daf6-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="4daf6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4daf6-107">EXAMPLES</span></span>

### <span data-ttu-id="4daf6-108">Przykład 1. Nowy monitor SAP</span><span class="sxs-lookup"><span data-stu-id="4daf6-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="4daf6-109">To polecenie tworzy monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="4daf6-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="4daf6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4daf6-110">PARAMETERS</span></span>

### <span data-ttu-id="4daf6-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4daf6-111">-AsJob</span></span>
<span data-ttu-id="4daf6-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="4daf6-112">Run the command as a job</span></span>

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

### <span data-ttu-id="4daf6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4daf6-113">-DefaultProfile</span></span>
<span data-ttu-id="4daf6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4daf6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4daf6-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="4daf6-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="4daf6-116">Wartość wskazująca, czy wysyłać analizy do firmy Microsoft</span><span class="sxs-lookup"><span data-stu-id="4daf6-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="4daf6-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4daf6-117">-Location</span></span>
<span data-ttu-id="4daf6-118">Lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="4daf6-118">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="4daf6-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="4daf6-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="4daf6-120">Identyfikator obszaru roboczego obszaru roboczego analizy dziennika, który ma być używany do monitorowania</span><span class="sxs-lookup"><span data-stu-id="4daf6-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="4daf6-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="4daf6-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="4daf6-122">Identyfikator ARM obszaru roboczego analizy dziennika używanego do monitorowania</span><span class="sxs-lookup"><span data-stu-id="4daf6-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="4daf6-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="4daf6-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="4daf6-124">Klucz udostępniony obszaru roboczego analizy dziennika używanego do monitorowania</span><span class="sxs-lookup"><span data-stu-id="4daf6-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="4daf6-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="4daf6-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="4daf6-126">Podsieci, w której zostanie wdrożony monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="4daf6-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="4daf6-127">Powinna to być ta sama podsieci bazy danych HANA.</span><span class="sxs-lookup"><span data-stu-id="4daf6-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="4daf6-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4daf6-128">-Name</span></span>
<span data-ttu-id="4daf6-129">Nazwa zasobu monitorowego SAP.</span><span class="sxs-lookup"><span data-stu-id="4daf6-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4daf6-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4daf6-130">-NoWait</span></span>
<span data-ttu-id="4daf6-131">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="4daf6-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4daf6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4daf6-132">-ResourceGroupName</span></span>
<span data-ttu-id="4daf6-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4daf6-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="4daf6-134">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4daf6-134">-SubscriptionId</span></span>
<span data-ttu-id="4daf6-135">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4daf6-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4daf6-136">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="4daf6-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4daf6-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="4daf6-137">-Tag</span></span>
<span data-ttu-id="4daf6-138">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="4daf6-138">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4daf6-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4daf6-139">-Confirm</span></span>
<span data-ttu-id="4daf6-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4daf6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4daf6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4daf6-141">-WhatIf</span></span>
<span data-ttu-id="4daf6-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4daf6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4daf6-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4daf6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4daf6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4daf6-144">CommonParameters</span></span>
<span data-ttu-id="4daf6-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4daf6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4daf6-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4daf6-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4daf6-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4daf6-147">INPUTS</span></span>

## <span data-ttu-id="4daf6-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4daf6-148">OUTPUTS</span></span>

### <span data-ttu-id="4daf6-149">Microsoft.Azure.PowerShell.Cmdlet.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="4daf6-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="4daf6-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4daf6-150">NOTES</span></span>

<span data-ttu-id="4daf6-151">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4daf6-151">ALIASES</span></span>

## <span data-ttu-id="4daf6-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4daf6-152">RELATED LINKS</span></span>

