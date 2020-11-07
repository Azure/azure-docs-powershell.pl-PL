---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: c675a8da84e61b659c593cc1f963dd1b07c7f316
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524242"
---
# <span data-ttu-id="42682-101">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="42682-101">Get-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="42682-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42682-102">SYNOPSIS</span></span>
<span data-ttu-id="42682-103">Pobiera wyniki zdefiniowane w określonym zadaniu Stream Analytics lub wyjściu.</span><span class="sxs-lookup"><span data-stu-id="42682-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42682-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42682-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42682-105">Opis</span><span class="sxs-lookup"><span data-stu-id="42682-105">DESCRIPTION</span></span>
<span data-ttu-id="42682-106">Polecenie cmdlet **Get-AzureRmStreamAnalyticsOutput** wyświetla listę wszystkich wyników zdefiniowanych w określonym zadaniu Stream Analytics lub pobiera informacje dotyczące konkretnego wyniku.</span><span class="sxs-lookup"><span data-stu-id="42682-106">The **Get-AzureRmStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="42682-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42682-107">EXAMPLES</span></span>

### <span data-ttu-id="42682-108">PRZYKŁAD 1: uzyskiwanie informacji o wyjściach z zadań</span><span class="sxs-lookup"><span data-stu-id="42682-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="42682-109">To polecenie zwraca informacje o danych wyjściowych zdefiniowanych w StreamingJobie zadania.</span><span class="sxs-lookup"><span data-stu-id="42682-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="42682-110">PRZYKŁAD 2: uzyskiwanie informacji na temat określonego wyjścia zlecenia</span><span class="sxs-lookup"><span data-stu-id="42682-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="42682-111">To polecenie zwraca informacje o wynikach o nazwie dane wyjściowe zdefiniowane w StreamingJob zadania.</span><span class="sxs-lookup"><span data-stu-id="42682-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="42682-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42682-112">PARAMETERS</span></span>

### <span data-ttu-id="42682-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42682-113">-DefaultProfile</span></span>
<span data-ttu-id="42682-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42682-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42682-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="42682-115">-JobName</span></span>
<span data-ttu-id="42682-116">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="42682-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="42682-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42682-117">-Name</span></span>
<span data-ttu-id="42682-118">Określa nazwę danych wyjściowych funkcji Analiza strumienia Azure do pobrania.</span><span class="sxs-lookup"><span data-stu-id="42682-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="42682-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42682-119">-ResourceGroupName</span></span>
<span data-ttu-id="42682-120">Określa nazwę grupy zasobów, do której należy dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="42682-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="42682-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42682-121">CommonParameters</span></span>
<span data-ttu-id="42682-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42682-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42682-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42682-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42682-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42682-124">INPUTS</span></span>

### <span data-ttu-id="42682-125">System. String</span><span class="sxs-lookup"><span data-stu-id="42682-125">System.String</span></span>

## <span data-ttu-id="42682-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42682-126">OUTPUTS</span></span>

### <span data-ttu-id="42682-127">Microsoft. Azure. Commands. StreamAnalytics. models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="42682-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="42682-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42682-128">NOTES</span></span>

## <span data-ttu-id="42682-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42682-129">RELATED LINKS</span></span>

[<span data-ttu-id="42682-130">Nowe — AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="42682-130">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="42682-131">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="42682-131">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="42682-132">Test — AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="42682-132">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)

