---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 1f959f96b02296d4cc25cca06ae6c95bdef98af7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973857"
---
# <span data-ttu-id="42f78-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="42f78-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="42f78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42f78-102">SYNOPSIS</span></span>
<span data-ttu-id="42f78-103">Pobiera dane wyjściowe zdefiniowane w określonym zadaniu lub danych wyjściowych usługi Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="42f78-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="42f78-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="42f78-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42f78-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="42f78-105">DESCRIPTION</span></span>
<span data-ttu-id="42f78-106">Polecenie **cmdlet Get-AzStreamAnalyticsOutput** wyświetla listę wszystkich wyników zdefiniowanych w określonym zadaniu analizy strumienia lub pobierających informacje o określonym wyniku.</span><span class="sxs-lookup"><span data-stu-id="42f78-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="42f78-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="42f78-107">EXAMPLES</span></span>

### <span data-ttu-id="42f78-108">Przykład 1. Uzyskiwanie informacji o wynikach zadań</span><span class="sxs-lookup"><span data-stu-id="42f78-108">Example 1: Get information about job outputs</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="42f78-109">To polecenie zwraca informacje o wynikach zdefiniowanych w zadaniu StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="42f78-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="42f78-110">Przykład 2. Uzyskiwanie informacji o określonym wyniku zadania</span><span class="sxs-lookup"><span data-stu-id="42f78-110">Example 2: Get information about a specific job output</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="42f78-111">To polecenie zwraca informacje o wynikach o nazwie Dane wyjściowe zdefiniowane w zadaniu StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="42f78-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="42f78-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42f78-112">PARAMETERS</span></span>

### <span data-ttu-id="42f78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f78-113">-DefaultProfile</span></span>
<span data-ttu-id="42f78-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="42f78-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42f78-115">— JobName</span><span class="sxs-lookup"><span data-stu-id="42f78-115">-JobName</span></span>
<span data-ttu-id="42f78-116">Określa nazwę zadania Azure Stream Analytics, do którego należy dane wyjściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="42f78-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="42f78-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="42f78-117">-Name</span></span>
<span data-ttu-id="42f78-118">Określa nazwę danych wyjściowych usługi Azure Stream Analytics do pobrania.</span><span class="sxs-lookup"><span data-stu-id="42f78-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="42f78-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42f78-119">-ResourceGroupName</span></span>
<span data-ttu-id="42f78-120">Określa nazwę grupy zasobów, do której należy dane wyjściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="42f78-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="42f78-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f78-121">CommonParameters</span></span>
<span data-ttu-id="42f78-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42f78-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f78-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42f78-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f78-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42f78-124">INPUTS</span></span>

### <span data-ttu-id="42f78-125">System.String</span><span class="sxs-lookup"><span data-stu-id="42f78-125">System.String</span></span>

## <span data-ttu-id="42f78-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42f78-126">OUTPUTS</span></span>

### <span data-ttu-id="42f78-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="42f78-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="42f78-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="42f78-128">NOTES</span></span>

## <span data-ttu-id="42f78-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42f78-129">RELATED LINKS</span></span>

[<span data-ttu-id="42f78-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="42f78-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="42f78-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="42f78-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="42f78-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="42f78-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


