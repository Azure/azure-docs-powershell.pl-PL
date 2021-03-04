---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: f735dc3f213069c1ecf5bbae9d1d5cf24dda98a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955953"
---
# <span data-ttu-id="e0389-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e0389-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="e0389-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0389-102">SYNOPSIS</span></span>
<span data-ttu-id="e0389-103">Czeka na ukończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="e0389-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="e0389-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0389-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0389-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0389-105">DESCRIPTION</span></span>
<span data-ttu-id="e0389-106">Polecenie cmdlet **Wait-AzDataLakeAnalyticsJob** czeka na ukończenie zadania usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e0389-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="e0389-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0389-107">EXAMPLES</span></span>

### <span data-ttu-id="e0389-108">Przykład 1. Oczekiwanie na ukończenie zadania</span><span class="sxs-lookup"><span data-stu-id="e0389-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="e0389-109">Poniższe polecenie czeka na ukończenie zadania z określonym identyfikatorem.</span><span class="sxs-lookup"><span data-stu-id="e0389-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="e0389-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0389-110">PARAMETERS</span></span>

### <span data-ttu-id="e0389-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="e0389-111">-Account</span></span>
<span data-ttu-id="e0389-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e0389-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e0389-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0389-113">-DefaultProfile</span></span>
<span data-ttu-id="e0389-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e0389-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0389-115">- JobId</span><span class="sxs-lookup"><span data-stu-id="e0389-115">-JobId</span></span>
<span data-ttu-id="e0389-116">Określa identyfikator zadania, dla którego ma być oczekiwana.</span><span class="sxs-lookup"><span data-stu-id="e0389-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0389-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="e0389-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="e0389-118">Określa liczbę sekund oczekiwania przed zamknięciem operacji oczekiwania.</span><span class="sxs-lookup"><span data-stu-id="e0389-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0389-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e0389-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="e0389-120">Określ liczbę sekund, które upłyną między każdym sprawdzeniem stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="e0389-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0389-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0389-121">CommonParameters</span></span>
<span data-ttu-id="e0389-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0389-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0389-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0389-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0389-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0389-124">INPUTS</span></span>

### <span data-ttu-id="e0389-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e0389-125">System.String</span></span>

### <span data-ttu-id="e0389-126">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e0389-126">System.Guid</span></span>

### <span data-ttu-id="e0389-127">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e0389-127">System.Int32</span></span>

## <span data-ttu-id="e0389-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0389-128">OUTPUTS</span></span>

### <span data-ttu-id="e0389-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="e0389-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="e0389-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0389-130">NOTES</span></span>

## <span data-ttu-id="e0389-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0389-131">RELATED LINKS</span></span>

[<span data-ttu-id="e0389-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e0389-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="e0389-133">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e0389-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="e0389-134">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e0389-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)


