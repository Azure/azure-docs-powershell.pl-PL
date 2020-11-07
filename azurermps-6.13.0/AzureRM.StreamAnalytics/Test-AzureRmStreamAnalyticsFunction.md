---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: c62d829da193ae36f10a64149260cf34c6bc20ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551968"
---
# <span data-ttu-id="7372d-101">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7372d-101">Test-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="7372d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7372d-102">SYNOPSIS</span></span>
<span data-ttu-id="7372d-103">Sprawdza, czy Analiza strumienia może nawiązać połączenie z funkcją.</span><span class="sxs-lookup"><span data-stu-id="7372d-103">Tests whether Stream Analytics can connect to a function.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7372d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7372d-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7372d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7372d-105">DESCRIPTION</span></span>
<span data-ttu-id="7372d-106">Polecenie cmdlet **test-AzureRmStreamAnalyticsFunction** sprawdza, czy usługa Azure Stream Analytics może nawiązać połączenie z funkcją.</span><span class="sxs-lookup"><span data-stu-id="7372d-106">The **Test-AzureRmStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="7372d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7372d-107">EXAMPLES</span></span>

### <span data-ttu-id="7372d-108">Przykład 1: Testowanie funkcji Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="7372d-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="7372d-109">To polecenie testuje stan połączenia funkcji o nazwie ScoreTweet w zadaniu o nazwie StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="7372d-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="7372d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7372d-110">PARAMETERS</span></span>

### <span data-ttu-id="7372d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7372d-111">-DefaultProfile</span></span>
<span data-ttu-id="7372d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7372d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7372d-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="7372d-113">-JobName</span></span>
<span data-ttu-id="7372d-114">Określa nazwę zadania Stream Analytics, do którego należy funkcja.</span><span class="sxs-lookup"><span data-stu-id="7372d-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="7372d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7372d-115">-Name</span></span>
<span data-ttu-id="7372d-116">Określa nazwę funkcji Stream Analytics, którą testuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7372d-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="7372d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7372d-117">-ResourceGroupName</span></span>
<span data-ttu-id="7372d-118">Określa nazwę grupy zasobów, do której należy funkcja Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="7372d-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="7372d-119">To polecenie cmdlet testuje działanie w grupie zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7372d-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7372d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7372d-120">CommonParameters</span></span>
<span data-ttu-id="7372d-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7372d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7372d-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7372d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7372d-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7372d-123">INPUTS</span></span>

### <span data-ttu-id="7372d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7372d-124">System.String</span></span>

## <span data-ttu-id="7372d-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7372d-125">OUTPUTS</span></span>

### <span data-ttu-id="7372d-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7372d-126">System.Boolean</span></span>

## <span data-ttu-id="7372d-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7372d-127">NOTES</span></span>

## <span data-ttu-id="7372d-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7372d-128">RELATED LINKS</span></span>

[<span data-ttu-id="7372d-129">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7372d-129">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="7372d-130">Nowe — AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7372d-130">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="7372d-131">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7372d-131">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

