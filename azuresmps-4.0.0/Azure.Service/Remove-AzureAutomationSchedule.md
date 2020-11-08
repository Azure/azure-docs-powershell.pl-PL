---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2412F6BC-E338-4D9C-8982-C0668C1CA4C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2b8ae09c79b420d7273fc6db23e23a6846a542e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055136"
---
# <span data-ttu-id="da47c-101">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="da47c-101">Remove-AzureAutomationSchedule</span></span>

## <span data-ttu-id="da47c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da47c-102">SYNOPSIS</span></span>

<span data-ttu-id="da47c-103">Usuwa harmonogram usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="da47c-103">Deletes an Azure Automation schedule.</span></span>

## <span data-ttu-id="da47c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da47c-104">SYNTAX</span></span>

```
Remove-AzureAutomationSchedule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da47c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da47c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="da47c-106">Polecenie cmdlet **Remove-AzureAutomationSchedule** usuwa harmonogram z usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="da47c-106">The **Remove-AzureAutomationSchedule** cmdlet deletes a schedule from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="da47c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da47c-107">EXAMPLES</span></span>

### <span data-ttu-id="da47c-108">Przykład 1. Usuń harmonogram</span><span class="sxs-lookup"><span data-stu-id="da47c-108">Example 1: Remove a schedule</span></span>
```
PS C:\> Remove-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "MySchedule"
```

<span data-ttu-id="da47c-109">To polecenie powoduje usunięcie harmonogramu o nazwie mój harmonogram.</span><span class="sxs-lookup"><span data-stu-id="da47c-109">This command removes the schedule named MySchedule.</span></span>

## <span data-ttu-id="da47c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da47c-110">PARAMETERS</span></span>

### <span data-ttu-id="da47c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="da47c-111">-AutomationAccountName</span></span>
<span data-ttu-id="da47c-112">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="da47c-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="da47c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="da47c-113">-Force</span></span>
<span data-ttu-id="da47c-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="da47c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da47c-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da47c-115">-Name</span></span>
<span data-ttu-id="da47c-116">Określa nazwę harmonogramu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="da47c-116">Specifies the name of the schedule to remove.</span></span>

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

### <span data-ttu-id="da47c-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="da47c-117">-Profile</span></span>
<span data-ttu-id="da47c-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da47c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="da47c-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="da47c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da47c-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da47c-120">-Confirm</span></span>
<span data-ttu-id="da47c-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da47c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da47c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da47c-122">-WhatIf</span></span>
<span data-ttu-id="da47c-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da47c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da47c-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da47c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da47c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da47c-125">CommonParameters</span></span>
<span data-ttu-id="da47c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da47c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da47c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da47c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da47c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da47c-128">INPUTS</span></span>

## <span data-ttu-id="da47c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da47c-129">OUTPUTS</span></span>

## <span data-ttu-id="da47c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da47c-130">NOTES</span></span>

## <span data-ttu-id="da47c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da47c-131">RELATED LINKS</span></span>

[<span data-ttu-id="da47c-132">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="da47c-132">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="da47c-133">Nowe — AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="da47c-133">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="da47c-134">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="da47c-134">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


