---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: bc04c78538e808ce67813a3d706c35817102cfc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542135"
---
# <span data-ttu-id="dc287-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="dc287-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="dc287-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc287-102">SYNOPSIS</span></span>
<span data-ttu-id="dc287-103">Pobiera domyślną definicję funkcji w analizie strumienia.</span><span class="sxs-lookup"><span data-stu-id="dc287-103">Gets the default definition of a function in Stream Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc287-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc287-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc287-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dc287-105">DESCRIPTION</span></span>
<span data-ttu-id="dc287-106">Polecenie cmdlet **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** pobiera domyślną definicję funkcji w usłudze Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="dc287-106">The **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="dc287-107">Do tworzenia funkcji można użyć definicji domyślnej i polecenia cmdlet New-AzureRmStreamAnalyticsFunction.</span><span class="sxs-lookup"><span data-stu-id="dc287-107">You can use the default definition and the New-AzureRmStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="dc287-108">Możesz zmodyfikować definicję domyślną przed utworzeniem funkcji.</span><span class="sxs-lookup"><span data-stu-id="dc287-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="dc287-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc287-109">EXAMPLES</span></span>

### <span data-ttu-id="dc287-110">Przykład 1: uzyskiwanie domyślnej definicji funkcji Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="dc287-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="dc287-111">To polecenie pobiera domyślną definicję funkcji o nazwie ScoreTweet przy użyciu parametrów określonych w RetrieveDefaultDefinitionRequest.jsw pliku.</span><span class="sxs-lookup"><span data-stu-id="dc287-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="dc287-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc287-112">PARAMETERS</span></span>

### <span data-ttu-id="dc287-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc287-113">-DefaultProfile</span></span>
<span data-ttu-id="dc287-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc287-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc287-115">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="dc287-115">-File</span></span>
<span data-ttu-id="dc287-116">Określa ścieżkę pliku JSON zawierającego reprezentację treści żądania dla żądania pobrania definicji funkcji domyślnej (JSON).</span><span class="sxs-lookup"><span data-stu-id="dc287-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc287-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="dc287-117">-JobName</span></span>
<span data-ttu-id="dc287-118">Określa nazwę zadania Stream Analytics, do którego należą funkcje.</span><span class="sxs-lookup"><span data-stu-id="dc287-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="dc287-119">To polecenie cmdlet pobiera domyślną definicję funkcji w zadaniu, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="dc287-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="dc287-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dc287-120">-Name</span></span>
<span data-ttu-id="dc287-121">Określa nazwę funkcji Stream Analytics, dla której to polecenie cmdlet pobiera definicję domyślną.</span><span class="sxs-lookup"><span data-stu-id="dc287-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="dc287-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc287-122">-ResourceGroupName</span></span>
<span data-ttu-id="dc287-123">Określa nazwę grupy zasobów, do której należą funkcje funkcji Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="dc287-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="dc287-124">To polecenie cmdlet umożliwia pobieranie definicji funkcji dla grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="dc287-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dc287-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc287-125">CommonParameters</span></span>
<span data-ttu-id="dc287-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc287-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc287-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc287-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc287-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc287-128">INPUTS</span></span>

### <span data-ttu-id="dc287-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dc287-129">None</span></span>
<span data-ttu-id="dc287-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="dc287-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc287-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc287-131">OUTPUTS</span></span>

### <span data-ttu-id="dc287-132">Microsoft. Azure. Commands. StreamAnalytics. models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="dc287-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="dc287-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc287-133">NOTES</span></span>

## <span data-ttu-id="dc287-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc287-134">RELATED LINKS</span></span>

[<span data-ttu-id="dc287-135">Nowe — AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="dc287-135">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)


