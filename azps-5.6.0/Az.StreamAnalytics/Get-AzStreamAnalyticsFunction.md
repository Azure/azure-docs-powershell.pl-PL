---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 681782db0e1621e8d1126ca1f3425ce87e8e30d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973921"
---
# <span data-ttu-id="67a49-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="67a49-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="67a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67a49-102">SYNOPSIS</span></span>
<span data-ttu-id="67a49-103">Pobiera funkcje w zadaniu Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="67a49-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="67a49-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67a49-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67a49-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="67a49-105">DESCRIPTION</span></span>
<span data-ttu-id="67a49-106">Polecenie **cmdlet Get-AzStreamAnalyticsFunction** pobiera listę funkcji zdefiniowanych w zadaniu usługi Azure Stream Analytics lub w informacjach o określonej funkcji.</span><span class="sxs-lookup"><span data-stu-id="67a49-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="67a49-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67a49-107">EXAMPLES</span></span>

### <span data-ttu-id="67a49-108">Przykład 1. Uzyskiwanie wszystkich funkcji analizy strumienia</span><span class="sxs-lookup"><span data-stu-id="67a49-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="67a49-109">To polecenie pobiera funkcje zdefiniowane w zadaniu o nazwie StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="67a49-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="67a49-110">Przykład 2. Uzyskiwanie konkretnej funkcji Analiza strumienia</span><span class="sxs-lookup"><span data-stu-id="67a49-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="67a49-111">To polecenie pobiera informacje o funkcji o nazwie ScoreTweet zdefiniowanej w zadaniu o nazwie StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="67a49-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="67a49-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67a49-112">PARAMETERS</span></span>

### <span data-ttu-id="67a49-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a49-113">-DefaultProfile</span></span>
<span data-ttu-id="67a49-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67a49-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67a49-115">— JobName</span><span class="sxs-lookup"><span data-stu-id="67a49-115">-JobName</span></span>
<span data-ttu-id="67a49-116">Określa nazwę zadania analiza strumienia, do którego należą funkcje.</span><span class="sxs-lookup"><span data-stu-id="67a49-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="67a49-117">To polecenie cmdlet pobiera funkcje dla zadania, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="67a49-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="67a49-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="67a49-118">-Name</span></span>
<span data-ttu-id="67a49-119">Określa nazwę funkcji Analiza strumienia, która będzie pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67a49-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="67a49-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67a49-120">-ResourceGroupName</span></span>
<span data-ttu-id="67a49-121">Określa nazwę grupy zasobów, do której należą funkcje analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="67a49-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="67a49-122">To polecenie cmdlet pobiera funkcje dla grupy, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="67a49-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="67a49-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a49-123">CommonParameters</span></span>
<span data-ttu-id="67a49-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a49-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a49-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67a49-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a49-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67a49-126">INPUTS</span></span>

### <span data-ttu-id="67a49-127">System.String</span><span class="sxs-lookup"><span data-stu-id="67a49-127">System.String</span></span>

## <span data-ttu-id="67a49-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67a49-128">OUTPUTS</span></span>

### <span data-ttu-id="67a49-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="67a49-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="67a49-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67a49-130">NOTES</span></span>

## <span data-ttu-id="67a49-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67a49-131">RELATED LINKS</span></span>

[<span data-ttu-id="67a49-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="67a49-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="67a49-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="67a49-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="67a49-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="67a49-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


