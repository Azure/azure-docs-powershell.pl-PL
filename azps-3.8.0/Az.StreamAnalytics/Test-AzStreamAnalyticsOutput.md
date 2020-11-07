---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: ba4eee78732e4217a6652fb6770ab5df8de05174
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895326"
---
# <span data-ttu-id="f1f9b-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f1f9b-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="f1f9b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f1f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f9b-103">Testuje stan połączenia danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f1f9b-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="f1f9b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f1f9b-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1f9b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f1f9b-105">DESCRIPTION</span></span>
<span data-ttu-id="f1f9b-106">Polecenie cmdlet **test-AzStreamAnalyticsOutput** testuje zdolność analizy strumienia do nawiązywania połączenia z danymi wyjściowymi.</span><span class="sxs-lookup"><span data-stu-id="f1f9b-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="f1f9b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f1f9b-107">EXAMPLES</span></span>

### <span data-ttu-id="f1f9b-108">PRZYKŁAD 1: testowanie stanu połączenia danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="f1f9b-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="f1f9b-109">Spowoduje to sprawdzenie stanu połączenia wyjściowej danych wyjściowych w programie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="f1f9b-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="f1f9b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1f9b-110">PARAMETERS</span></span>

### <span data-ttu-id="f1f9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f9b-111">-DefaultProfile</span></span>
<span data-ttu-id="f1f9b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1f9b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1f9b-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="f1f9b-113">-JobName</span></span>
<span data-ttu-id="f1f9b-114">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy żądana Produkcja Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="f1f9b-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f1f9b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f1f9b-115">-Name</span></span>
<span data-ttu-id="f1f9b-116">Określa nazwę danych wyjściowych funkcji Analiza strumienia Azure do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="f1f9b-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="f1f9b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1f9b-117">-ResourceGroupName</span></span>
<span data-ttu-id="f1f9b-118">Określa nazwę grupy zasobów, do której należy dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="f1f9b-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f1f9b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f9b-119">CommonParameters</span></span>
<span data-ttu-id="f1f9b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f9b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f9b-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f9b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f9b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1f9b-122">INPUTS</span></span>

### <span data-ttu-id="f1f9b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f1f9b-123">System.String</span></span>

## <span data-ttu-id="f1f9b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f1f9b-124">OUTPUTS</span></span>

### <span data-ttu-id="f1f9b-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1f9b-125">System.Boolean</span></span>

## <span data-ttu-id="f1f9b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f1f9b-126">NOTES</span></span>

## <span data-ttu-id="f1f9b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1f9b-127">RELATED LINKS</span></span>

[<span data-ttu-id="f1f9b-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f1f9b-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="f1f9b-129">Nowe — AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f1f9b-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="f1f9b-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f1f9b-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


