---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: 09cf95f6fd7feb17053063952ae7110098353c86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002177"
---
# <span data-ttu-id="14f53-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="14f53-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="14f53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14f53-102">SYNOPSIS</span></span>
<span data-ttu-id="14f53-103">Sprawdza stan połączenia danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="14f53-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="14f53-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14f53-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14f53-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="14f53-105">DESCRIPTION</span></span>
<span data-ttu-id="14f53-106">Polecenie **cmdlet Test-AzStreamAnalyticsInput** sprawdza możliwość łączenia się z elementami wejściowymi przez usługę Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="14f53-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="14f53-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14f53-107">EXAMPLES</span></span>

### <span data-ttu-id="14f53-108">Przykład 1. Testowanie stanu połączenia strumienia wejściowego</span><span class="sxs-lookup"><span data-stu-id="14f53-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="14f53-109">To sprawdza stan połączenia wejściowego strumienia Danych Wejściowych w transmisję strumieniową StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="14f53-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="14f53-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14f53-110">PARAMETERS</span></span>

### <span data-ttu-id="14f53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f53-111">-DefaultProfile</span></span>
<span data-ttu-id="14f53-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="14f53-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14f53-113">— JobName</span><span class="sxs-lookup"><span data-stu-id="14f53-113">-JobName</span></span>
<span data-ttu-id="14f53-114">Określa nazwę zadania Azure Stream Analytics, do którego należy dane wejściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="14f53-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="14f53-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="14f53-115">-Name</span></span>
<span data-ttu-id="14f53-116">Określa nazwę danych wejściowych usługi Azure Stream Analytics do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="14f53-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="14f53-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14f53-117">-ResourceGroupName</span></span>
<span data-ttu-id="14f53-118">Określa nazwę grupy zasobów, do której należy dane wejściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="14f53-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="14f53-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f53-119">CommonParameters</span></span>
<span data-ttu-id="14f53-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14f53-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f53-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14f53-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f53-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14f53-122">INPUTS</span></span>

### <span data-ttu-id="14f53-123">System.String</span><span class="sxs-lookup"><span data-stu-id="14f53-123">System.String</span></span>

## <span data-ttu-id="14f53-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14f53-124">OUTPUTS</span></span>

### <span data-ttu-id="14f53-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="14f53-125">System.Boolean</span></span>

## <span data-ttu-id="14f53-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14f53-126">NOTES</span></span>

## <span data-ttu-id="14f53-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14f53-127">RELATED LINKS</span></span>

[<span data-ttu-id="14f53-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="14f53-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="14f53-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="14f53-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="14f53-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="14f53-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


