---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: f9139514850fe9d538c58d14813e91d2d24de502
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707395"
---
# <span data-ttu-id="cba1a-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="cba1a-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="cba1a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cba1a-102">SYNOPSIS</span></span>
<span data-ttu-id="cba1a-103">Sprawdza, czy Analiza strumienia może nawiązać połączenie z funkcją.</span><span class="sxs-lookup"><span data-stu-id="cba1a-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="cba1a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cba1a-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cba1a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cba1a-105">DESCRIPTION</span></span>
<span data-ttu-id="cba1a-106">Polecenie cmdlet **test-AzStreamAnalyticsFunction** sprawdza, czy usługa Azure Stream Analytics może nawiązać połączenie z funkcją.</span><span class="sxs-lookup"><span data-stu-id="cba1a-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="cba1a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cba1a-107">EXAMPLES</span></span>

### <span data-ttu-id="cba1a-108">Przykład 1: Testowanie funkcji Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="cba1a-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="cba1a-109">To polecenie testuje stan połączenia funkcji o nazwie ScoreTweet w zadaniu o nazwie StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="cba1a-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="cba1a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cba1a-110">PARAMETERS</span></span>

### <span data-ttu-id="cba1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba1a-111">-DefaultProfile</span></span>
<span data-ttu-id="cba1a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cba1a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cba1a-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="cba1a-113">-JobName</span></span>
<span data-ttu-id="cba1a-114">Określa nazwę zadania Stream Analytics, do którego należy funkcja.</span><span class="sxs-lookup"><span data-stu-id="cba1a-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="cba1a-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cba1a-115">-Name</span></span>
<span data-ttu-id="cba1a-116">Określa nazwę funkcji Stream Analytics, którą testuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cba1a-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba1a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba1a-117">-ResourceGroupName</span></span>
<span data-ttu-id="cba1a-118">Określa nazwę grupy zasobów, do której należy funkcja Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="cba1a-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="cba1a-119">To polecenie cmdlet testuje działanie w grupie zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cba1a-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cba1a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba1a-120">CommonParameters</span></span>
<span data-ttu-id="cba1a-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cba1a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba1a-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cba1a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba1a-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cba1a-123">INPUTS</span></span>

### <span data-ttu-id="cba1a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="cba1a-124">System.String</span></span>

## <span data-ttu-id="cba1a-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cba1a-125">OUTPUTS</span></span>

### <span data-ttu-id="cba1a-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cba1a-126">System.Boolean</span></span>

## <span data-ttu-id="cba1a-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cba1a-127">NOTES</span></span>

## <span data-ttu-id="cba1a-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cba1a-128">RELATED LINKS</span></span>

[<span data-ttu-id="cba1a-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="cba1a-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="cba1a-130">Nowe — AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="cba1a-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="cba1a-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="cba1a-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


