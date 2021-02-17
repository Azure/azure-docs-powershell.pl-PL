---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182915"
---
# <span data-ttu-id="43cfb-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="43cfb-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="43cfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="43cfb-103">Uruchamia zadanie analizy strumieniowej.</span><span class="sxs-lookup"><span data-stu-id="43cfb-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="43cfb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="43cfb-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43cfb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="43cfb-105">DESCRIPTION</span></span>
<span data-ttu-id="43cfb-106">Polecenie **cmdlet Start-AzStreamAnalyticsJob** asynchronicznie wdraża i uruchamia zadanie analizy strumienia na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="43cfb-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="43cfb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="43cfb-107">EXAMPLES</span></span>

### <span data-ttu-id="43cfb-108">Przykład 1. Uruchamianie zadania analizy strumieniowej</span><span class="sxs-lookup"><span data-stu-id="43cfb-108">Example 1: Start a Stream Analytics job</span></span>
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="43cfb-109">To polecenie uruchamia zadanie StreamingJob i określa, że strumienie zdarzeń wyjściowych powinny rozpoczynać się w sygnaturze czasowej 2014-07-03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="43cfb-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="43cfb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43cfb-110">PARAMETERS</span></span>

### <span data-ttu-id="43cfb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43cfb-111">-DefaultProfile</span></span>
<span data-ttu-id="43cfb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="43cfb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43cfb-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="43cfb-113">-Name</span></span>
<span data-ttu-id="43cfb-114">Określa nazwę zadania Azure Stream Analytics, które ma się rozpocząć.</span><span class="sxs-lookup"><span data-stu-id="43cfb-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43cfb-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="43cfb-115">-OutputStartMode</span></span>
<span data-ttu-id="43cfb-116">Określa tryb uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="43cfb-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="43cfb-117">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="43cfb-117">Valid values are:</span></span> 
- <span data-ttu-id="43cfb-118">JobStartTime — ta wartość wskazuje, że punkt początkowy wyjściowego strumienia zdarzeń powinien się rozpocząć po uruchomieniu zadania.</span><span class="sxs-lookup"><span data-stu-id="43cfb-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="43cfb-119">CustomTime — ta wartość wskazuje, że punkt początkowy strumieniowego zdarzenia wyjściowego powinien rozpoczynać się w niestandardowej godzinie określonej w parametrze *OutputStartTime.*</span><span class="sxs-lookup"><span data-stu-id="43cfb-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="43cfb-120">LastOutputEventTime — ta wartość wskazuje, że punkt początkowy strumieniowego zdarzenia wyjściowego powinien rozpoczynać się od ostatniego czasu wyjściowego zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="43cfb-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="43cfb-121">Jeśli właściwość jest nieobecna, wartością domyślną jest JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="43cfb-121">If the property is absent, the default is JobStartTime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43cfb-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="43cfb-122">-OutputStartTime</span></span>
<span data-ttu-id="43cfb-123">Określa czas rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="43cfb-123">Specifies the output start time.</span></span>
<span data-ttu-id="43cfb-124">Ta wartość jest albo sformatowaną sygnaturą czasową ISO-8601, która wskazuje punkt początkowy wyjściowego strumienia zdarzeń, albo $Null, aby wskazać, że wyjściowy strumień zdarzeń będzie odtwarzany po każdym uruchomieniu zadania przesyłania strumieniowego.</span><span class="sxs-lookup"><span data-stu-id="43cfb-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="43cfb-125">Jeśli dla właściwości *OutputStartMode* ustawiono wartość CustomTime, ta właściwość musi mieć wartość.</span><span class="sxs-lookup"><span data-stu-id="43cfb-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43cfb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43cfb-126">-ResourceGroupName</span></span>
<span data-ttu-id="43cfb-127">Określa nazwę grupy zasobów, do której należy zadanie Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="43cfb-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43cfb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43cfb-128">CommonParameters</span></span>
<span data-ttu-id="43cfb-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43cfb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43cfb-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43cfb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43cfb-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43cfb-131">INPUTS</span></span>

### <span data-ttu-id="43cfb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="43cfb-132">System.String</span></span>

### <span data-ttu-id="43cfb-133">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="43cfb-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="43cfb-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43cfb-134">OUTPUTS</span></span>

### <span data-ttu-id="43cfb-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="43cfb-135">System.Boolean</span></span>

## <span data-ttu-id="43cfb-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="43cfb-136">NOTES</span></span>

## <span data-ttu-id="43cfb-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43cfb-137">RELATED LINKS</span></span>

[<span data-ttu-id="43cfb-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="43cfb-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="43cfb-139">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="43cfb-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="43cfb-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="43cfb-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="43cfb-141">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="43cfb-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


