---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 28a595b3e63a01439417ed07f6fd47c1cfc40a79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981962"
---
# <span data-ttu-id="d8ec6-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d8ec6-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="d8ec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ec6-103">Sprawdza stan połączenia danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d8ec6-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="d8ec6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8ec6-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8ec6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8ec6-105">DESCRIPTION</span></span>
<span data-ttu-id="d8ec6-106">Polecenie **cmdlet Test-AzStreamAnalyticsOutput** sprawdza możliwość łączenia się z wyjściem przez usługę Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d8ec6-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="d8ec6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8ec6-107">EXAMPLES</span></span>

### <span data-ttu-id="d8ec6-108">Przykład 1. Testowanie stanu połączenia danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="d8ec6-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="d8ec6-109">To sprawdza stan połączenia wyjściowego danych wyjściowych w transmisję strumieniową WI-Fi.</span><span class="sxs-lookup"><span data-stu-id="d8ec6-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="d8ec6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8ec6-110">PARAMETERS</span></span>

### <span data-ttu-id="d8ec6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ec6-111">-DefaultProfile</span></span>
<span data-ttu-id="d8ec6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8ec6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8ec6-113">— JobName</span><span class="sxs-lookup"><span data-stu-id="d8ec6-113">-JobName</span></span>
<span data-ttu-id="d8ec6-114">Określa nazwę zadania Azure Stream Analytics, do którego należy żądane dane wyjściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d8ec6-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="d8ec6-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d8ec6-115">-Name</span></span>
<span data-ttu-id="d8ec6-116">Określa nazwę danych wyjściowych usługi Azure Stream Analytics do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="d8ec6-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="d8ec6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8ec6-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8ec6-118">Określa nazwę grupy zasobów, do której należy dane wyjściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d8ec6-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="d8ec6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ec6-119">CommonParameters</span></span>
<span data-ttu-id="d8ec6-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ec6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ec6-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8ec6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ec6-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8ec6-122">INPUTS</span></span>

### <span data-ttu-id="d8ec6-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d8ec6-123">System.String</span></span>

## <span data-ttu-id="d8ec6-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8ec6-124">OUTPUTS</span></span>

### <span data-ttu-id="d8ec6-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ec6-125">System.Boolean</span></span>

## <span data-ttu-id="d8ec6-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8ec6-126">NOTES</span></span>

## <span data-ttu-id="d8ec6-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8ec6-127">RELATED LINKS</span></span>

[<span data-ttu-id="d8ec6-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d8ec6-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="d8ec6-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d8ec6-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="d8ec6-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d8ec6-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


