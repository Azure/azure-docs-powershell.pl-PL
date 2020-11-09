---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 1d13d1b6e55831c972457c5a6a5aadc427ecb3a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305833"
---
# <span data-ttu-id="df5af-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="df5af-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="df5af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df5af-102">SYNOPSIS</span></span>
<span data-ttu-id="df5af-103">Pobiera potok lub potok zadań z danymi w usłudze analiza danych.</span><span class="sxs-lookup"><span data-stu-id="df5af-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="df5af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df5af-104">SYNTAX</span></span>

### <span data-ttu-id="df5af-105">GetAllInAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df5af-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df5af-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="df5af-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df5af-107">Opis</span><span class="sxs-lookup"><span data-stu-id="df5af-107">DESCRIPTION</span></span>
<span data-ttu-id="df5af-108">Usługa **Get-AzDataLakeAnalyticsJobPipeline** pobiera określone potoku pracy usługi Azure Data Lake Analytics lub listę rurociągów.</span><span class="sxs-lookup"><span data-stu-id="df5af-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="df5af-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df5af-109">EXAMPLES</span></span>

### <span data-ttu-id="df5af-110">Przykład 1: uzyskiwanie określonego rurociągu</span><span class="sxs-lookup"><span data-stu-id="df5af-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="df5af-111">To polecenie pobiera określoną potok z identyfikatorem "83cb7ad2-3523-4b82-b909-d478b0d8aea3" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="df5af-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="df5af-112">Przykład 2: Wyświetlanie listy wszystkich rurociągów na koncie</span><span class="sxs-lookup"><span data-stu-id="df5af-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="df5af-113">To polecenie pobiera listę wszystkich rurociągów na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="df5af-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="df5af-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df5af-114">PARAMETERS</span></span>

### <span data-ttu-id="df5af-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="df5af-115">-Account</span></span>
<span data-ttu-id="df5af-116">Nazwa konta usługi Data Lake Analytics, pod którą ma zostać pobrany potok zadań.</span><span class="sxs-lookup"><span data-stu-id="df5af-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="df5af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5af-117">-DefaultProfile</span></span>
<span data-ttu-id="df5af-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="df5af-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df5af-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="df5af-119">-PipelineId</span></span>
<span data-ttu-id="df5af-120">Identyfikator konkretnego potoku pracy, dla którego ma zostać zwrócona informacja.</span><span class="sxs-lookup"><span data-stu-id="df5af-120">ID of the specific job pipeline to return information for.</span></span>

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

### <span data-ttu-id="df5af-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="df5af-121">-SubmittedAfter</span></span>
<span data-ttu-id="df5af-122">Opcjonalny filtr, który zwraca potok (y) wysłany tylko po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="df5af-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="df5af-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="df5af-123">-SubmittedBefore</span></span>
<span data-ttu-id="df5af-124">Opcjonalny filtr, który zwraca potoki zadań przesłane przed określoną godziną.</span><span class="sxs-lookup"><span data-stu-id="df5af-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="df5af-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5af-125">CommonParameters</span></span>
<span data-ttu-id="df5af-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df5af-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5af-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df5af-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5af-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df5af-128">INPUTS</span></span>

### <span data-ttu-id="df5af-129">System. String</span><span class="sxs-lookup"><span data-stu-id="df5af-129">System.String</span></span>

### <span data-ttu-id="df5af-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="df5af-130">System.Guid</span></span>

### <span data-ttu-id="df5af-131">System. Nullable "1 [[System. DateTimeOffset, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="df5af-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="df5af-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df5af-132">OUTPUTS</span></span>

### <span data-ttu-id="df5af-133">Microsoft. Azure. Commands. DataLakeAnalytics. models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="df5af-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="df5af-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df5af-134">NOTES</span></span>

## <span data-ttu-id="df5af-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df5af-135">RELATED LINKS</span></span>
