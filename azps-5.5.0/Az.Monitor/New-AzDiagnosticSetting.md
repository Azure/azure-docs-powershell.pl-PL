---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
ms.openlocfilehash: 8fa796b9b8940662c091e160cea55235816a29d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180147"
---
# <span data-ttu-id="07ec9-101">New-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="07ec9-101">New-AzDiagnosticSetting</span></span>

## <span data-ttu-id="07ec9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="07ec9-103">Tworzenie obiektu PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="07ec9-103">Create PSServiceDiagnosticSettings object.</span></span>

## <span data-ttu-id="07ec9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="07ec9-104">SYNTAX</span></span>

```
New-AzDiagnosticSetting -TargetResourceId <String> -Name <String> [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-WorkspaceId <String>] [-DedicatedLogAnalyticsDestinationType] [-Setting <PSDiagnosticDetailSettings[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07ec9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="07ec9-105">DESCRIPTION</span></span>
<span data-ttu-id="07ec9-106">Tworzenie obiektu PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="07ec9-106">Create PSServiceDiagnosticSettings object.</span></span>
<span data-ttu-id="07ec9-107">Ten parametr może być używany jako parametr dla `-InputObject``Set-AzDiagnosticSetting`</span><span class="sxs-lookup"><span data-stu-id="07ec9-107">This can be used as parameter `-InputObject` for `Set-AzDiagnosticSetting`</span></span>

## <span data-ttu-id="07ec9-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="07ec9-108">EXAMPLES</span></span>

### <span data-ttu-id="07ec9-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="07ec9-109">Example 1</span></span>
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

<span data-ttu-id="07ec9-110">Tworzenie obiektu PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="07ec9-110">Create PSServiceDiagnosticSettings object.</span></span> <span data-ttu-id="07ec9-111">Następnie utwórz ustawienie diagnostyczne dla zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="07ec9-111">And create diagnostic setting for target resource.</span></span>

## <span data-ttu-id="07ec9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07ec9-112">PARAMETERS</span></span>

### <span data-ttu-id="07ec9-113">-DedicatedLogAnalyticsDestinationType</span><span class="sxs-lookup"><span data-stu-id="07ec9-113">-DedicatedLogAnalyticsDestinationType</span></span>
<span data-ttu-id="07ec9-114">Wartość wskazująca, czy eksportować (do ods) do określonego zasobu (jeśli występuje), czy do narzędzia AzureDiagnostics (domyślnie nie występuje)</span><span class="sxs-lookup"><span data-stu-id="07ec9-114">The value indicating whether to export (to ODS) to resource-specific (if present) or to AzureDiagnostics (default, not present)</span></span>

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

### <span data-ttu-id="07ec9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ec9-115">-DefaultProfile</span></span>
<span data-ttu-id="07ec9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="07ec9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07ec9-117">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="07ec9-117">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="07ec9-118">Identyfikator reguły centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="07ec9-118">The event hub rule id</span></span>

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

### <span data-ttu-id="07ec9-119">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="07ec9-119">-EventHubName</span></span>
<span data-ttu-id="07ec9-120">Identyfikator reguły autobusu usługowego</span><span class="sxs-lookup"><span data-stu-id="07ec9-120">The service bus rule id</span></span>

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

### <span data-ttu-id="07ec9-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="07ec9-121">-Name</span></span>
<span data-ttu-id="07ec9-122">Nazwa ustawienia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="07ec9-122">The name of the diagnostic setting.</span></span>
<span data-ttu-id="07ec9-123">Domyślnie "usługa"</span><span class="sxs-lookup"><span data-stu-id="07ec9-123">Defaults to 'service'</span></span>

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

### <span data-ttu-id="07ec9-124">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="07ec9-124">-ServiceBusRuleId</span></span>
<span data-ttu-id="07ec9-125">Identyfikator reguły autobusu usługowego</span><span class="sxs-lookup"><span data-stu-id="07ec9-125">The service bus rule id</span></span>

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

### <span data-ttu-id="07ec9-126">— Ustawienie</span><span class="sxs-lookup"><span data-stu-id="07ec9-126">-Setting</span></span>
<span data-ttu-id="07ec9-127">Ustawienia metryczne lub ustawienia dziennika</span><span class="sxs-lookup"><span data-stu-id="07ec9-127">Metric settings or Log settings</span></span>

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

### <span data-ttu-id="07ec9-128">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="07ec9-128">-StorageAccountId</span></span>
<span data-ttu-id="07ec9-129">Identyfikator konta magazynu</span><span class="sxs-lookup"><span data-stu-id="07ec9-129">The storage account id</span></span>

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

### <span data-ttu-id="07ec9-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="07ec9-130">-TargetResourceId</span></span>
<span data-ttu-id="07ec9-131">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="07ec9-131">The resource id</span></span>

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

### <span data-ttu-id="07ec9-132">- WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="07ec9-132">-WorkspaceId</span></span>
<span data-ttu-id="07ec9-133">Identyfikator zasobu obszaru roboczego analizy dziennika w celu wysyłania dzienników/metryk do</span><span class="sxs-lookup"><span data-stu-id="07ec9-133">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

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

### <span data-ttu-id="07ec9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ec9-134">CommonParameters</span></span>
<span data-ttu-id="07ec9-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ec9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ec9-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07ec9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ec9-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07ec9-137">INPUTS</span></span>

### <span data-ttu-id="07ec9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="07ec9-138">System.String</span></span>

### <span data-ttu-id="07ec9-139">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="07ec9-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="07ec9-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDianossticDetailSettings[]</span><span class="sxs-lookup"><span data-stu-id="07ec9-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span></span>

## <span data-ttu-id="07ec9-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="07ec9-141">OUTPUTS</span></span>

### <span data-ttu-id="07ec9-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="07ec9-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="07ec9-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="07ec9-143">NOTES</span></span>

## <span data-ttu-id="07ec9-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07ec9-144">RELATED LINKS</span></span>
