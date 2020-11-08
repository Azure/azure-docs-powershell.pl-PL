---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6D15837A-22A9-4C5A-8064-C3605088EA71
online version: ''
schema: 2.0.0
ms.openlocfilehash: d31a2ef49674054ca6bb257df67d3439f5abe074
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054839"
---
# <span data-ttu-id="3ffa6-101">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="3ffa6-101">Register-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="3ffa6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ffa6-102">SYNOPSIS</span></span>

<span data-ttu-id="3ffa6-103">Kojarzy element Runbook z harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="3ffa6-103">Associates a runbook with a schedule.</span></span>

## <span data-ttu-id="3ffa6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ffa6-104">SYNTAX</span></span>

### <span data-ttu-id="3ffa6-105">ByRunbookName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3ffa6-105">ByRunbookName (Default)</span></span>
```
Register-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ffa6-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="3ffa6-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3ffa6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3ffa6-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3ffa6-108">Polecenie cmdlet **register-AzureAutomationScheduledRunbook** kojarzy element Runbook z harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="3ffa6-108">The **Register-AzureAutomationScheduledRunbook** cmdlet associates a runbook with a schedule.</span></span>
<span data-ttu-id="3ffa6-109">Element Runbook rozpoczyna się według harmonogramu określonego za pomocą parametru *ScheduleName* .</span><span class="sxs-lookup"><span data-stu-id="3ffa6-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="3ffa6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ffa6-110">EXAMPLES</span></span>

### <span data-ttu-id="3ffa6-111">Przykład 1: Kojarzenie elementu Runbook z harmonogramem</span><span class="sxs-lookup"><span data-stu-id="3ffa6-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\> Register-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01"
```

<span data-ttu-id="3ffa6-112">To polecenie kojarzy element Runbook o nazwie Runbk01 z harmonogramem o nazwie Sched01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3ffa6-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="3ffa6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ffa6-113">PARAMETERS</span></span>

### <span data-ttu-id="3ffa6-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3ffa6-114">-AutomationAccountName</span></span>
<span data-ttu-id="3ffa6-115">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3ffa6-115">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="3ffa6-116">— Parametry</span><span class="sxs-lookup"><span data-stu-id="3ffa6-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffa6-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="3ffa6-117">-Profile</span></span>
<span data-ttu-id="3ffa6-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ffa6-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3ffa6-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3ffa6-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3ffa6-120">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="3ffa6-120">-RunbookName</span></span>
<span data-ttu-id="3ffa6-121">Określa nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="3ffa6-121">Specifies the name of the runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffa6-122">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="3ffa6-122">-ScheduleName</span></span>
<span data-ttu-id="3ffa6-123">Określa nazwę harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="3ffa6-123">Specifies the name of the schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffa6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ffa6-124">CommonParameters</span></span>
<span data-ttu-id="3ffa6-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ffa6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ffa6-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ffa6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ffa6-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ffa6-127">INPUTS</span></span>

## <span data-ttu-id="3ffa6-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ffa6-128">OUTPUTS</span></span>

### <span data-ttu-id="3ffa6-129">Microsoft. Azure. Commands. Automation. model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="3ffa6-129">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="3ffa6-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ffa6-130">NOTES</span></span>

## <span data-ttu-id="3ffa6-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ffa6-131">RELATED LINKS</span></span>

[<span data-ttu-id="3ffa6-132">Nowe — AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3ffa6-132">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="3ffa6-133">Wyrejestrowanie — AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="3ffa6-133">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


