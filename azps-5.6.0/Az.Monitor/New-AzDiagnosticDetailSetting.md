---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: cccc773adf4b70f0dcef077ea436963c0af9f190
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984544"
---
# <span data-ttu-id="bf0b2-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="bf0b2-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="bf0b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0b2-103">Tworzenie obiektu PSDiagnosticDetailSetting, typ może być metryka lub dziennik</span><span class="sxs-lookup"><span data-stu-id="bf0b2-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="bf0b2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bf0b2-104">SYNTAX</span></span>

### <span data-ttu-id="bf0b2-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf0b2-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf0b2-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf0b2-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf0b2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bf0b2-107">DESCRIPTION</span></span>
<span data-ttu-id="bf0b2-108">Tworzenie obiektu PSMetricSettings lub PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="bf0b2-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="bf0b2-109">Kategorie można uzyskać przy `Get-AzDiagnosticSettingCategory` użyciu.</span><span class="sxs-lookup"><span data-stu-id="bf0b2-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="bf0b2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bf0b2-110">EXAMPLES</span></span>

### <span data-ttu-id="bf0b2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bf0b2-111">Example 1</span></span>
```powershell
PS C:\> $TimeGrain=New-TimeSpan -Days 90
PS C:\> New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics -Enabled -TimeGrain $TimeGrain
TimeGrain       : 90.00:00:00
Category        : AllMetrics
Enabled         : True
RetentionPolicy :
                  Enabled : True
                  Days    : 1
CategoryType    : Metrics
```

<span data-ttu-id="bf0b2-112">Tworzenie obiektu PSMetricSettings.</span><span class="sxs-lookup"><span data-stu-id="bf0b2-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="bf0b2-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bf0b2-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="bf0b2-114">Tworzenie obiektu PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="bf0b2-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="bf0b2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf0b2-115">PARAMETERS</span></span>

### <span data-ttu-id="bf0b2-116">— Kategoria</span><span class="sxs-lookup"><span data-stu-id="bf0b2-116">-Category</span></span>
<span data-ttu-id="bf0b2-117">Kategoria ustawień</span><span class="sxs-lookup"><span data-stu-id="bf0b2-117">Category of setting</span></span>

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

### <span data-ttu-id="bf0b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0b2-118">-DefaultProfile</span></span>
<span data-ttu-id="bf0b2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf0b2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf0b2-120">— włączone</span><span class="sxs-lookup"><span data-stu-id="bf0b2-120">-Enabled</span></span>
<span data-ttu-id="bf0b2-121">Włączanie ustawienia</span><span class="sxs-lookup"><span data-stu-id="bf0b2-121">Enable the setting</span></span>

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

### <span data-ttu-id="bf0b2-122">—Log</span><span class="sxs-lookup"><span data-stu-id="bf0b2-122">-Log</span></span>
<span data-ttu-id="bf0b2-123">Aby utworzyć ustawienie dziennika</span><span class="sxs-lookup"><span data-stu-id="bf0b2-123">To create log setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0b2-124">— Metryka</span><span class="sxs-lookup"><span data-stu-id="bf0b2-124">-Metric</span></span>
<span data-ttu-id="bf0b2-125">Aby utworzyć ustawienie metryczne</span><span class="sxs-lookup"><span data-stu-id="bf0b2-125">To create metric setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0b2-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="bf0b2-126">-RetentionEnabled</span></span>
<span data-ttu-id="bf0b2-127">Włącz zasady przechowywania</span><span class="sxs-lookup"><span data-stu-id="bf0b2-127">Enable Retention policy</span></span>

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

### <span data-ttu-id="bf0b2-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="bf0b2-128">-RetentionInDays</span></span>
<span data-ttu-id="bf0b2-129">Dni przechowywania zasad przechowywania</span><span class="sxs-lookup"><span data-stu-id="bf0b2-129">Retention days for retention policy</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0b2-130">- TimeGrain</span><span class="sxs-lookup"><span data-stu-id="bf0b2-130">-TimeGrain</span></span>
<span data-ttu-id="bf0b2-131">TimeGrain for metric setting</span><span class="sxs-lookup"><span data-stu-id="bf0b2-131">TimeGrain for metric setting</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0b2-132">CommonParameters</span></span>
<span data-ttu-id="bf0b2-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf0b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0b2-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf0b2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0b2-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf0b2-135">INPUTS</span></span>

### <span data-ttu-id="bf0b2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bf0b2-136">System.String</span></span>

## <span data-ttu-id="bf0b2-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf0b2-137">OUTPUTS</span></span>

### <span data-ttu-id="bf0b2-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDianossticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="bf0b2-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="bf0b2-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bf0b2-139">NOTES</span></span>

## <span data-ttu-id="bf0b2-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf0b2-140">RELATED LINKS</span></span>
