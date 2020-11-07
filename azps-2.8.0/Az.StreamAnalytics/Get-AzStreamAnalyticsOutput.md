---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: bf4a8734304ce92dac1bc329d6ae0ffa0f30c09c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871424"
---
# <span data-ttu-id="84628-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="84628-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="84628-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84628-102">SYNOPSIS</span></span>
<span data-ttu-id="84628-103">Pobiera wyniki zdefiniowane w określonym zadaniu Stream Analytics lub wyjściu.</span><span class="sxs-lookup"><span data-stu-id="84628-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="84628-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84628-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84628-105">Opis</span><span class="sxs-lookup"><span data-stu-id="84628-105">DESCRIPTION</span></span>
<span data-ttu-id="84628-106">Polecenie cmdlet **Get-AzStreamAnalyticsOutput** wyświetla listę wszystkich wyników zdefiniowanych w określonym zadaniu Stream Analytics lub pobiera informacje dotyczące konkretnego wyniku.</span><span class="sxs-lookup"><span data-stu-id="84628-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="84628-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84628-107">EXAMPLES</span></span>

### <span data-ttu-id="84628-108">PRZYKŁAD 1: uzyskiwanie informacji o wyjściach z zadań</span><span class="sxs-lookup"><span data-stu-id="84628-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="84628-109">To polecenie zwraca informacje o danych wyjściowych zdefiniowanych w StreamingJobie zadania.</span><span class="sxs-lookup"><span data-stu-id="84628-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="84628-110">PRZYKŁAD 2: uzyskiwanie informacji na temat określonego wyjścia zlecenia</span><span class="sxs-lookup"><span data-stu-id="84628-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="84628-111">To polecenie zwraca informacje o wynikach o nazwie dane wyjściowe zdefiniowane w StreamingJob zadania.</span><span class="sxs-lookup"><span data-stu-id="84628-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="84628-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84628-112">PARAMETERS</span></span>

### <span data-ttu-id="84628-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84628-113">-DefaultProfile</span></span>
<span data-ttu-id="84628-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84628-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84628-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="84628-115">-JobName</span></span>
<span data-ttu-id="84628-116">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="84628-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="84628-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84628-117">-Name</span></span>
<span data-ttu-id="84628-118">Określa nazwę danych wyjściowych funkcji Analiza strumienia Azure do pobrania.</span><span class="sxs-lookup"><span data-stu-id="84628-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="84628-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84628-119">-ResourceGroupName</span></span>
<span data-ttu-id="84628-120">Określa nazwę grupy zasobów, do której należy dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="84628-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="84628-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84628-121">CommonParameters</span></span>
<span data-ttu-id="84628-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84628-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84628-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84628-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84628-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84628-124">INPUTS</span></span>

### <span data-ttu-id="84628-125">System. String</span><span class="sxs-lookup"><span data-stu-id="84628-125">System.String</span></span>

## <span data-ttu-id="84628-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84628-126">OUTPUTS</span></span>

### <span data-ttu-id="84628-127">Microsoft. Azure. Commands. StreamAnalytics. models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="84628-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="84628-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84628-128">NOTES</span></span>

## <span data-ttu-id="84628-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84628-129">RELATED LINKS</span></span>

[<span data-ttu-id="84628-130">Nowe — AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="84628-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="84628-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="84628-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="84628-132">Test — AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="84628-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


