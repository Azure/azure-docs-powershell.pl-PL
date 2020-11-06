---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 4a387da5b8f1f4ed9e6f3653a32ff8880ffaa734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544635"
---
# <span data-ttu-id="9fc61-101">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="9fc61-101">Get-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="9fc61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fc61-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc61-103">Pobiera funkcje w zadaniu Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="9fc61-103">Gets functions in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fc61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fc61-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fc61-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9fc61-105">DESCRIPTION</span></span>
<span data-ttu-id="9fc61-106">Polecenie cmdlet **Get-AzureRmStreamAnalyticsFunction** pobiera listę funkcji zdefiniowanych w zadaniu usługi Analiza strumienia Azure lub informacje na temat określonej funkcji.</span><span class="sxs-lookup"><span data-stu-id="9fc61-106">The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="9fc61-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fc61-107">EXAMPLES</span></span>

### <span data-ttu-id="9fc61-108">Przykład 1: pobieranie wszystkich funkcji analizy strumienia</span><span class="sxs-lookup"><span data-stu-id="9fc61-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="9fc61-109">To polecenie pobiera funkcje zdefiniowane w zadaniu o nazwie StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="9fc61-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="9fc61-110">Przykład 2: uzyskiwanie określonej funkcji analizy strumienia</span><span class="sxs-lookup"><span data-stu-id="9fc61-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="9fc61-111">To polecenie pobiera informacje o funkcji o nazwie ScoreTweet zdefiniowanej w zadaniu o nazwie StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="9fc61-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="9fc61-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fc61-112">PARAMETERS</span></span>

### <span data-ttu-id="9fc61-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="9fc61-113">-JobName</span></span>
<span data-ttu-id="9fc61-114">Określa nazwę zadania Stream Analytics, do którego należą funkcje.</span><span class="sxs-lookup"><span data-stu-id="9fc61-114">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="9fc61-115">To polecenie cmdlet pobiera funkcje dla zadania, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9fc61-115">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="9fc61-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9fc61-116">-Name</span></span>
<span data-ttu-id="9fc61-117">Określa nazwę funkcji Stream Analytics, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fc61-117">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9fc61-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fc61-118">-ResourceGroupName</span></span>
<span data-ttu-id="9fc61-119">Określa nazwę grupy zasobów, do której należą funkcje funkcji Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="9fc61-119">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="9fc61-120">To polecenie cmdlet pobiera funkcje dla grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9fc61-120">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9fc61-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc61-121">-DefaultProfile</span></span>
<span data-ttu-id="9fc61-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fc61-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fc61-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc61-123">CommonParameters</span></span>
<span data-ttu-id="9fc61-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fc61-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc61-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fc61-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc61-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fc61-126">INPUTS</span></span>

## <span data-ttu-id="9fc61-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fc61-127">OUTPUTS</span></span>

### <span data-ttu-id="9fc61-128">System. Collections. Generic. list [Microsoft. Azure. Commands. StreamAnalytics. MODELES. PSFunction, Microsoft. Azure. Commands. StreamAnalytics], Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="9fc61-128">System.Collections.Generic.List[Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction, Microsoft.Azure.Commands.StreamAnalytics], Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="9fc61-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fc61-129">NOTES</span></span>

## <span data-ttu-id="9fc61-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fc61-130">RELATED LINKS</span></span>

[<span data-ttu-id="9fc61-131">Nowe — AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="9fc61-131">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="9fc61-132">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="9fc61-132">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="9fc61-133">Test — AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="9fc61-133">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


