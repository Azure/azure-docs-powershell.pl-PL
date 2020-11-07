---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: d0357e06257ad1df97b47ea7be59a1797e0f6902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717554"
---
# <span data-ttu-id="382aa-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="382aa-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="382aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="382aa-102">SYNOPSIS</span></span>
<span data-ttu-id="382aa-103">Testuje stan połączenia wejściowego.</span><span class="sxs-lookup"><span data-stu-id="382aa-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="382aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="382aa-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="382aa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="382aa-105">DESCRIPTION</span></span>
<span data-ttu-id="382aa-106">Polecenie cmdlet **test-AzureRmStreamAnalyticsInput** testuje zdolność analizy strumienia do nawiązywania połączenia z danymi wejściowymi.</span><span class="sxs-lookup"><span data-stu-id="382aa-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="382aa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="382aa-107">EXAMPLES</span></span>

### <span data-ttu-id="382aa-108">PRZYKŁAD 1: testowanie stanu połączenia strumienia wejściowego</span><span class="sxs-lookup"><span data-stu-id="382aa-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="382aa-109">To testuje stan połączenia w EntryStream wejściowym in StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="382aa-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="382aa-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="382aa-110">PARAMETERS</span></span>

### <span data-ttu-id="382aa-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="382aa-111">-JobName</span></span>
<span data-ttu-id="382aa-112">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="382aa-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="382aa-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="382aa-113">-Name</span></span>
<span data-ttu-id="382aa-114">Określa nazwę danych wejściowych funkcji Analiza strumienia Azure do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="382aa-114">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="382aa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="382aa-115">-ResourceGroupName</span></span>
<span data-ttu-id="382aa-116">Określa nazwę grupy zasobów, do której należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="382aa-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="382aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="382aa-117">-DefaultProfile</span></span>
<span data-ttu-id="382aa-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="382aa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="382aa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="382aa-119">CommonParameters</span></span>
<span data-ttu-id="382aa-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="382aa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="382aa-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="382aa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="382aa-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="382aa-122">INPUTS</span></span>

## <span data-ttu-id="382aa-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="382aa-123">OUTPUTS</span></span>

### <span data-ttu-id="382aa-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="382aa-124">System.Object</span></span>

## <span data-ttu-id="382aa-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="382aa-125">NOTES</span></span>

## <span data-ttu-id="382aa-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="382aa-126">RELATED LINKS</span></span>

[<span data-ttu-id="382aa-127">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="382aa-127">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="382aa-128">Nowe — AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="382aa-128">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="382aa-129">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="382aa-129">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


