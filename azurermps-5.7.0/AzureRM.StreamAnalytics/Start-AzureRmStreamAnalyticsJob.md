---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/start-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: a4e6ac26eeca6150feabaa07dc28a787ea01112d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524793"
---
# <span data-ttu-id="f7ae1-101">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f7ae1-101">Start-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="f7ae1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ae1-103">Rozpoczyna zadanie analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-103">Starts a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7ae1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7ae1-104">SYNTAX</span></span>

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7ae1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7ae1-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ae1-106">Polecenie cmdlet **Start-AzureRmStreamAnalyticsJob** asynchronicznie wdraża i uruchamia zadanie Stream Analytics na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-106">The **Start-AzureRmStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="f7ae1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7ae1-107">EXAMPLES</span></span>

### <span data-ttu-id="f7ae1-108">PRZYKŁAD 1. Uruchom zadanie analizy strumienia</span><span class="sxs-lookup"><span data-stu-id="f7ae1-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="f7ae1-109">To polecenie uruchamia zadanie StreamingJob i określa, że strumień zdarzeń wyjściowych powinien rozpoczynać się od sygnatury czasowej 2014 — 07-03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="f7ae1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7ae1-110">PARAMETERS</span></span>

### <span data-ttu-id="f7ae1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ae1-111">-DefaultProfile</span></span>
<span data-ttu-id="f7ae1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7ae1-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7ae1-113">-Name</span></span>
<span data-ttu-id="f7ae1-114">Określa nazwę zadania usługi Azure Stream Analytics, które ma zostać uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7ae1-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="f7ae1-115">-OutputStartMode</span></span>
<span data-ttu-id="f7ae1-116">Określa tryb uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="f7ae1-117">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="f7ae1-117">Valid values are:</span></span> 

- <span data-ttu-id="f7ae1-118">JobStartTime — ta wartość wskazuje, że punkt początkowy strumienia zdarzeń wyjściowych powinien zostać uruchomiony po uruchomieniu zadania.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="f7ae1-119">CustomTime — ta wartość wskazuje, że punkt początkowy strumienia zdarzeń wyjściowych powinien rozpoczynać się od niestandardowego czasu określonego w parametrze *OutputStartTime* .</span><span class="sxs-lookup"><span data-stu-id="f7ae1-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 <span data-ttu-id="f7ae1-120">--LastOutputEventTime-ta wartość wskazuje, że punkt początkowy strumienia zdarzeń wyjściowych powinien rozpoczynać się od ostatniego czasu wyjściowego zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-120">-- LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>

<span data-ttu-id="f7ae1-121">Jeśli właściwość jest nieobecna, wartością domyślną jest JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-121">If the property is absent, the default is JobStartTime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7ae1-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="f7ae1-122">-OutputStartTime</span></span>
<span data-ttu-id="f7ae1-123">Określa godzinę rozpoczęcia produkcji.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-123">Specifies the output start time.</span></span>
<span data-ttu-id="f7ae1-124">Ta wartość to sformatowana sygnatura czasowa ISO-8601, która wskazuje punkt początkowy strumienia zdarzeń wyjściowych, lub $Null, aby wskazać, że strumień zdarzeń wyjściowych rozpocznie się przy każdym uruchomieniu zadania przesyłania strumieniowego.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="f7ae1-125">Właściwość ta musi mieć wartość, jeśli *OutputStartMode* jest ustawiona na CustomTime.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7ae1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7ae1-126">-ResourceGroupName</span></span>
<span data-ttu-id="f7ae1-127">Określa nazwę grupy zasobów, do której należy zadanie usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7ae1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ae1-128">CommonParameters</span></span>
<span data-ttu-id="f7ae1-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ae1-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7ae1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ae1-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7ae1-131">INPUTS</span></span>

### <span data-ttu-id="f7ae1-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f7ae1-132">None</span></span>
<span data-ttu-id="f7ae1-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f7ae1-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7ae1-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7ae1-134">OUTPUTS</span></span>

### <span data-ttu-id="f7ae1-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="f7ae1-135">System.Object</span></span>

## <span data-ttu-id="f7ae1-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7ae1-136">NOTES</span></span>

## <span data-ttu-id="f7ae1-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7ae1-137">RELATED LINKS</span></span>

[<span data-ttu-id="f7ae1-138">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f7ae1-138">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="f7ae1-139">Nowe — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f7ae1-139">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="f7ae1-140">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f7ae1-140">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="f7ae1-141">Zatrzymaj — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f7ae1-141">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


