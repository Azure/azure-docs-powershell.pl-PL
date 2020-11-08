---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0C156A1C-72DC-4B3C-9033-1B985139A732
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43f371e44876c8927edc4f30fcfe0095a28cb27b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055137"
---
# <span data-ttu-id="d2914-101">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d2914-101">Remove-AzureAutomationRunbook</span></span>

## <span data-ttu-id="d2914-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2914-102">SYNOPSIS</span></span>

<span data-ttu-id="d2914-103">Usuwa element Runbook.</span><span class="sxs-lookup"><span data-stu-id="d2914-103">Removes a runbook.</span></span>

## <span data-ttu-id="d2914-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2914-104">SYNTAX</span></span>

```
Remove-AzureAutomationRunbook -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2914-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d2914-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="d2914-106">Polecenie cmdlet **Remove-AzureAutomationRunbook** usuwa element Runbook z usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d2914-106">The **Remove-AzureAutomationRunbook** cmdlet removes a runbook from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="d2914-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2914-107">EXAMPLES</span></span>

### <span data-ttu-id="d2914-108">Przykład 1. Usuń element Runbook</span><span class="sxs-lookup"><span data-stu-id="d2914-108">Example 1: Remove a runbook</span></span>
```
PS C:\> Remove-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook"
```

<span data-ttu-id="d2914-109">To polecenie umożliwia usunięcie elementu Runbook o nazwie webrunbook z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d2914-109">This command removes the runbook named MyRunbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d2914-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2914-110">PARAMETERS</span></span>

### <span data-ttu-id="d2914-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d2914-111">-AutomationAccountName</span></span>
<span data-ttu-id="d2914-112">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d2914-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="d2914-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d2914-113">-Force</span></span>
<span data-ttu-id="d2914-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d2914-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2914-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d2914-115">-Name</span></span>
<span data-ttu-id="d2914-116">Określa nazwę elementu Runbook, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="d2914-116">Specifies the name of the runbook to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2914-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="d2914-117">-Profile</span></span>
<span data-ttu-id="d2914-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2914-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d2914-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d2914-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d2914-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2914-120">-Confirm</span></span>
<span data-ttu-id="d2914-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2914-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2914-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2914-122">-WhatIf</span></span>
<span data-ttu-id="d2914-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2914-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2914-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d2914-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2914-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2914-125">CommonParameters</span></span>
<span data-ttu-id="d2914-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2914-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2914-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2914-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2914-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2914-128">INPUTS</span></span>

## <span data-ttu-id="d2914-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2914-129">OUTPUTS</span></span>

## <span data-ttu-id="d2914-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2914-130">NOTES</span></span>

## <span data-ttu-id="d2914-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2914-131">RELATED LINKS</span></span>

[<span data-ttu-id="d2914-132">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d2914-132">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="d2914-133">Nowe — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d2914-133">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="d2914-134">Publikowanie — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d2914-134">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="d2914-135">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d2914-135">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="d2914-136">Start — AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d2914-136">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


