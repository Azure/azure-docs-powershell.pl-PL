---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: f8cb65d1884cff247c5debcf347ab50bff0b6ce3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718930"
---
# <span data-ttu-id="c8b06-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="c8b06-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="c8b06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8b06-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b06-103">Pobiera potok lub potok zadań z danymi w usłudze analiza danych.</span><span class="sxs-lookup"><span data-stu-id="c8b06-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8b06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8b06-104">SYNTAX</span></span>

### <span data-ttu-id="c8b06-105">GetAllInAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c8b06-105">GetAllInAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8b06-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="c8b06-106">GetBySpecificJobPipeline</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8b06-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c8b06-107">DESCRIPTION</span></span>
<span data-ttu-id="c8b06-108">Usługa **Get-AzureRmDataLakeAnalyticsJobPipeline** pobiera określone potoku pracy usługi Azure Data Lake Analytics lub listę rurociągów.</span><span class="sxs-lookup"><span data-stu-id="c8b06-108">The **Get-AzureRmDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="c8b06-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8b06-109">EXAMPLES</span></span>

### <span data-ttu-id="c8b06-110">Przykład 1: uzyskiwanie określonego rurociągu</span><span class="sxs-lookup"><span data-stu-id="c8b06-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="c8b06-111">To polecenie pobiera określoną potok z identyfikatorem "83cb7ad2-3523-4b82-b909-d478b0d8aea3" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="c8b06-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="c8b06-112">Przykład 2: Wyświetlanie listy wszystkich rurociągów na koncie</span><span class="sxs-lookup"><span data-stu-id="c8b06-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="c8b06-113">To polecenie pobiera listę wszystkich rurociągów na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="c8b06-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="c8b06-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8b06-114">PARAMETERS</span></span>

### <span data-ttu-id="c8b06-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="c8b06-115">-Account</span></span>
<span data-ttu-id="c8b06-116">Nazwa konta usługi Data Lake Analytics, pod którą ma zostać pobrany potok zadań.</span><span class="sxs-lookup"><span data-stu-id="c8b06-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b06-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8b06-117">-DefaultProfile</span></span>
<span data-ttu-id="c8b06-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c8b06-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8b06-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="c8b06-119">-PipelineId</span></span>
<span data-ttu-id="c8b06-120">Identyfikator konkretnego potoku pracy, dla którego ma zostać zwrócona informacja.</span><span class="sxs-lookup"><span data-stu-id="c8b06-120">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b06-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="c8b06-121">-SubmittedAfter</span></span>
<span data-ttu-id="c8b06-122">Opcjonalny filtr, który zwraca potok (y) wysłany tylko po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="c8b06-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b06-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="c8b06-123">-SubmittedBefore</span></span>
<span data-ttu-id="c8b06-124">Opcjonalny filtr, który zwraca potoki zadań przesłane przed określoną godziną.</span><span class="sxs-lookup"><span data-stu-id="c8b06-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b06-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b06-125">CommonParameters</span></span>
<span data-ttu-id="c8b06-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8b06-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b06-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8b06-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b06-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8b06-128">INPUTS</span></span>

### <span data-ttu-id="c8b06-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c8b06-129">System.String</span></span>

### <span data-ttu-id="c8b06-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c8b06-130">System.Guid</span></span>

## <span data-ttu-id="c8b06-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8b06-131">OUTPUTS</span></span>

### <span data-ttu-id="c8b06-132">Microsoft. Azure. Commands. DataLakeAnalytics. models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="c8b06-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="c8b06-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8b06-133">NOTES</span></span>

## <span data-ttu-id="c8b06-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8b06-134">RELATED LINKS</span></span>

