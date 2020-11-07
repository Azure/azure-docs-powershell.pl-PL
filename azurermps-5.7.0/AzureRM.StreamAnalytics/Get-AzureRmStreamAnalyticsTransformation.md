---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: 9c92156f3fe739cd4f4285d536bd8a4c79cd3ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717296"
---
# <span data-ttu-id="eaa8a-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="eaa8a-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="eaa8a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eaa8a-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa8a-103">Pobiera informacje o transformacji zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaa8a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eaa8a-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaa8a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eaa8a-105">DESCRIPTION</span></span>
<span data-ttu-id="eaa8a-106">Polecenie cmdlet **Get-AzureRmStreamAnalyticsTransformation** pobiera informacje o transformacji zdefiniowanej w zadaniu Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="eaa8a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eaa8a-107">EXAMPLES</span></span>

### <span data-ttu-id="eaa8a-108">PRZYKŁAD 1: uzyskiwanie informacji o przekształceń analizy strumienia</span><span class="sxs-lookup"><span data-stu-id="eaa8a-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="eaa8a-109">To polecenie zwraca informacje o transformacji o nazwie StreamingJob w przypadku zadania o nazwie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="eaa8a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eaa8a-110">PARAMETERS</span></span>

### <span data-ttu-id="eaa8a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa8a-111">-DefaultProfile</span></span>
<span data-ttu-id="eaa8a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaa8a-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="eaa8a-113">-JobName</span></span>
<span data-ttu-id="eaa8a-114">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy transformacja analizy strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaa8a-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eaa8a-115">-Name</span></span>
<span data-ttu-id="eaa8a-116">Określa nazwę przekształcenia usługi Analiza strumienia Azure do pobrania.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaa8a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaa8a-117">-ResourceGroupName</span></span>
<span data-ttu-id="eaa8a-118">Określa nazwę grupy zasobów, do której należy transformacja analizy strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaa8a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa8a-119">CommonParameters</span></span>
<span data-ttu-id="eaa8a-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa8a-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaa8a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa8a-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eaa8a-122">INPUTS</span></span>

### <span data-ttu-id="eaa8a-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="eaa8a-123">None</span></span>
<span data-ttu-id="eaa8a-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="eaa8a-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eaa8a-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eaa8a-125">OUTPUTS</span></span>

### <span data-ttu-id="eaa8a-126">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. StreamAnalytics. MODELES. PSTransformation, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. modele. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="eaa8a-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="eaa8a-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eaa8a-127">NOTES</span></span>

## <span data-ttu-id="eaa8a-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eaa8a-128">RELATED LINKS</span></span>

[<span data-ttu-id="eaa8a-129">Nowe — AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="eaa8a-129">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


