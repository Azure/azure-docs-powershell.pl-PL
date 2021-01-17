---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
ms.openlocfilehash: 8fa796b9b8940662c091e160cea55235816a29d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350866"
---
# <span data-ttu-id="1d91b-101">New-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="1d91b-101">New-AzDiagnosticSetting</span></span>

## <span data-ttu-id="1d91b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d91b-102">SYNOPSIS</span></span>
<span data-ttu-id="1d91b-103">Utwórz obiekt PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="1d91b-103">Create PSServiceDiagnosticSettings object.</span></span>

## <span data-ttu-id="1d91b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d91b-104">SYNTAX</span></span>

```
New-AzDiagnosticSetting -TargetResourceId <String> -Name <String> [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-WorkspaceId <String>] [-DedicatedLogAnalyticsDestinationType] [-Setting <PSDiagnosticDetailSettings[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d91b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d91b-105">DESCRIPTION</span></span>
<span data-ttu-id="1d91b-106">Utwórz obiekt PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="1d91b-106">Create PSServiceDiagnosticSettings object.</span></span>
<span data-ttu-id="1d91b-107">Może służyć jako parametr `-InputObject` dla `Set-AzDiagnosticSetting`</span><span class="sxs-lookup"><span data-stu-id="1d91b-107">This can be used as parameter `-InputObject` for `Set-AzDiagnosticSetting`</span></span>

## <span data-ttu-id="1d91b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d91b-108">EXAMPLES</span></span>

### <span data-ttu-id="1d91b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1d91b-109">Example 1</span></span>
```powershell
$TimeGrain=New-TimeSpan -Days 90
$metric = New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics
$log = New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
$setting = New-AzDiagnosticSetting -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX -Name diagnostic-test -WorkspaceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX -DedicatedLogAnalyticsDestinationType -Setting $log,$metric
Location                    :
Tags                        :
Id                          : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/diagnosticSettings/diagnostic-test
Name                        : diagnostic-test
StorageAccountId            :
ServiceBusRuleId            :
EventHubAuthorizationRuleId :
EventHubName                :
Metrics
    TimeGrain       :
    Category        : AllMetrics
    Enabled         : False
    RetentionPolicy
    Enabled : True
    Days    : 1


Logs
    Category        : Audit
    Enabled         : True
    RetentionPolicy
    Enabled : True
    Days    : 1


WorkspaceId                 : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX
LogAnalyticsDestinationType : Dedicated
Type                        :

Set-AzDiagnosticSetting -InputObject $setting
```

<span data-ttu-id="1d91b-110">Utwórz obiekt PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="1d91b-110">Create PSServiceDiagnosticSettings object.</span></span> <span data-ttu-id="1d91b-111">I Utwórz ustawienia diagnostyczne dla zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="1d91b-111">And create diagnostic setting for target resource.</span></span>

## <span data-ttu-id="1d91b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d91b-112">PARAMETERS</span></span>

### <span data-ttu-id="1d91b-113">-DedicatedLogAnalyticsDestinationType</span><span class="sxs-lookup"><span data-stu-id="1d91b-113">-DedicatedLogAnalyticsDestinationType</span></span>
<span data-ttu-id="1d91b-114">Wartość wskazująca, czy wyeksportować (do ODS) do specyficznych dla zasobów (jeśli istnieje) lub do AzureDiagnostics (domyślnie nie jest to obecne)</span><span class="sxs-lookup"><span data-stu-id="1d91b-114">The value indicating whether to export (to ODS) to resource-specific (if present) or to AzureDiagnostics (default, not present)</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d91b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d91b-115">-DefaultProfile</span></span>
<span data-ttu-id="1d91b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d91b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d91b-117">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="1d91b-117">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="1d91b-118">Identyfikator reguły centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="1d91b-118">The event hub rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d91b-119">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="1d91b-119">-EventHubName</span></span>
<span data-ttu-id="1d91b-120">Identyfikator reguły usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="1d91b-120">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d91b-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d91b-121">-Name</span></span>
<span data-ttu-id="1d91b-122">Nazwa ustawienia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="1d91b-122">The name of the diagnostic setting.</span></span>
<span data-ttu-id="1d91b-123">Wartość domyślna "usługa"</span><span class="sxs-lookup"><span data-stu-id="1d91b-123">Defaults to 'service'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d91b-124">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="1d91b-124">-ServiceBusRuleId</span></span>
<span data-ttu-id="1d91b-125">Identyfikator reguły usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="1d91b-125">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d91b-126">-Setting</span><span class="sxs-lookup"><span data-stu-id="1d91b-126">-Setting</span></span>
<span data-ttu-id="1d91b-127">Ustawienia metryki lub ustawienia dziennika</span><span class="sxs-lookup"><span data-stu-id="1d91b-127">Metric settings or Log settings</span></span>

```yaml
Type: PSDiagnosticDetailSettings[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d91b-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1d91b-128">-StorageAccountId</span></span>
<span data-ttu-id="1d91b-129">Identyfikator konta magazynu</span><span class="sxs-lookup"><span data-stu-id="1d91b-129">The storage account id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d91b-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="1d91b-130">-TargetResourceId</span></span>
<span data-ttu-id="1d91b-131">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="1d91b-131">The resource id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d91b-132">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="1d91b-132">-WorkspaceId</span></span>
<span data-ttu-id="1d91b-133">Identyfikator zasobu obszaru roboczego Analiza dzienników, do którego mają być wysyłane dzienniki/metryki</span><span class="sxs-lookup"><span data-stu-id="1d91b-133">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d91b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d91b-134">CommonParameters</span></span>
<span data-ttu-id="1d91b-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d91b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d91b-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d91b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d91b-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d91b-137">INPUTS</span></span>

### <span data-ttu-id="1d91b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1d91b-138">System.String</span></span>

### <span data-ttu-id="1d91b-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1d91b-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1d91b-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings []</span><span class="sxs-lookup"><span data-stu-id="1d91b-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span></span>

## <span data-ttu-id="1d91b-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d91b-141">OUTPUTS</span></span>

### <span data-ttu-id="1d91b-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="1d91b-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="1d91b-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d91b-143">NOTES</span></span>

## <span data-ttu-id="1d91b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d91b-144">RELATED LINKS</span></span>
