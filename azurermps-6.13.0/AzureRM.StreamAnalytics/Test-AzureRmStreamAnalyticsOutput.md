---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: f8bd4feab9bdcf99daf713d3a584a574f699a8b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525954"
---
# <span data-ttu-id="a218d-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a218d-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="a218d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a218d-102">SYNOPSIS</span></span>
<span data-ttu-id="a218d-103">Testuje stan połączenia danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a218d-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a218d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a218d-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a218d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a218d-105">DESCRIPTION</span></span>
<span data-ttu-id="a218d-106">Polecenie cmdlet **test-AzureRmStreamAnalyticsOutput** testuje zdolność analizy strumienia do nawiązywania połączenia z danymi wyjściowymi.</span><span class="sxs-lookup"><span data-stu-id="a218d-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="a218d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a218d-107">EXAMPLES</span></span>

### <span data-ttu-id="a218d-108">PRZYKŁAD 1: testowanie stanu połączenia danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="a218d-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="a218d-109">Spowoduje to sprawdzenie stanu połączenia wyjściowej danych wyjściowych w programie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="a218d-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="a218d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a218d-110">PARAMETERS</span></span>

### <span data-ttu-id="a218d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a218d-111">-DefaultProfile</span></span>
<span data-ttu-id="a218d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a218d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a218d-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="a218d-113">-JobName</span></span>
<span data-ttu-id="a218d-114">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy żądana Produkcja Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a218d-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="a218d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a218d-115">-Name</span></span>
<span data-ttu-id="a218d-116">Określa nazwę danych wyjściowych funkcji Analiza strumienia Azure do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="a218d-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="a218d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a218d-117">-ResourceGroupName</span></span>
<span data-ttu-id="a218d-118">Określa nazwę grupy zasobów, do której należy dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="a218d-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="a218d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a218d-119">CommonParameters</span></span>
<span data-ttu-id="a218d-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a218d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a218d-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a218d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a218d-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a218d-122">INPUTS</span></span>

### <span data-ttu-id="a218d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a218d-123">System.String</span></span>

## <span data-ttu-id="a218d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a218d-124">OUTPUTS</span></span>

### <span data-ttu-id="a218d-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a218d-125">System.Boolean</span></span>

## <span data-ttu-id="a218d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a218d-126">NOTES</span></span>

## <span data-ttu-id="a218d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a218d-127">RELATED LINKS</span></span>

[<span data-ttu-id="a218d-128">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a218d-128">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="a218d-129">Nowe — AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a218d-129">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="a218d-130">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a218d-130">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


