---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: dd2a52167a773b241364311ed4e0e00c03ea8459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544047"
---
# <span data-ttu-id="85864-101">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="85864-101">Get-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="85864-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85864-102">SYNOPSIS</span></span>
<span data-ttu-id="85864-103">Pobiera funkcje w zadaniu Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="85864-103">Gets functions in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85864-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85864-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85864-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85864-105">DESCRIPTION</span></span>
<span data-ttu-id="85864-106">Polecenie cmdlet **Get-AzureRmStreamAnalyticsFunction** pobiera listę funkcji zdefiniowanych w zadaniu usługi Analiza strumienia Azure lub informacje na temat określonej funkcji.</span><span class="sxs-lookup"><span data-stu-id="85864-106">The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="85864-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85864-107">EXAMPLES</span></span>

### <span data-ttu-id="85864-108">Przykład 1: pobieranie wszystkich funkcji analizy strumienia</span><span class="sxs-lookup"><span data-stu-id="85864-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="85864-109">To polecenie pobiera funkcje zdefiniowane w zadaniu o nazwie StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="85864-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="85864-110">Przykład 2: uzyskiwanie określonej funkcji analizy strumienia</span><span class="sxs-lookup"><span data-stu-id="85864-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="85864-111">To polecenie pobiera informacje o funkcji o nazwie ScoreTweet zdefiniowanej w zadaniu o nazwie StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="85864-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="85864-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85864-112">PARAMETERS</span></span>

### <span data-ttu-id="85864-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85864-113">-DefaultProfile</span></span>
<span data-ttu-id="85864-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85864-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85864-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="85864-115">-JobName</span></span>
<span data-ttu-id="85864-116">Określa nazwę zadania Stream Analytics, do którego należą funkcje.</span><span class="sxs-lookup"><span data-stu-id="85864-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="85864-117">To polecenie cmdlet pobiera funkcje dla zadania, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="85864-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="85864-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85864-118">-Name</span></span>
<span data-ttu-id="85864-119">Określa nazwę funkcji Stream Analytics, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85864-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="85864-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85864-120">-ResourceGroupName</span></span>
<span data-ttu-id="85864-121">Określa nazwę grupy zasobów, do której należą funkcje funkcji Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="85864-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="85864-122">To polecenie cmdlet pobiera funkcje dla grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="85864-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="85864-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85864-123">CommonParameters</span></span>
<span data-ttu-id="85864-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85864-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85864-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85864-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85864-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85864-126">INPUTS</span></span>

### <span data-ttu-id="85864-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="85864-127">None</span></span>
<span data-ttu-id="85864-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="85864-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85864-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85864-129">OUTPUTS</span></span>

### <span data-ttu-id="85864-130">System. Collections. Generic. list [Microsoft. Azure. Commands. StreamAnalytics. MODELES. PSFunction, Microsoft. Azure. Commands. StreamAnalytics], Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="85864-130">System.Collections.Generic.List[Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction, Microsoft.Azure.Commands.StreamAnalytics], Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="85864-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85864-131">NOTES</span></span>

## <span data-ttu-id="85864-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85864-132">RELATED LINKS</span></span>

[<span data-ttu-id="85864-133">Nowe — AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="85864-133">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="85864-134">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="85864-134">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="85864-135">Test — AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="85864-135">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


