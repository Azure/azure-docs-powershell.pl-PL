---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CE04DEE6-28AE-43A3-A8DE-98AC0A57E575
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1c2d9a3aa53cb8efd2924f24aa80db2c7fd07fea
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054725"
---
# <span data-ttu-id="4cc82-101">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4cc82-101">Suspend-AzureAutomationJob</span></span>

## <span data-ttu-id="4cc82-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4cc82-102">SYNOPSIS</span></span>

<span data-ttu-id="4cc82-103">Wstrzymuje zadanie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="4cc82-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="4cc82-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4cc82-104">SYNTAX</span></span>

```
Suspend-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cc82-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4cc82-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4cc82-106">Polecenie cmdlet **Suspend-AzureAutomationJob** zawiesza zadanie automatyzacji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4cc82-106">The **Suspend-AzureAutomationJob** cmdlet suspends a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="4cc82-107">Określanie uruchomionego zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="4cc82-107">Specify a running Automation job.</span></span>

<span data-ttu-id="4cc82-108">Aby wznowić zawieszone zadanie, użyj polecenia cmdlet **Resume-AzureAutomationJob** .</span><span class="sxs-lookup"><span data-stu-id="4cc82-108">To resume a suspended job, use the **Resume-AzureAutomationJob** cmdlet.</span></span>

## <span data-ttu-id="4cc82-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4cc82-109">EXAMPLES</span></span>

### <span data-ttu-id="4cc82-110">Przykład 1: Wstrzymywanie zadania</span><span class="sxs-lookup"><span data-stu-id="4cc82-110">Example 1: Suspend a job</span></span>
```
PS C:\> Suspend-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="4cc82-111">To polecenie zawiesza zadanie o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="4cc82-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="4cc82-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4cc82-112">PARAMETERS</span></span>

### <span data-ttu-id="4cc82-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4cc82-113">-AutomationAccountName</span></span>
<span data-ttu-id="4cc82-114">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="4cc82-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="4cc82-115">-ID</span><span class="sxs-lookup"><span data-stu-id="4cc82-115">-Id</span></span>
<span data-ttu-id="4cc82-116">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="4cc82-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="4cc82-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="4cc82-117">-Profile</span></span>
<span data-ttu-id="4cc82-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cc82-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4cc82-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4cc82-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4cc82-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc82-120">CommonParameters</span></span>
<span data-ttu-id="4cc82-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cc82-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc82-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc82-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc82-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cc82-123">INPUTS</span></span>

## <span data-ttu-id="4cc82-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4cc82-124">OUTPUTS</span></span>

## <span data-ttu-id="4cc82-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4cc82-125">NOTES</span></span>

## <span data-ttu-id="4cc82-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cc82-126">RELATED LINKS</span></span>

[<span data-ttu-id="4cc82-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4cc82-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="4cc82-128">Życiorys — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4cc82-128">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="4cc82-129">Zatrzymaj — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4cc82-129">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)


