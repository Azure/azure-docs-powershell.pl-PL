---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 1854c2e060dbbc83ba196043debb0ba08c9a933e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502692"
---
# <span data-ttu-id="20af3-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="20af3-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="20af3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20af3-102">SYNOPSIS</span></span>
<span data-ttu-id="20af3-103">Pobiera domyślną definicję funkcji w analizie strumienia.</span><span class="sxs-lookup"><span data-stu-id="20af3-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="20af3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20af3-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20af3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="20af3-105">DESCRIPTION</span></span>
<span data-ttu-id="20af3-106">Polecenie cmdlet **Get-AzStreamAnalyticsDefaultFunctionDefinition** pobiera domyślną definicję funkcji w usłudze Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="20af3-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="20af3-107">Do tworzenia funkcji można użyć definicji domyślnej i polecenia cmdlet New-AzStreamAnalyticsFunction.</span><span class="sxs-lookup"><span data-stu-id="20af3-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="20af3-108">Możesz zmodyfikować definicję domyślną przed utworzeniem funkcji.</span><span class="sxs-lookup"><span data-stu-id="20af3-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="20af3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20af3-109">EXAMPLES</span></span>

### <span data-ttu-id="20af3-110">Przykład 1: uzyskiwanie domyślnej definicji funkcji Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="20af3-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="20af3-111">To polecenie pobiera domyślną definicję funkcji o nazwie ScoreTweet przy użyciu parametrów określonych w RetrieveDefaultDefinitionRequest.jsw pliku.</span><span class="sxs-lookup"><span data-stu-id="20af3-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="20af3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20af3-112">PARAMETERS</span></span>

### <span data-ttu-id="20af3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20af3-113">-DefaultProfile</span></span>
<span data-ttu-id="20af3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20af3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20af3-115">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="20af3-115">-File</span></span>
<span data-ttu-id="20af3-116">Określa ścieżkę pliku JSON zawierającego reprezentację treści żądania dla żądania pobrania definicji funkcji domyślnej (JSON).</span><span class="sxs-lookup"><span data-stu-id="20af3-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20af3-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="20af3-117">-JobName</span></span>
<span data-ttu-id="20af3-118">Określa nazwę zadania Stream Analytics, do którego należą funkcje.</span><span class="sxs-lookup"><span data-stu-id="20af3-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="20af3-119">To polecenie cmdlet pobiera domyślną definicję funkcji w zadaniu, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="20af3-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="20af3-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="20af3-120">-Name</span></span>
<span data-ttu-id="20af3-121">Określa nazwę funkcji Stream Analytics, dla której to polecenie cmdlet pobiera definicję domyślną.</span><span class="sxs-lookup"><span data-stu-id="20af3-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="20af3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20af3-122">-ResourceGroupName</span></span>
<span data-ttu-id="20af3-123">Określa nazwę grupy zasobów, do której należą funkcje funkcji Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="20af3-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="20af3-124">To polecenie cmdlet umożliwia pobieranie definicji funkcji dla grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="20af3-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="20af3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20af3-125">CommonParameters</span></span>
<span data-ttu-id="20af3-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20af3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20af3-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20af3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20af3-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20af3-128">INPUTS</span></span>

### <span data-ttu-id="20af3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="20af3-129">System.String</span></span>

## <span data-ttu-id="20af3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20af3-130">OUTPUTS</span></span>

### <span data-ttu-id="20af3-131">Microsoft. Azure. Commands. StreamAnalytics. models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="20af3-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="20af3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20af3-132">NOTES</span></span>

## <span data-ttu-id="20af3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20af3-133">RELATED LINKS</span></span>

[<span data-ttu-id="20af3-134">Nowe — AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="20af3-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


