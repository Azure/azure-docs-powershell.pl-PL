---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: b990a386feebe8e04ba612c45550ecbd07524c7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203415"
---
# <span data-ttu-id="efc05-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="efc05-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="efc05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efc05-102">SYNOPSIS</span></span>
<span data-ttu-id="efc05-103">Tworzenie obiektu PSDiagnosticDetailSetting, typ może być metryka lub dziennik</span><span class="sxs-lookup"><span data-stu-id="efc05-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="efc05-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="efc05-104">SYNTAX</span></span>

### <span data-ttu-id="efc05-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="efc05-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efc05-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="efc05-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efc05-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="efc05-107">DESCRIPTION</span></span>
<span data-ttu-id="efc05-108">Tworzenie obiektu PSMetricSettings lub PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="efc05-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="efc05-109">Kategorie można uzyskać przy `Get-AzDiagnosticSettingCategory` użyciu.</span><span class="sxs-lookup"><span data-stu-id="efc05-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="efc05-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="efc05-110">EXAMPLES</span></span>

### <span data-ttu-id="efc05-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="efc05-111">Example 1</span></span>
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

<span data-ttu-id="efc05-112">Tworzenie obiektu PSMetricSettings.</span><span class="sxs-lookup"><span data-stu-id="efc05-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="efc05-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="efc05-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="efc05-114">Tworzenie obiektu PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="efc05-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="efc05-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efc05-115">PARAMETERS</span></span>

### <span data-ttu-id="efc05-116">— Kategoria</span><span class="sxs-lookup"><span data-stu-id="efc05-116">-Category</span></span>
<span data-ttu-id="efc05-117">Kategoria ustawień</span><span class="sxs-lookup"><span data-stu-id="efc05-117">Category of setting</span></span>

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

### <span data-ttu-id="efc05-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc05-118">-DefaultProfile</span></span>
<span data-ttu-id="efc05-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="efc05-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efc05-120">— włączone</span><span class="sxs-lookup"><span data-stu-id="efc05-120">-Enabled</span></span>
<span data-ttu-id="efc05-121">Włączanie ustawienia</span><span class="sxs-lookup"><span data-stu-id="efc05-121">Enable the setting</span></span>

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

### <span data-ttu-id="efc05-122">—Log</span><span class="sxs-lookup"><span data-stu-id="efc05-122">-Log</span></span>
<span data-ttu-id="efc05-123">Aby utworzyć ustawienie dziennika</span><span class="sxs-lookup"><span data-stu-id="efc05-123">To create log setting</span></span>

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

### <span data-ttu-id="efc05-124">— Metryka</span><span class="sxs-lookup"><span data-stu-id="efc05-124">-Metric</span></span>
<span data-ttu-id="efc05-125">Aby utworzyć ustawienie metryczne</span><span class="sxs-lookup"><span data-stu-id="efc05-125">To create metric setting</span></span>

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

### <span data-ttu-id="efc05-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="efc05-126">-RetentionEnabled</span></span>
<span data-ttu-id="efc05-127">Włącz zasady przechowywania</span><span class="sxs-lookup"><span data-stu-id="efc05-127">Enable Retention policy</span></span>

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

### <span data-ttu-id="efc05-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="efc05-128">-RetentionInDays</span></span>
<span data-ttu-id="efc05-129">Dni przechowywania zasad przechowywania</span><span class="sxs-lookup"><span data-stu-id="efc05-129">Retention days for retention policy</span></span>

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

### <span data-ttu-id="efc05-130">- TimeGrain</span><span class="sxs-lookup"><span data-stu-id="efc05-130">-TimeGrain</span></span>
<span data-ttu-id="efc05-131">TimeGrain for metric setting</span><span class="sxs-lookup"><span data-stu-id="efc05-131">TimeGrain for metric setting</span></span>

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

### <span data-ttu-id="efc05-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc05-132">CommonParameters</span></span>
<span data-ttu-id="efc05-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc05-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc05-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efc05-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc05-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efc05-135">INPUTS</span></span>

### <span data-ttu-id="efc05-136">System.String</span><span class="sxs-lookup"><span data-stu-id="efc05-136">System.String</span></span>

## <span data-ttu-id="efc05-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="efc05-137">OUTPUTS</span></span>

### <span data-ttu-id="efc05-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDianossticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="efc05-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="efc05-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="efc05-139">NOTES</span></span>

## <span data-ttu-id="efc05-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efc05-140">RELATED LINKS</span></span>
