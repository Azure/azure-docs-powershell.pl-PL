---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 5e34e0b1ba9e9ab24c0cb47de636ceecec9751f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888417"
---
# <span data-ttu-id="c6324-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c6324-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="c6324-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6324-102">SYNOPSIS</span></span>
<span data-ttu-id="c6324-103">Pobiera funkcje w zadaniu Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="c6324-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="c6324-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6324-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6324-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c6324-105">DESCRIPTION</span></span>
<span data-ttu-id="c6324-106">Polecenie cmdlet **Get-AzStreamAnalyticsFunction** pobiera listę funkcji zdefiniowanych w zadaniu usługi Analiza strumienia Azure lub informacje na temat określonej funkcji.</span><span class="sxs-lookup"><span data-stu-id="c6324-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="c6324-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6324-107">EXAMPLES</span></span>

### <span data-ttu-id="c6324-108">Przykład 1: pobieranie wszystkich funkcji analizy strumienia</span><span class="sxs-lookup"><span data-stu-id="c6324-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="c6324-109">To polecenie pobiera funkcje zdefiniowane w zadaniu o nazwie StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="c6324-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="c6324-110">Przykład 2: uzyskiwanie określonej funkcji analizy strumienia</span><span class="sxs-lookup"><span data-stu-id="c6324-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="c6324-111">To polecenie pobiera informacje o funkcji o nazwie ScoreTweet zdefiniowanej w zadaniu o nazwie StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="c6324-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="c6324-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6324-112">PARAMETERS</span></span>

### <span data-ttu-id="c6324-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6324-113">-DefaultProfile</span></span>
<span data-ttu-id="c6324-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6324-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6324-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="c6324-115">-JobName</span></span>
<span data-ttu-id="c6324-116">Określa nazwę zadania Stream Analytics, do którego należą funkcje.</span><span class="sxs-lookup"><span data-stu-id="c6324-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="c6324-117">To polecenie cmdlet pobiera funkcje dla zadania, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c6324-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6324-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c6324-118">-Name</span></span>
<span data-ttu-id="c6324-119">Określa nazwę funkcji Stream Analytics, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6324-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c6324-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6324-120">-ResourceGroupName</span></span>
<span data-ttu-id="c6324-121">Określa nazwę grupy zasobów, do której należą funkcje funkcji Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="c6324-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="c6324-122">To polecenie cmdlet pobiera funkcje dla grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c6324-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6324-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6324-123">CommonParameters</span></span>
<span data-ttu-id="c6324-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6324-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6324-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6324-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6324-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6324-126">INPUTS</span></span>

### <span data-ttu-id="c6324-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c6324-127">System.String</span></span>

## <span data-ttu-id="c6324-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6324-128">OUTPUTS</span></span>

### <span data-ttu-id="c6324-129">Microsoft. Azure. Commands. StreamAnalytics. models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="c6324-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="c6324-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6324-130">NOTES</span></span>

## <span data-ttu-id="c6324-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6324-131">RELATED LINKS</span></span>

[<span data-ttu-id="c6324-132">Nowe — AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c6324-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="c6324-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c6324-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="c6324-134">Test — AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="c6324-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


