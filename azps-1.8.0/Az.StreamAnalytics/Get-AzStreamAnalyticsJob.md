---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 630f32bc9dd4542ad022ed7b65ec85f6456367b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707429"
---
# <span data-ttu-id="393af-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="393af-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="393af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="393af-102">SYNOPSIS</span></span>
<span data-ttu-id="393af-103">Pobiera informacje o zadaniach analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="393af-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="393af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="393af-104">SYNTAX</span></span>

### <span data-ttu-id="393af-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="393af-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="393af-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="393af-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="393af-107">Opis</span><span class="sxs-lookup"><span data-stu-id="393af-107">DESCRIPTION</span></span>
<span data-ttu-id="393af-108">Polecenie cmdlet **Get-AzStreamAnalyticsJob** wyświetla wszystkie zadania analizy strumienia zdefiniowane w subskrypcji platformy Azure lub określonej grupie zasobów albo pobiera informacje o zadaniach dotyczących określonego zadania w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="393af-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="393af-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="393af-109">EXAMPLES</span></span>

### <span data-ttu-id="393af-110">PRZYKŁAD 1: uzyskiwanie informacji o wszystkich zadaniach w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="393af-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="393af-111">To polecenie zwraca informacje na temat wszystkich zadań analizy strumienia w ramach subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="393af-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="393af-112">PRZYKŁAD 2: uzyskiwanie informacji o wszystkich zadaniach w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="393af-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="393af-113">To polecenie zwraca informacje na temat wszystkich zadań analizy strumienia w grupie zasób StreamAnalytics-default-zachód-my.</span><span class="sxs-lookup"><span data-stu-id="393af-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="393af-114">PRZYKŁAD 3: uzyskiwanie informacji o konkretnym zadaniu w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="393af-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="393af-115">To polecenie zwraca informacje o zadaniu Stream Analytics StreamingJob w grupie zasób StreamAnalytics-default-zachód-USA.</span><span class="sxs-lookup"><span data-stu-id="393af-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="393af-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="393af-116">PARAMETERS</span></span>

### <span data-ttu-id="393af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393af-117">-DefaultProfile</span></span>
<span data-ttu-id="393af-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="393af-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="393af-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="393af-119">-Name</span></span>
<span data-ttu-id="393af-120">Określa nazwę zadania usługi Azure Stream Analytics, które ma zostać pobrane.</span><span class="sxs-lookup"><span data-stu-id="393af-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="393af-121">-NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="393af-121">-NoExpand</span></span>
<span data-ttu-id="393af-122">Wskazuje, że polecenie cmdlet będzie pobierać zadanie usługi Azure Stream Analytics, ale nie zwraca informacji na temat danych wejściowych, wyjść i transformacji.</span><span class="sxs-lookup"><span data-stu-id="393af-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="393af-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="393af-123">-ResourceGroupName</span></span>
<span data-ttu-id="393af-124">Określa nazwę grupy zasobów, do której należy zadanie usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="393af-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="393af-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393af-125">CommonParameters</span></span>
<span data-ttu-id="393af-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="393af-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393af-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="393af-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393af-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="393af-128">INPUTS</span></span>

### <span data-ttu-id="393af-129">System. String</span><span class="sxs-lookup"><span data-stu-id="393af-129">System.String</span></span>

### <span data-ttu-id="393af-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="393af-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="393af-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="393af-131">OUTPUTS</span></span>

### <span data-ttu-id="393af-132">Microsoft. Azure. Commands. StreamAnalytics. models. PSJob</span><span class="sxs-lookup"><span data-stu-id="393af-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="393af-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="393af-133">NOTES</span></span>

## <span data-ttu-id="393af-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="393af-134">RELATED LINKS</span></span>

[<span data-ttu-id="393af-135">Nowe — AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="393af-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="393af-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="393af-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="393af-137">Start — AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="393af-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="393af-138">Zatrzymaj — AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="393af-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


