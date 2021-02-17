---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182995"
---
# <span data-ttu-id="7c653-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="7c653-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="7c653-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c653-102">SYNOPSIS</span></span>
<span data-ttu-id="7c653-103">Pobiera informacje o przekształceniu zadania usługi Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7c653-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="7c653-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7c653-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c653-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7c653-105">DESCRIPTION</span></span>
<span data-ttu-id="7c653-106">Polecenie **cmdlet Get-AzStreamAnalyticsTransformation** pobiera informacje o przekształceniu zdefiniowanym w zadaniu analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="7c653-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="7c653-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7c653-107">EXAMPLES</span></span>

### <span data-ttu-id="7c653-108">PRZYKŁAD 1. Uzyskiwanie informacji o przekształceniu usługi Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="7c653-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="7c653-109">To polecenie zwraca informacje o przekształceniu o nazwie StreamingJob w zadaniu o nazwie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="7c653-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="7c653-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c653-110">PARAMETERS</span></span>

### <span data-ttu-id="7c653-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c653-111">-DefaultProfile</span></span>
<span data-ttu-id="7c653-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c653-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c653-113">— JobName</span><span class="sxs-lookup"><span data-stu-id="7c653-113">-JobName</span></span>
<span data-ttu-id="7c653-114">Określa nazwę zadania Azure Stream Analytics, do którego należy przekształcenie usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7c653-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="7c653-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7c653-115">-Name</span></span>
<span data-ttu-id="7c653-116">Określa nazwę przekształcenia usługi Azure Stream Analytics do pobrania.</span><span class="sxs-lookup"><span data-stu-id="7c653-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="7c653-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c653-117">-ResourceGroupName</span></span>
<span data-ttu-id="7c653-118">Określa nazwę grupy zasobów, do której należy transformacja usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7c653-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="7c653-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c653-119">CommonParameters</span></span>
<span data-ttu-id="7c653-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c653-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c653-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c653-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c653-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c653-122">INPUTS</span></span>

### <span data-ttu-id="7c653-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7c653-123">System.String</span></span>

## <span data-ttu-id="7c653-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7c653-124">OUTPUTS</span></span>

### <span data-ttu-id="7c653-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="7c653-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="7c653-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7c653-126">NOTES</span></span>

## <span data-ttu-id="7c653-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c653-127">RELATED LINKS</span></span>

[<span data-ttu-id="7c653-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="7c653-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


