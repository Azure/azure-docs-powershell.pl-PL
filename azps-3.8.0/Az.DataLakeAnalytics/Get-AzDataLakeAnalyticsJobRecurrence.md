---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: d571eb887069aa5c28029dfa98ab022c1d82fc88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049812"
---
# <span data-ttu-id="12e5a-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="12e5a-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="12e5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="12e5a-103">Pobiera cykl lub cykl zadania Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="12e5a-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="12e5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12e5a-104">SYNTAX</span></span>

### <span data-ttu-id="12e5a-105">GetAllInAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="12e5a-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12e5a-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="12e5a-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12e5a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="12e5a-107">DESCRIPTION</span></span>
<span data-ttu-id="12e5a-108">**Element get-AzDataLakeAnalyticsJobRecurrence** Pobiera określony cykl zadania usługi Azure Data Lake Analytics lub listę cykli.</span><span class="sxs-lookup"><span data-stu-id="12e5a-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="12e5a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12e5a-109">EXAMPLES</span></span>

### <span data-ttu-id="12e5a-110">Przykład 1: uzyskiwanie określonego cyklu</span><span class="sxs-lookup"><span data-stu-id="12e5a-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="12e5a-111">To polecenie pobiera określony cykl zadania o identyfikatorze "83cb7ad2-3523-4b82-b909-d478b0d8aea3" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="12e5a-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="12e5a-112">Przykład 2: Pobieranie listy wszystkich cykli na koncie</span><span class="sxs-lookup"><span data-stu-id="12e5a-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="12e5a-113">To polecenie pobiera listę wszystkich cykli na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="12e5a-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="12e5a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12e5a-114">PARAMETERS</span></span>

### <span data-ttu-id="12e5a-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="12e5a-115">-Account</span></span>
<span data-ttu-id="12e5a-116">Nazwa konta usługi Data Lake Analytics, pod którą ma być pobierany cykl zadania.</span><span class="sxs-lookup"><span data-stu-id="12e5a-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="12e5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e5a-117">-DefaultProfile</span></span>
<span data-ttu-id="12e5a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="12e5a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12e5a-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="12e5a-119">-RecurrenceId</span></span>
<span data-ttu-id="12e5a-120">Identyfikator określonego cyklu zadania, dla którego ma zostać zwrócona informacja.</span><span class="sxs-lookup"><span data-stu-id="12e5a-120">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12e5a-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="12e5a-121">-SubmittedAfter</span></span>
<span data-ttu-id="12e5a-122">Opcjonalny filtr, który zwraca cykl zadania, tylko przesłany po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="12e5a-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="12e5a-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="12e5a-123">-SubmittedBefore</span></span>
<span data-ttu-id="12e5a-124">Opcjonalny filtr, który zwraca tylko cykl zadania, przed określoną godziną.</span><span class="sxs-lookup"><span data-stu-id="12e5a-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="12e5a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e5a-125">CommonParameters</span></span>
<span data-ttu-id="12e5a-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e5a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e5a-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12e5a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e5a-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12e5a-128">INPUTS</span></span>

### <span data-ttu-id="12e5a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="12e5a-129">System.String</span></span>

### <span data-ttu-id="12e5a-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="12e5a-130">System.Guid</span></span>

### <span data-ttu-id="12e5a-131">System. Nullable "1 [[System. DateTimeOffset, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="12e5a-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="12e5a-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12e5a-132">OUTPUTS</span></span>

### <span data-ttu-id="12e5a-133">Microsoft. Azure. Commands. DataLakeAnalytics. models. PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="12e5a-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="12e5a-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12e5a-134">NOTES</span></span>

## <span data-ttu-id="12e5a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12e5a-135">RELATED LINKS</span></span>
