---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 9e925e1bd118a9ac5f676ee666cb945f22d1ffac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988275"
---
# <span data-ttu-id="d94f0-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="d94f0-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="d94f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d94f0-102">SYNOPSIS</span></span>
<span data-ttu-id="d94f0-103">Pobiera potok zadania lub potoki zadania usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d94f0-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="d94f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d94f0-104">SYNTAX</span></span>

### <span data-ttu-id="d94f0-105">GetAllInAccount (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d94f0-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d94f0-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="d94f0-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d94f0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d94f0-107">DESCRIPTION</span></span>
<span data-ttu-id="d94f0-108">Narzędzie **Get-AzDataLakeAnalyticsJobPipeline** pobiera określony potok zadania usługi Azure Data Lake Analytics lub listę potoków.</span><span class="sxs-lookup"><span data-stu-id="d94f0-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="d94f0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d94f0-109">EXAMPLES</span></span>

### <span data-ttu-id="d94f0-110">Przykład 1. Uzyskiwanie określonego potoku</span><span class="sxs-lookup"><span data-stu-id="d94f0-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="d94f0-111">To polecenie pobiera określony potok o identyfikatorze "83cb7ad2-3523-4b82-b909-d478b0d8aea3" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="d94f0-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="d94f0-112">Przykład 2. Uzyskiwanie listy wszystkich potoków na koncie</span><span class="sxs-lookup"><span data-stu-id="d94f0-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="d94f0-113">To polecenie pobiera listę wszystkich potoków na koncie "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="d94f0-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="d94f0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d94f0-114">PARAMETERS</span></span>

### <span data-ttu-id="d94f0-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="d94f0-115">-Account</span></span>
<span data-ttu-id="d94f0-116">Nazwa konta usługi Data Lake Analytics, pod którą chcesz pobrać potok zadania.</span><span class="sxs-lookup"><span data-stu-id="d94f0-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="d94f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d94f0-117">-DefaultProfile</span></span>
<span data-ttu-id="d94f0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d94f0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d94f0-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="d94f0-119">-PipelineId</span></span>
<span data-ttu-id="d94f0-120">Identyfikator określonego potoku zadania, dla których mają być zwracane informacje.</span><span class="sxs-lookup"><span data-stu-id="d94f0-120">ID of the specific job pipeline to return information for.</span></span>

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

### <span data-ttu-id="d94f0-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="d94f0-121">-SubmittedAfter</span></span>
<span data-ttu-id="d94f0-122">Filtr opcjonalny, który zwraca potoki zadań przesłane tylko po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="d94f0-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="d94f0-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="d94f0-123">-SubmittedBefore</span></span>
<span data-ttu-id="d94f0-124">Filtr opcjonalny, który zwraca potoki zadań przesłane tylko przed określonym czasem.</span><span class="sxs-lookup"><span data-stu-id="d94f0-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="d94f0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94f0-125">CommonParameters</span></span>
<span data-ttu-id="d94f0-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d94f0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94f0-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d94f0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94f0-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d94f0-128">INPUTS</span></span>

### <span data-ttu-id="d94f0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d94f0-129">System.String</span></span>

### <span data-ttu-id="d94f0-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d94f0-130">System.Guid</span></span>

### <span data-ttu-id="d94f0-131">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d94f0-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d94f0-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d94f0-132">OUTPUTS</span></span>

### <span data-ttu-id="d94f0-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="d94f0-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="d94f0-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d94f0-134">NOTES</span></span>

## <span data-ttu-id="d94f0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d94f0-135">RELATED LINKS</span></span>
