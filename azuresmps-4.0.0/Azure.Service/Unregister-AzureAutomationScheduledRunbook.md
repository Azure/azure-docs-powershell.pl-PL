---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: EA7C1449-E11F-4AE8-A513-59BDCA38875D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e432edd2469fa25519c12f0cd1f2dadb1d0dca2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055553"
---
# <span data-ttu-id="cdfd5-101">Unregister-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="cdfd5-101">Unregister-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="cdfd5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cdfd5-102">SYNOPSIS</span></span>

<span data-ttu-id="cdfd5-103">Usuwa skojarzenie między elementem Runbook a harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="cdfd5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cdfd5-104">SYNTAX</span></span>

### <span data-ttu-id="cdfd5-105">ByJobScheduleId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cdfd5-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cdfd5-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="cdfd5-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cdfd5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cdfd5-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="cdfd5-108">Polecenie cmdlet **Unregister-AzureAutomationScheduledRunbook** powoduje usunięcie skojarzenia elementu Runbook usługi Microsoft Azure Automation i harmonogramu, który uniemożliwia uruchomienie elementu Runbook po uruchomieniu harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-108">The **Unregister-AzureAutomationScheduledRunbook** cmdlet removes the association between a Microsoft Azure Automation runbook and a schedule, which stops the runbook from starting when the schedule fires.</span></span>

## <span data-ttu-id="cdfd5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cdfd5-109">EXAMPLES</span></span>

### <span data-ttu-id="cdfd5-110">Przykład 1: Usuwanie skojarzenia między elementem Runbook a harmonogramem</span><span class="sxs-lookup"><span data-stu-id="cdfd5-110">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\> Unregister-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="cdfd5-111">To polecenie powoduje usunięcie skojarzenia między elementem Runbook o nazwie Runbk01 a harmonogramem o nazwie Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-111">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="cdfd5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdfd5-112">PARAMETERS</span></span>

### <span data-ttu-id="cdfd5-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cdfd5-113">-AutomationAccountName</span></span>
<span data-ttu-id="cdfd5-114">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="cdfd5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cdfd5-115">-Force</span></span>
<span data-ttu-id="cdfd5-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdfd5-117">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="cdfd5-117">-JobScheduleId</span></span>
<span data-ttu-id="cdfd5-118">Określa identyfikator zaplanowanego elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-118">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdfd5-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="cdfd5-119">-Profile</span></span>
<span data-ttu-id="cdfd5-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cdfd5-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cdfd5-122">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="cdfd5-122">-RunbookName</span></span>
<span data-ttu-id="cdfd5-123">Określa nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-123">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="cdfd5-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="cdfd5-124">-ScheduleName</span></span>
<span data-ttu-id="cdfd5-125">Określa nazwę harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-125">Specifies the name of a schedule.</span></span>

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

### <span data-ttu-id="cdfd5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdfd5-126">CommonParameters</span></span>
<span data-ttu-id="cdfd5-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdfd5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdfd5-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdfd5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdfd5-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdfd5-129">INPUTS</span></span>

## <span data-ttu-id="cdfd5-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cdfd5-130">OUTPUTS</span></span>

## <span data-ttu-id="cdfd5-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cdfd5-131">NOTES</span></span>

## <span data-ttu-id="cdfd5-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdfd5-132">RELATED LINKS</span></span>

[<span data-ttu-id="cdfd5-133">Rejestr — AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="cdfd5-133">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)


