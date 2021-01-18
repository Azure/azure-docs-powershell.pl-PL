---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 1d13d1b6e55831c972457c5a6a5aadc427ecb3a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503613"
---
# <span data-ttu-id="6a11f-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="6a11f-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="6a11f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a11f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a11f-103">Pobiera potok lub potok zadań z danymi w usłudze analiza danych.</span><span class="sxs-lookup"><span data-stu-id="6a11f-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="6a11f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a11f-104">SYNTAX</span></span>

### <span data-ttu-id="6a11f-105">GetAllInAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6a11f-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a11f-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="6a11f-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a11f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6a11f-107">DESCRIPTION</span></span>
<span data-ttu-id="6a11f-108">Usługa **Get-AzDataLakeAnalyticsJobPipeline** pobiera określone potoku pracy usługi Azure Data Lake Analytics lub listę rurociągów.</span><span class="sxs-lookup"><span data-stu-id="6a11f-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="6a11f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a11f-109">EXAMPLES</span></span>

### <span data-ttu-id="6a11f-110">Przykład 1: uzyskiwanie określonego rurociągu</span><span class="sxs-lookup"><span data-stu-id="6a11f-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="6a11f-111">To polecenie pobiera określoną potok z identyfikatorem "83cb7ad2-3523-4b82-b909-d478b0d8aea3" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="6a11f-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="6a11f-112">Przykład 2: Wyświetlanie listy wszystkich rurociągów na koncie</span><span class="sxs-lookup"><span data-stu-id="6a11f-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="6a11f-113">To polecenie pobiera listę wszystkich rurociągów na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="6a11f-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="6a11f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a11f-114">PARAMETERS</span></span>

### <span data-ttu-id="6a11f-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="6a11f-115">-Account</span></span>
<span data-ttu-id="6a11f-116">Nazwa konta usługi Data Lake Analytics, pod którą ma zostać pobrany potok zadań.</span><span class="sxs-lookup"><span data-stu-id="6a11f-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a11f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a11f-117">-DefaultProfile</span></span>
<span data-ttu-id="6a11f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6a11f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a11f-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="6a11f-119">-PipelineId</span></span>
<span data-ttu-id="6a11f-120">Identyfikator konkretnego potoku pracy, dla którego ma zostać zwrócona informacja.</span><span class="sxs-lookup"><span data-stu-id="6a11f-120">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a11f-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="6a11f-121">-SubmittedAfter</span></span>
<span data-ttu-id="6a11f-122">Opcjonalny filtr, który zwraca potok (y) wysłany tylko po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="6a11f-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a11f-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="6a11f-123">-SubmittedBefore</span></span>
<span data-ttu-id="6a11f-124">Opcjonalny filtr, który zwraca potoki zadań przesłane przed określoną godziną.</span><span class="sxs-lookup"><span data-stu-id="6a11f-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a11f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a11f-125">CommonParameters</span></span>
<span data-ttu-id="6a11f-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a11f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a11f-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a11f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a11f-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a11f-128">INPUTS</span></span>

### <span data-ttu-id="6a11f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6a11f-129">System.String</span></span>

### <span data-ttu-id="6a11f-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6a11f-130">System.Guid</span></span>

### <span data-ttu-id="6a11f-131">System. Nullable "1 [[System. DateTimeOffset, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6a11f-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6a11f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a11f-132">OUTPUTS</span></span>

### <span data-ttu-id="6a11f-133">Microsoft. Azure. Commands. DataLakeAnalytics. models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="6a11f-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="6a11f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a11f-134">NOTES</span></span>

## <span data-ttu-id="6a11f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a11f-135">RELATED LINKS</span></span>
