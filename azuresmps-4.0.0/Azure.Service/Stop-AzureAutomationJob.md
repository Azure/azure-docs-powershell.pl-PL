---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2E363D6B-7A05-4C54-B005-68FDBA49A105
online version: ''
schema: 2.0.0
ms.openlocfilehash: cda64b916635d3b46ffb7e8b4170330810a95b5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054908"
---
# <span data-ttu-id="ba590-101">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ba590-101">Stop-AzureAutomationJob</span></span>

## <span data-ttu-id="ba590-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba590-102">SYNOPSIS</span></span>

<span data-ttu-id="ba590-103">Zatrzymuje zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="ba590-103">Stops an Automation job.</span></span>

## <span data-ttu-id="ba590-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba590-104">SYNTAX</span></span>

```
Stop-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba590-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba590-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ba590-106">Polecenie cmdlet **stop-AzureAutomationJob** zatrzymuje zadanie usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ba590-106">The **Stop-AzureAutomationJob** cmdlet stops a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="ba590-107">Określanie uruchomionego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="ba590-107">Specify a running automation job.</span></span>

## <span data-ttu-id="ba590-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba590-108">EXAMPLES</span></span>

### <span data-ttu-id="ba590-109">Przykład 1: Zatrzymywanie zadania</span><span class="sxs-lookup"><span data-stu-id="ba590-109">Example 1: Stop a job</span></span>
```
PS C:\> Stop-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="ba590-110">To polecenie zatrzymuje zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="ba590-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="ba590-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba590-111">PARAMETERS</span></span>

### <span data-ttu-id="ba590-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ba590-112">-AutomationAccountName</span></span>
<span data-ttu-id="ba590-113">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="ba590-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="ba590-114">-ID</span><span class="sxs-lookup"><span data-stu-id="ba590-114">-Id</span></span>
<span data-ttu-id="ba590-115">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="ba590-115">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="ba590-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="ba590-116">-Profile</span></span>
<span data-ttu-id="ba590-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba590-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba590-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ba590-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ba590-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba590-119">CommonParameters</span></span>
<span data-ttu-id="ba590-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba590-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba590-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba590-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba590-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba590-122">INPUTS</span></span>

## <span data-ttu-id="ba590-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba590-123">OUTPUTS</span></span>

## <span data-ttu-id="ba590-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba590-124">NOTES</span></span>

## <span data-ttu-id="ba590-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba590-125">RELATED LINKS</span></span>

[<span data-ttu-id="ba590-126">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ba590-126">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="ba590-127">Życiorys — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ba590-127">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="ba590-128">Suspend — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ba590-128">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


