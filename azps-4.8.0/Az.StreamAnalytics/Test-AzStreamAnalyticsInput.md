---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: e353e1e8be820c96f1eb1381274a8e245f542947
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064615"
---
# <span data-ttu-id="d87fd-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="d87fd-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="d87fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d87fd-102">SYNOPSIS</span></span>
<span data-ttu-id="d87fd-103">Testuje stan połączenia wejściowego.</span><span class="sxs-lookup"><span data-stu-id="d87fd-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="d87fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d87fd-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d87fd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d87fd-105">DESCRIPTION</span></span>
<span data-ttu-id="d87fd-106">Polecenie cmdlet **test-AzStreamAnalyticsInput** testuje zdolność analizy strumienia do nawiązywania połączenia z danymi wejściowymi.</span><span class="sxs-lookup"><span data-stu-id="d87fd-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="d87fd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d87fd-107">EXAMPLES</span></span>

### <span data-ttu-id="d87fd-108">Przykład 1: testowanie stanu połączenia strumienia wejściowego</span><span class="sxs-lookup"><span data-stu-id="d87fd-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="d87fd-109">To testuje stan połączenia w EntryStream wejściowym in StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="d87fd-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="d87fd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d87fd-110">PARAMETERS</span></span>

### <span data-ttu-id="d87fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d87fd-111">-DefaultProfile</span></span>
<span data-ttu-id="d87fd-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d87fd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d87fd-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="d87fd-113">-JobName</span></span>
<span data-ttu-id="d87fd-114">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="d87fd-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="d87fd-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d87fd-115">-Name</span></span>
<span data-ttu-id="d87fd-116">Określa nazwę danych wejściowych funkcji Analiza strumienia Azure do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="d87fd-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="d87fd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d87fd-117">-ResourceGroupName</span></span>
<span data-ttu-id="d87fd-118">Określa nazwę grupy zasobów, do której należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="d87fd-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="d87fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87fd-119">CommonParameters</span></span>
<span data-ttu-id="d87fd-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d87fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87fd-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d87fd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87fd-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d87fd-122">INPUTS</span></span>

### <span data-ttu-id="d87fd-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d87fd-123">System.String</span></span>

## <span data-ttu-id="d87fd-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d87fd-124">OUTPUTS</span></span>

### <span data-ttu-id="d87fd-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d87fd-125">System.Boolean</span></span>

## <span data-ttu-id="d87fd-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d87fd-126">NOTES</span></span>

## <span data-ttu-id="d87fd-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d87fd-127">RELATED LINKS</span></span>

[<span data-ttu-id="d87fd-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="d87fd-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="d87fd-129">Nowe — AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="d87fd-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="d87fd-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="d87fd-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


