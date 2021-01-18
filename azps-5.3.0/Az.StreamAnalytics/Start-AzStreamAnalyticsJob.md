---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502678"
---
# <span data-ttu-id="11cf7-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="11cf7-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="11cf7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="11cf7-103">Rozpoczyna zadanie analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="11cf7-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="11cf7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11cf7-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11cf7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="11cf7-105">DESCRIPTION</span></span>
<span data-ttu-id="11cf7-106">Polecenie cmdlet **Start-AzStreamAnalyticsJob** asynchronicznie wdraża i uruchamia zadanie Stream Analytics na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="11cf7-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="11cf7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11cf7-107">EXAMPLES</span></span>

### <span data-ttu-id="11cf7-108">Przykład 1. Uruchom zadanie analizy strumienia</span><span class="sxs-lookup"><span data-stu-id="11cf7-108">Example 1: Start a Stream Analytics job</span></span>
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="11cf7-109">To polecenie uruchamia zadanie StreamingJob i określa, że strumień zdarzeń wyjściowych powinien rozpoczynać się od sygnatury czasowej 2014 — 07-03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="11cf7-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="11cf7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11cf7-110">PARAMETERS</span></span>

### <span data-ttu-id="11cf7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11cf7-111">-DefaultProfile</span></span>
<span data-ttu-id="11cf7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11cf7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11cf7-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11cf7-113">-Name</span></span>
<span data-ttu-id="11cf7-114">Określa nazwę zadania usługi Azure Stream Analytics, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11cf7-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="11cf7-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="11cf7-115">-OutputStartMode</span></span>
<span data-ttu-id="11cf7-116">Określa tryb uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="11cf7-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="11cf7-117">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="11cf7-117">Valid values are:</span></span> 
- <span data-ttu-id="11cf7-118">JobStartTime — ta wartość wskazuje, że punkt początkowy strumienia zdarzeń wyjściowych powinien zostać uruchomiony po uruchomieniu zadania.</span><span class="sxs-lookup"><span data-stu-id="11cf7-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="11cf7-119">CustomTime — ta wartość wskazuje, że punkt początkowy strumienia zdarzeń wyjściowych powinien rozpoczynać się od niestandardowego czasu określonego w parametrze *OutputStartTime* .</span><span class="sxs-lookup"><span data-stu-id="11cf7-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="11cf7-120">LastOutputEventTime — ta wartość wskazuje, że punkt początkowy strumienia zdarzeń wyjściowych powinien rozpoczynać się od ostatniego czasu wyjściowego zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="11cf7-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="11cf7-121">Jeśli właściwość jest nieobecna, wartością domyślną jest JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="11cf7-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="11cf7-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="11cf7-122">-OutputStartTime</span></span>
<span data-ttu-id="11cf7-123">Określa godzinę rozpoczęcia produkcji.</span><span class="sxs-lookup"><span data-stu-id="11cf7-123">Specifies the output start time.</span></span>
<span data-ttu-id="11cf7-124">Ta wartość to sformatowana sygnatura czasowa ISO-8601, która wskazuje punkt początkowy strumienia zdarzeń wyjściowych, lub $Null, aby wskazać, że strumień zdarzeń wyjściowych rozpocznie się przy każdym uruchomieniu zadania przesyłania strumieniowego.</span><span class="sxs-lookup"><span data-stu-id="11cf7-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="11cf7-125">Właściwość ta musi mieć wartość, jeśli *OutputStartMode* jest ustawiona na CustomTime.</span><span class="sxs-lookup"><span data-stu-id="11cf7-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="11cf7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11cf7-126">-ResourceGroupName</span></span>
<span data-ttu-id="11cf7-127">Określa nazwę grupy zasobów, do której należy zadanie usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="11cf7-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="11cf7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11cf7-128">CommonParameters</span></span>
<span data-ttu-id="11cf7-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11cf7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11cf7-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11cf7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11cf7-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11cf7-131">INPUTS</span></span>

### <span data-ttu-id="11cf7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="11cf7-132">System.String</span></span>

### <span data-ttu-id="11cf7-133">System. Nullable "1 [[System. DateTime, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="11cf7-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="11cf7-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11cf7-134">OUTPUTS</span></span>

### <span data-ttu-id="11cf7-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11cf7-135">System.Boolean</span></span>

## <span data-ttu-id="11cf7-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11cf7-136">NOTES</span></span>

## <span data-ttu-id="11cf7-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11cf7-137">RELATED LINKS</span></span>

[<span data-ttu-id="11cf7-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="11cf7-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="11cf7-139">Nowe — AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="11cf7-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="11cf7-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="11cf7-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="11cf7-141">Zatrzymaj — AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="11cf7-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


