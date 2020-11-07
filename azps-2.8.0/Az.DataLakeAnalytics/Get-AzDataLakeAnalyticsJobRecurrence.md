---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: ba6cff5c2618754caa35efbaa7345c24b1f25a3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705885"
---
# <span data-ttu-id="3e1f4-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="3e1f4-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="3e1f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e1f4-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1f4-103">Pobiera cykl lub cykl zadania Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="3e1f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e1f4-104">SYNTAX</span></span>

### <span data-ttu-id="3e1f4-105">GetAllInAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e1f4-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e1f4-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="3e1f4-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e1f4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3e1f4-107">DESCRIPTION</span></span>
<span data-ttu-id="3e1f4-108">**Element get-AzDataLakeAnalyticsJobRecurrence** Pobiera określony cykl zadania usługi Azure Data Lake Analytics lub listę cykli.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="3e1f4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e1f4-109">EXAMPLES</span></span>

### <span data-ttu-id="3e1f4-110">Przykład 1: uzyskiwanie określonego cyklu</span><span class="sxs-lookup"><span data-stu-id="3e1f4-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="3e1f4-111">To polecenie pobiera określony cykl zadania o identyfikatorze "83cb7ad2-3523-4b82-b909-d478b0d8aea3" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="3e1f4-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="3e1f4-112">Przykład 2: Pobieranie listy wszystkich cykli na koncie</span><span class="sxs-lookup"><span data-stu-id="3e1f4-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="3e1f4-113">To polecenie pobiera listę wszystkich cykli na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="3e1f4-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="3e1f4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e1f4-114">PARAMETERS</span></span>

### <span data-ttu-id="3e1f4-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="3e1f4-115">-Account</span></span>
<span data-ttu-id="3e1f4-116">Nazwa konta usługi Data Lake Analytics, pod którą ma być pobierany cykl zadania.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="3e1f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1f4-117">-DefaultProfile</span></span>
<span data-ttu-id="3e1f4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3e1f4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e1f4-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="3e1f4-119">-RecurrenceId</span></span>
<span data-ttu-id="3e1f4-120">Identyfikator określonego cyklu zadania, dla którego ma zostać zwrócona informacja.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-120">ID of the specific job recurrence to return information for.</span></span>

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

### <span data-ttu-id="3e1f4-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="3e1f4-121">-SubmittedAfter</span></span>
<span data-ttu-id="3e1f4-122">Opcjonalny filtr, który zwraca cykl zadania, tylko przesłany po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="3e1f4-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="3e1f4-123">-SubmittedBefore</span></span>
<span data-ttu-id="3e1f4-124">Opcjonalny filtr, który zwraca tylko cykl zadania, przed określoną godziną.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="3e1f4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1f4-125">CommonParameters</span></span>
<span data-ttu-id="3e1f4-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e1f4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1f4-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e1f4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1f4-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e1f4-128">INPUTS</span></span>

### <span data-ttu-id="3e1f4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3e1f4-129">System.String</span></span>

### <span data-ttu-id="3e1f4-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3e1f4-130">System.Guid</span></span>

### <span data-ttu-id="3e1f4-131">System. Nullable "1 [[System. DateTimeOffset, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3e1f4-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3e1f4-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e1f4-132">OUTPUTS</span></span>

### <span data-ttu-id="3e1f4-133">Microsoft. Azure. Commands. DataLakeAnalytics. models. PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="3e1f4-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="3e1f4-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e1f4-134">NOTES</span></span>

## <span data-ttu-id="3e1f4-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e1f4-135">RELATED LINKS</span></span>
