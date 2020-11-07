---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: ce933affbe3b99854f1ce907c968f35645c1d777
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872927"
---
# <span data-ttu-id="c35a0-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="c35a0-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="c35a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c35a0-102">SYNOPSIS</span></span>
<span data-ttu-id="c35a0-103">Pobiera informacje o transformacji zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="c35a0-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="c35a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c35a0-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c35a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c35a0-105">DESCRIPTION</span></span>
<span data-ttu-id="c35a0-106">Polecenie cmdlet **Get-AzStreamAnalyticsTransformation** pobiera informacje o transformacji zdefiniowanej w zadaniu Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="c35a0-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="c35a0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c35a0-107">EXAMPLES</span></span>

### <span data-ttu-id="c35a0-108">PRZYKŁAD 1: uzyskiwanie informacji o przekształceń analizy strumienia</span><span class="sxs-lookup"><span data-stu-id="c35a0-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="c35a0-109">To polecenie zwraca informacje o transformacji o nazwie StreamingJob w przypadku zadania o nazwie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="c35a0-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="c35a0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c35a0-110">PARAMETERS</span></span>

### <span data-ttu-id="c35a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c35a0-111">-DefaultProfile</span></span>
<span data-ttu-id="c35a0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c35a0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c35a0-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="c35a0-113">-JobName</span></span>
<span data-ttu-id="c35a0-114">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy transformacja analizy strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="c35a0-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="c35a0-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c35a0-115">-Name</span></span>
<span data-ttu-id="c35a0-116">Określa nazwę przekształcenia usługi Analiza strumienia Azure do pobrania.</span><span class="sxs-lookup"><span data-stu-id="c35a0-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="c35a0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c35a0-117">-ResourceGroupName</span></span>
<span data-ttu-id="c35a0-118">Określa nazwę grupy zasobów, do której należy transformacja analizy strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="c35a0-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="c35a0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c35a0-119">CommonParameters</span></span>
<span data-ttu-id="c35a0-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c35a0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c35a0-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c35a0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c35a0-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c35a0-122">INPUTS</span></span>

### <span data-ttu-id="c35a0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c35a0-123">System.String</span></span>

## <span data-ttu-id="c35a0-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c35a0-124">OUTPUTS</span></span>

### <span data-ttu-id="c35a0-125">Microsoft. Azure. Commands. StreamAnalytics. models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="c35a0-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="c35a0-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c35a0-126">NOTES</span></span>

## <span data-ttu-id="c35a0-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c35a0-127">RELATED LINKS</span></span>

[<span data-ttu-id="c35a0-128">Nowe — AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="c35a0-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


