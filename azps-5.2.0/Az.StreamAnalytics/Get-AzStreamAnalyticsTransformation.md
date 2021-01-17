---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366410"
---
# <span data-ttu-id="9278f-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="9278f-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="9278f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9278f-102">SYNOPSIS</span></span>
<span data-ttu-id="9278f-103">Pobiera informacje o transformacji zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="9278f-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="9278f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9278f-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9278f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9278f-105">DESCRIPTION</span></span>
<span data-ttu-id="9278f-106">Polecenie cmdlet **Get-AzStreamAnalyticsTransformation** pobiera informacje o transformacji zdefiniowanej w zadaniu Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="9278f-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="9278f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9278f-107">EXAMPLES</span></span>

### <span data-ttu-id="9278f-108">PRZYKŁAD 1: uzyskiwanie informacji o przekształceń analizy strumienia</span><span class="sxs-lookup"><span data-stu-id="9278f-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="9278f-109">To polecenie zwraca informacje o transformacji o nazwie StreamingJob w przypadku zadania o nazwie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="9278f-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="9278f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9278f-110">PARAMETERS</span></span>

### <span data-ttu-id="9278f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9278f-111">-DefaultProfile</span></span>
<span data-ttu-id="9278f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9278f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9278f-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="9278f-113">-JobName</span></span>
<span data-ttu-id="9278f-114">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy transformacja analizy strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="9278f-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="9278f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9278f-115">-Name</span></span>
<span data-ttu-id="9278f-116">Określa nazwę przekształcenia usługi Analiza strumienia Azure do pobrania.</span><span class="sxs-lookup"><span data-stu-id="9278f-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="9278f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9278f-117">-ResourceGroupName</span></span>
<span data-ttu-id="9278f-118">Określa nazwę grupy zasobów, do której należy transformacja analizy strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="9278f-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="9278f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9278f-119">CommonParameters</span></span>
<span data-ttu-id="9278f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9278f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9278f-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9278f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9278f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9278f-122">INPUTS</span></span>

### <span data-ttu-id="9278f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9278f-123">System.String</span></span>

## <span data-ttu-id="9278f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9278f-124">OUTPUTS</span></span>

### <span data-ttu-id="9278f-125">Microsoft. Azure. Commands. StreamAnalytics. models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="9278f-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="9278f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9278f-126">NOTES</span></span>

## <span data-ttu-id="9278f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9278f-127">RELATED LINKS</span></span>

[<span data-ttu-id="9278f-128">Nowe — AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="9278f-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


