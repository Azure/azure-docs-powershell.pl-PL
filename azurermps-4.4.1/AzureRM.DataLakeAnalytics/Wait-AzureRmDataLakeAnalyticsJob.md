---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 672a992dd86fcbd95e17f0795147231b1b62cd5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718233"
---
# <span data-ttu-id="27791-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="27791-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="27791-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27791-102">SYNOPSIS</span></span>
<span data-ttu-id="27791-103">Oczekuje na ukończenie zadania.</span><span class="sxs-lookup"><span data-stu-id="27791-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27791-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27791-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27791-105">Opis</span><span class="sxs-lookup"><span data-stu-id="27791-105">DESCRIPTION</span></span>
<span data-ttu-id="27791-106">Polecenie cmdlet **wait-AzureRmDataLakeAnalyticsJob** oczekuje na ukończenie zadania usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="27791-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="27791-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27791-107">EXAMPLES</span></span>

### <span data-ttu-id="27791-108">Przykład 1. oczekiwanie na ukończenie zadania</span><span class="sxs-lookup"><span data-stu-id="27791-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="27791-109">Poniższe polecenie czeka na zakończenie zadania o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="27791-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="27791-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27791-110">PARAMETERS</span></span>

### <span data-ttu-id="27791-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="27791-111">-Account</span></span>
<span data-ttu-id="27791-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="27791-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="27791-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="27791-113">-JobId</span></span>
<span data-ttu-id="27791-114">Określa identyfikator zadania, do którego należy czekać.</span><span class="sxs-lookup"><span data-stu-id="27791-114">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="27791-115">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="27791-115">-TimeoutInSeconds</span></span>
<span data-ttu-id="27791-116">Określa liczbę sekund określającą czas oczekiwania przed zakończeniem operacji oczekiwania.</span><span class="sxs-lookup"><span data-stu-id="27791-116">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

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

### <span data-ttu-id="27791-117">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="27791-117">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="27791-118">Określ liczbę sekund, które powinny upłynąć między kolejnymi sprawdzeniami stanu zadania.</span><span class="sxs-lookup"><span data-stu-id="27791-118">Specify the number of seconds that elapse between each check of the job state.</span></span>

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

### <span data-ttu-id="27791-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27791-119">-DefaultProfile</span></span>
<span data-ttu-id="27791-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="27791-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27791-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27791-121">CommonParameters</span></span>
<span data-ttu-id="27791-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27791-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27791-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27791-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27791-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27791-124">INPUTS</span></span>

### <span data-ttu-id="27791-125">Wiodąc</span><span class="sxs-lookup"><span data-stu-id="27791-125">Guid</span></span>
<span data-ttu-id="27791-126">Parametr "JobId" akceptuje wartość typu "GUID" z procesu</span><span class="sxs-lookup"><span data-stu-id="27791-126">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="27791-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27791-127">OUTPUTS</span></span>

### <span data-ttu-id="27791-128">JobInformation</span><span class="sxs-lookup"><span data-stu-id="27791-128">JobInformation</span></span>
<span data-ttu-id="27791-129">Ostatnie szczegóły zadania dla ukończonego zadania.</span><span class="sxs-lookup"><span data-stu-id="27791-129">The final job details for the completed job.</span></span>

## <span data-ttu-id="27791-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27791-130">NOTES</span></span>

## <span data-ttu-id="27791-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27791-131">RELATED LINKS</span></span>

[<span data-ttu-id="27791-132">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="27791-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="27791-133">Zatrzymaj — AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="27791-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="27791-134">Prześlij — AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="27791-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


