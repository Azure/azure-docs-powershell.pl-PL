---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: 0c37c33b60d430bc1782254401033934552f5663
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239530"
---
# <span data-ttu-id="9cd9c-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9cd9c-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="9cd9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cd9c-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd9c-103">Usuwa harmonogram automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9cd9c-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="9cd9c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9cd9c-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cd9c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9cd9c-105">DESCRIPTION</span></span>
<span data-ttu-id="9cd9c-106">Polecenie **cmdlet Remove-AzAutomationSchedule** usuwa harmonogram z automatyzacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9cd9c-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="9cd9c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9cd9c-107">EXAMPLES</span></span>

### <span data-ttu-id="9cd9c-108">Przykład 1. Usuwanie harmonogramu</span><span class="sxs-lookup"><span data-stu-id="9cd9c-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9cd9c-109">To polecenie usuwa harmonogram o nazwie Harmonogram01 w koncie automatyzacji Contoso17 w grupie zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="9cd9c-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="9cd9c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cd9c-110">PARAMETERS</span></span>

### <span data-ttu-id="9cd9c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9cd9c-111">-AutomationAccountName</span></span>
<span data-ttu-id="9cd9c-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa harmonogram.</span><span class="sxs-lookup"><span data-stu-id="9cd9c-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd9c-113">-DefaultProfile</span></span>
<span data-ttu-id="9cd9c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9cd9c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd9c-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9cd9c-115">-Force</span></span>
<span data-ttu-id="9cd9c-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="9cd9c-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd9c-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9cd9c-117">-Name</span></span>
<span data-ttu-id="9cd9c-118">Określa nazwę harmonogramu usunięcia tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cd9c-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd9c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd9c-119">-ResourceGroupName</span></span>
<span data-ttu-id="9cd9c-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet usuwa harmonogram.</span><span class="sxs-lookup"><span data-stu-id="9cd9c-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd9c-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9cd9c-121">-Confirm</span></span>
<span data-ttu-id="9cd9c-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9cd9c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd9c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cd9c-123">-WhatIf</span></span>
<span data-ttu-id="9cd9c-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cd9c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cd9c-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9cd9c-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd9c-126">CommonParameters</span></span>
<span data-ttu-id="9cd9c-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd9c-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cd9c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd9c-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cd9c-129">INPUTS</span></span>

### <span data-ttu-id="9cd9c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9cd9c-130">System.String</span></span>

## <span data-ttu-id="9cd9c-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9cd9c-131">OUTPUTS</span></span>

### <span data-ttu-id="9cd9c-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="9cd9c-132">System.Void</span></span>

## <span data-ttu-id="9cd9c-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9cd9c-133">NOTES</span></span>

## <span data-ttu-id="9cd9c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cd9c-134">RELATED LINKS</span></span>

[<span data-ttu-id="9cd9c-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9cd9c-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="9cd9c-136">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9cd9c-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="9cd9c-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9cd9c-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


