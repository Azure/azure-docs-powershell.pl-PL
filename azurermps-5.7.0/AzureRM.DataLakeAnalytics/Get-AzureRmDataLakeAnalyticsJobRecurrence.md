---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: 34d2921526f54e20697a11cf17708fef50e49fc2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542667"
---
# <span data-ttu-id="c5acb-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="c5acb-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="c5acb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5acb-102">SYNOPSIS</span></span>
<span data-ttu-id="c5acb-103">Pobiera cykl lub cykl zadania Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c5acb-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5acb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5acb-104">SYNTAX</span></span>

### <span data-ttu-id="c5acb-105">GetAllInAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c5acb-105">GetAllInAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5acb-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="c5acb-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5acb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c5acb-107">DESCRIPTION</span></span>
<span data-ttu-id="c5acb-108">**Element get-AzureRmDataLakeAnalyticsJobRecurrence** Pobiera określony cykl zadania usługi Azure Data Lake Analytics lub listę cykli.</span><span class="sxs-lookup"><span data-stu-id="c5acb-108">The **Get-AzureRmDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="c5acb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5acb-109">EXAMPLES</span></span>

### <span data-ttu-id="c5acb-110">Przykład 1: uzyskiwanie określonego cyklu</span><span class="sxs-lookup"><span data-stu-id="c5acb-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="c5acb-111">To polecenie pobiera określony cykl zadania o identyfikatorze "83cb7ad2-3523-4b82-b909-d478b0d8aea3" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="c5acb-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="c5acb-112">Przykład 2: Pobieranie listy wszystkich cykli na koncie</span><span class="sxs-lookup"><span data-stu-id="c5acb-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="c5acb-113">To polecenie pobiera listę wszystkich cykli na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="c5acb-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="c5acb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5acb-114">PARAMETERS</span></span>

### <span data-ttu-id="c5acb-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="c5acb-115">-Account</span></span>
<span data-ttu-id="c5acb-116">Nazwa konta usługi Data Lake Analytics, pod którą ma być pobierany cykl zadania.</span><span class="sxs-lookup"><span data-stu-id="c5acb-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="c5acb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5acb-117">-DefaultProfile</span></span>
<span data-ttu-id="c5acb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c5acb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5acb-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="c5acb-119">-RecurrenceId</span></span>
<span data-ttu-id="c5acb-120">Identyfikator określonego cyklu zadania, dla którego ma zostać zwrócona informacja.</span><span class="sxs-lookup"><span data-stu-id="c5acb-120">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5acb-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="c5acb-121">-SubmittedAfter</span></span>
<span data-ttu-id="c5acb-122">Opcjonalny filtr, który zwraca cykl zadania, tylko przesłany po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="c5acb-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="c5acb-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="c5acb-123">-SubmittedBefore</span></span>
<span data-ttu-id="c5acb-124">Opcjonalny filtr, który zwraca tylko cykl zadania, przed określoną godziną.</span><span class="sxs-lookup"><span data-stu-id="c5acb-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="c5acb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5acb-125">CommonParameters</span></span>
<span data-ttu-id="c5acb-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5acb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5acb-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5acb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5acb-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5acb-128">INPUTS</span></span>

### <span data-ttu-id="c5acb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c5acb-129">System.String</span></span>
<span data-ttu-id="c5acb-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c5acb-130">System.Guid</span></span>

## <span data-ttu-id="c5acb-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5acb-131">OUTPUTS</span></span>

### <span data-ttu-id="c5acb-132">Microsoft. Azure. Commands. DataLakeAnalytics. models. PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="c5acb-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="c5acb-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5acb-133">NOTES</span></span>

## <span data-ttu-id="c5acb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5acb-134">RELATED LINKS</span></span>

