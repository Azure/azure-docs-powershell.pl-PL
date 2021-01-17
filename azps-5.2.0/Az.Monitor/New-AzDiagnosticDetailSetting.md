---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: b990a386feebe8e04ba612c45550ecbd07524c7a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350869"
---
# <span data-ttu-id="7a13a-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="7a13a-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="7a13a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a13a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a13a-103">Tworzenie obiektu PSDiagnosticDetailSetting, typ może być metryką lub dziennikiem</span><span class="sxs-lookup"><span data-stu-id="7a13a-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="7a13a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a13a-104">SYNTAX</span></span>

### <span data-ttu-id="7a13a-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a13a-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a13a-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a13a-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a13a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7a13a-107">DESCRIPTION</span></span>
<span data-ttu-id="7a13a-108">Utwórz obiekt PSMetricSettings lub PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="7a13a-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="7a13a-109">Kategorie można uzyskiwać za pomocą funkcji `Get-AzDiagnosticSettingCategory` .</span><span class="sxs-lookup"><span data-stu-id="7a13a-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="7a13a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a13a-110">EXAMPLES</span></span>

### <span data-ttu-id="7a13a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7a13a-111">Example 1</span></span>
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

<span data-ttu-id="7a13a-112">Utwórz obiekt PSMetricSettings.</span><span class="sxs-lookup"><span data-stu-id="7a13a-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="7a13a-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7a13a-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="7a13a-114">Utwórz obiekt PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="7a13a-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="7a13a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a13a-115">PARAMETERS</span></span>

### <span data-ttu-id="7a13a-116">-Category</span><span class="sxs-lookup"><span data-stu-id="7a13a-116">-Category</span></span>
<span data-ttu-id="7a13a-117">Kategoria ustawienia</span><span class="sxs-lookup"><span data-stu-id="7a13a-117">Category of setting</span></span>

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

### <span data-ttu-id="7a13a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a13a-118">-DefaultProfile</span></span>
<span data-ttu-id="7a13a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a13a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a13a-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="7a13a-120">-Enabled</span></span>
<span data-ttu-id="7a13a-121">Włączanie ustawienia</span><span class="sxs-lookup"><span data-stu-id="7a13a-121">Enable the setting</span></span>

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

### <span data-ttu-id="7a13a-122">-Log</span><span class="sxs-lookup"><span data-stu-id="7a13a-122">-Log</span></span>
<span data-ttu-id="7a13a-123">Aby utworzyć ustawienia dziennika</span><span class="sxs-lookup"><span data-stu-id="7a13a-123">To create log setting</span></span>

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

### <span data-ttu-id="7a13a-124">-Metric</span><span class="sxs-lookup"><span data-stu-id="7a13a-124">-Metric</span></span>
<span data-ttu-id="7a13a-125">Aby utworzyć ustawienie metryki</span><span class="sxs-lookup"><span data-stu-id="7a13a-125">To create metric setting</span></span>

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

### <span data-ttu-id="7a13a-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="7a13a-126">-RetentionEnabled</span></span>
<span data-ttu-id="7a13a-127">Włączanie zasad przechowywania</span><span class="sxs-lookup"><span data-stu-id="7a13a-127">Enable Retention policy</span></span>

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

### <span data-ttu-id="7a13a-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7a13a-128">-RetentionInDays</span></span>
<span data-ttu-id="7a13a-129">Dni przechowywania zasad przechowywania</span><span class="sxs-lookup"><span data-stu-id="7a13a-129">Retention days for retention policy</span></span>

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

### <span data-ttu-id="7a13a-130">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="7a13a-130">-TimeGrain</span></span>
<span data-ttu-id="7a13a-131">TimeGrain dla ustawienia metryki</span><span class="sxs-lookup"><span data-stu-id="7a13a-131">TimeGrain for metric setting</span></span>

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

### <span data-ttu-id="7a13a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a13a-132">CommonParameters</span></span>
<span data-ttu-id="7a13a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a13a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a13a-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a13a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a13a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a13a-135">INPUTS</span></span>

### <span data-ttu-id="7a13a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7a13a-136">System.String</span></span>

## <span data-ttu-id="7a13a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a13a-137">OUTPUTS</span></span>

### <span data-ttu-id="7a13a-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="7a13a-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="7a13a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a13a-139">NOTES</span></span>

## <span data-ttu-id="7a13a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a13a-140">RELATED LINKS</span></span>
