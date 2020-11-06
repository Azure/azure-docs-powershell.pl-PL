---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/stop-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 956e263f402a3b6cb78631f8337d46fc1effdd98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544379"
---
# <span data-ttu-id="3c17c-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3c17c-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="3c17c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c17c-102">SYNOPSIS</span></span>
<span data-ttu-id="3c17c-103">Anuluje zadanie.</span><span class="sxs-lookup"><span data-stu-id="3c17c-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c17c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c17c-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c17c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3c17c-105">DESCRIPTION</span></span>
<span data-ttu-id="3c17c-106">Polecenie cmdlet **stop-AzureRmDataLakeAnalyticsJob** anuluje zadanie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3c17c-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="3c17c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c17c-107">EXAMPLES</span></span>

### <span data-ttu-id="3c17c-108">Przykład 1: Anulowanie zadania</span><span class="sxs-lookup"><span data-stu-id="3c17c-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="3c17c-109">To polecenie anuluje zadanie z określonym IDENTYFIKATORem.</span><span class="sxs-lookup"><span data-stu-id="3c17c-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="3c17c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c17c-110">PARAMETERS</span></span>

### <span data-ttu-id="3c17c-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="3c17c-111">-Account</span></span>
<span data-ttu-id="3c17c-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3c17c-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="3c17c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c17c-113">-DefaultProfile</span></span>
<span data-ttu-id="3c17c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3c17c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c17c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3c17c-115">-Force</span></span>
<span data-ttu-id="3c17c-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3c17c-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c17c-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="3c17c-117">-JobId</span></span>
<span data-ttu-id="3c17c-118">Określa identyfikator zadania, które ma zostać anulowane.</span><span class="sxs-lookup"><span data-stu-id="3c17c-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c17c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c17c-119">-PassThru</span></span>
<span data-ttu-id="3c17c-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3c17c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3c17c-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3c17c-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c17c-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c17c-122">-Confirm</span></span>
<span data-ttu-id="3c17c-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c17c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c17c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c17c-124">-WhatIf</span></span>
<span data-ttu-id="3c17c-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c17c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c17c-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3c17c-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c17c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c17c-127">CommonParameters</span></span>
<span data-ttu-id="3c17c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c17c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c17c-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c17c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c17c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c17c-130">INPUTS</span></span>

### <span data-ttu-id="3c17c-131">Wiodąc</span><span class="sxs-lookup"><span data-stu-id="3c17c-131">Guid</span></span>
<span data-ttu-id="3c17c-132">Parametr "JobId" akceptuje wartość typu "GUID" z procesu</span><span class="sxs-lookup"><span data-stu-id="3c17c-132">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="3c17c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c17c-133">OUTPUTS</span></span>

### <span data-ttu-id="3c17c-134">logiczną</span><span class="sxs-lookup"><span data-stu-id="3c17c-134">bool</span></span>
<span data-ttu-id="3c17c-135">Jeśli PassThru jest określony, zwraca wartość Prawda po wykonaniu operacji.</span><span class="sxs-lookup"><span data-stu-id="3c17c-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="3c17c-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c17c-136">NOTES</span></span>

## <span data-ttu-id="3c17c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c17c-137">RELATED LINKS</span></span>

[<span data-ttu-id="3c17c-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3c17c-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="3c17c-139">Prześlij — AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3c17c-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="3c17c-140">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3c17c-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


