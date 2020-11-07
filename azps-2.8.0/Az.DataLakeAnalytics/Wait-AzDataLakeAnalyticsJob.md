---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 3d112a39afc522914e31acbc8c5539a45175fd81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705845"
---
# <span data-ttu-id="70b03-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="70b03-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="70b03-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70b03-102">SYNOPSIS</span></span>
<span data-ttu-id="70b03-103">Oczekuje na ukończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="70b03-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="70b03-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70b03-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70b03-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70b03-105">DESCRIPTION</span></span>
<span data-ttu-id="70b03-106">Polecenie cmdlet **wait-AzDataLakeAnalyticsJob** oczekuje na ukończenie zadania usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="70b03-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="70b03-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70b03-107">EXAMPLES</span></span>

### <span data-ttu-id="70b03-108">Przykład 1. oczekiwanie na ukończenie zadania</span><span class="sxs-lookup"><span data-stu-id="70b03-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="70b03-109">Poniższe polecenie czeka na zakończenie zadania o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="70b03-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="70b03-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70b03-110">PARAMETERS</span></span>

### <span data-ttu-id="70b03-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="70b03-111">-Account</span></span>
<span data-ttu-id="70b03-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="70b03-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="70b03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70b03-113">-DefaultProfile</span></span>
<span data-ttu-id="70b03-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="70b03-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70b03-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="70b03-115">-JobId</span></span>
<span data-ttu-id="70b03-116">Określa identyfikator zadania, do którego należy czekać.</span><span class="sxs-lookup"><span data-stu-id="70b03-116">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="70b03-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="70b03-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="70b03-118">Określa liczbę sekund określającą czas oczekiwania przed zakończeniem operacji oczekiwania.</span><span class="sxs-lookup"><span data-stu-id="70b03-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

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

### <span data-ttu-id="70b03-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="70b03-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="70b03-120">Określ liczbę sekund, które powinny upłynąć między kolejnymi sprawdzeniami stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="70b03-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

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

### <span data-ttu-id="70b03-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b03-121">CommonParameters</span></span>
<span data-ttu-id="70b03-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70b03-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b03-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70b03-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b03-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70b03-124">INPUTS</span></span>

### <span data-ttu-id="70b03-125">System. String</span><span class="sxs-lookup"><span data-stu-id="70b03-125">System.String</span></span>

### <span data-ttu-id="70b03-126">System. GUID</span><span class="sxs-lookup"><span data-stu-id="70b03-126">System.Guid</span></span>

### <span data-ttu-id="70b03-127">System. Int32</span><span class="sxs-lookup"><span data-stu-id="70b03-127">System.Int32</span></span>

## <span data-ttu-id="70b03-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70b03-128">OUTPUTS</span></span>

### <span data-ttu-id="70b03-129">Microsoft. Azure. Management. datalake. Analytics. modele. JobInformation</span><span class="sxs-lookup"><span data-stu-id="70b03-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="70b03-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70b03-130">NOTES</span></span>

## <span data-ttu-id="70b03-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70b03-131">RELATED LINKS</span></span>

[<span data-ttu-id="70b03-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="70b03-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="70b03-133">Zatrzymaj — AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="70b03-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="70b03-134">Prześlij — AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="70b03-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

