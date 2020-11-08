---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 5E5B8102-9E7E-4128-8160-3AA3803B118F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ff0831e6458a9d587b508acfa2e09948d81d87e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054428"
---
# <span data-ttu-id="3a04c-101">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3a04c-101">Resume-AzureAutomationJob</span></span>

## <span data-ttu-id="3a04c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a04c-102">SYNOPSIS</span></span>

<span data-ttu-id="3a04c-103">Wznawia zawieszone zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3a04c-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="3a04c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a04c-104">SYNTAX</span></span>

```
Resume-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a04c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a04c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3a04c-106">Polecenie cmdlet **Resume-AzureAutomationJob** wznawia wstrzymane zadanie automatyzacji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a04c-106">The **Resume-AzureAutomationJob** cmdlet resumes a suspended Microsoft Azure Automation job.</span></span>
<span data-ttu-id="3a04c-107">Użyj parametru *ID* , aby określić zadanie zawieszone.</span><span class="sxs-lookup"><span data-stu-id="3a04c-107">Use the *Id* parameter to specify the suspended job.</span></span>

<span data-ttu-id="3a04c-108">Aby zawiesić zadanie, użyj polecenia cmdlet Suspend-AzureAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="3a04c-108">To suspend a job, use the Suspend-AzureAutomationJob cmdlet.</span></span>

## <span data-ttu-id="3a04c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a04c-109">EXAMPLES</span></span>

### <span data-ttu-id="3a04c-110">Przykład 1: wznawianie zawieszonego zadania</span><span class="sxs-lookup"><span data-stu-id="3a04c-110">Example 1: Resume a suspended job</span></span>
```
PS C:\> Resume-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="3a04c-111">To polecenie wznawia zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="3a04c-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="3a04c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a04c-112">PARAMETERS</span></span>

### <span data-ttu-id="3a04c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3a04c-113">-AutomationAccountName</span></span>
<span data-ttu-id="3a04c-114">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3a04c-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="3a04c-115">-ID</span><span class="sxs-lookup"><span data-stu-id="3a04c-115">-Id</span></span>
<span data-ttu-id="3a04c-116">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="3a04c-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="3a04c-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="3a04c-117">-Profile</span></span>
<span data-ttu-id="3a04c-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a04c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a04c-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3a04c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a04c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a04c-120">CommonParameters</span></span>
<span data-ttu-id="3a04c-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a04c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a04c-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a04c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a04c-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a04c-123">INPUTS</span></span>

## <span data-ttu-id="3a04c-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a04c-124">OUTPUTS</span></span>

## <span data-ttu-id="3a04c-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a04c-125">NOTES</span></span>

## <span data-ttu-id="3a04c-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a04c-126">RELATED LINKS</span></span>

[<span data-ttu-id="3a04c-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3a04c-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="3a04c-128">Zatrzymaj — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3a04c-128">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="3a04c-129">Suspend — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3a04c-129">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


