---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1C18EE5D-A916-4776-ABAE-A7B24FA74108
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf97dd5958eb2e1fdd9790355ac0236974c0db7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054624"
---
# <span data-ttu-id="e7364-101">Get-AzureAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="e7364-101">Get-AzureAutomationJobOutput</span></span>

## <span data-ttu-id="e7364-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7364-102">SYNOPSIS</span></span>

<span data-ttu-id="e7364-103">Pobiera dane wyjściowe zadania usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e7364-103">Gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="e7364-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7364-104">SYNTAX</span></span>

```
Get-AzureAutomationJobOutput -Id <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e7364-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e7364-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e7364-106">Polecenie cmdlet **Get-AzureAutomationJobOutput** pobiera dane wyjściowe zadania automatyzacji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e7364-106">The **Get-AzureAutomationJobOutput** cmdlet gets the output of a Microsoft Azure Automation job.</span></span>

## <span data-ttu-id="e7364-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7364-107">EXAMPLES</span></span>

### <span data-ttu-id="e7364-108">Przykład 1. Pobieranie danych wyjściowych zadania usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="e7364-108">Example 1: Get the output of an Azure Automation job</span></span>
```
PS C:\> Get-AzureAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -Stream "Any"
```

<span data-ttu-id="e7364-109">To polecenie pobiera wszystkie dane wyjściowe zadania o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="e7364-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="e7364-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7364-110">PARAMETERS</span></span>

### <span data-ttu-id="e7364-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e7364-111">-AutomationAccountName</span></span>
<span data-ttu-id="e7364-112">Określa nazwę konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e7364-112">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7364-113">-ID</span><span class="sxs-lookup"><span data-stu-id="e7364-113">-Id</span></span>
<span data-ttu-id="e7364-114">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="e7364-114">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7364-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="e7364-115">-Profile</span></span>
<span data-ttu-id="e7364-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7364-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7364-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e7364-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7364-118">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e7364-118">-StartTime</span></span>
<span data-ttu-id="e7364-119">Określa godzinę rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="e7364-119">Specifies a start time.</span></span>

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

### <span data-ttu-id="e7364-120">-Stream</span><span class="sxs-lookup"><span data-stu-id="e7364-120">-Stream</span></span>
<span data-ttu-id="e7364-121">Określa typ danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e7364-121">Specifies the type of output.</span></span>
<span data-ttu-id="e7364-122">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e7364-122">Valid values are:</span></span> 

- <span data-ttu-id="e7364-123">Jakieś</span><span class="sxs-lookup"><span data-stu-id="e7364-123">Any</span></span>
- <span data-ttu-id="e7364-124">Wykrywanie</span><span class="sxs-lookup"><span data-stu-id="e7364-124">Debug</span></span>
- <span data-ttu-id="e7364-125">Błędów</span><span class="sxs-lookup"><span data-stu-id="e7364-125">Error</span></span>
- <span data-ttu-id="e7364-126">Prowadzone</span><span class="sxs-lookup"><span data-stu-id="e7364-126">Output</span></span>
- <span data-ttu-id="e7364-127">Okres</span><span class="sxs-lookup"><span data-stu-id="e7364-127">Progress</span></span>
- <span data-ttu-id="e7364-128">Pełne</span><span class="sxs-lookup"><span data-stu-id="e7364-128">Verbose</span></span>
- <span data-ttu-id="e7364-129">Ostrzeżenie</span><span class="sxs-lookup"><span data-stu-id="e7364-129">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7364-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7364-130">CommonParameters</span></span>
<span data-ttu-id="e7364-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7364-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7364-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7364-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7364-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7364-133">INPUTS</span></span>

## <span data-ttu-id="e7364-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7364-134">OUTPUTS</span></span>

## <span data-ttu-id="e7364-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7364-135">NOTES</span></span>

## <span data-ttu-id="e7364-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7364-136">RELATED LINKS</span></span>

[<span data-ttu-id="e7364-137">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e7364-137">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="e7364-138">Życiorys — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e7364-138">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="e7364-139">Zatrzymaj — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e7364-139">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="e7364-140">Suspend — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e7364-140">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


