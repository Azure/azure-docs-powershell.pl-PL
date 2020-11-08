---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: 0c37c33b60d430bc1782254401033934552f5663
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063674"
---
# <span data-ttu-id="09db5-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="09db5-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="09db5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09db5-102">SYNOPSIS</span></span>
<span data-ttu-id="09db5-103">Usuwa harmonogram automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="09db5-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="09db5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09db5-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09db5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="09db5-105">DESCRIPTION</span></span>
<span data-ttu-id="09db5-106">Polecenie cmdlet **Remove-AzAutomationSchedule** usuwa harmonogram z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="09db5-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="09db5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09db5-107">EXAMPLES</span></span>

### <span data-ttu-id="09db5-108">Przykład 1. Usuń harmonogram</span><span class="sxs-lookup"><span data-stu-id="09db5-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="09db5-109">To polecenie usuwa harmonogram o nazwie Schedule01 na koncie usługi Automation Contoso17 w grupie zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="09db5-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="09db5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09db5-110">PARAMETERS</span></span>

### <span data-ttu-id="09db5-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="09db5-111">-AutomationAccountName</span></span>
<span data-ttu-id="09db5-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa harmonogram.</span><span class="sxs-lookup"><span data-stu-id="09db5-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="09db5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09db5-113">-DefaultProfile</span></span>
<span data-ttu-id="09db5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="09db5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09db5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="09db5-115">-Force</span></span>
<span data-ttu-id="09db5-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="09db5-116">ps_force</span></span>

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

### <span data-ttu-id="09db5-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09db5-117">-Name</span></span>
<span data-ttu-id="09db5-118">Określa nazwę harmonogramu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09db5-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="09db5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09db5-119">-ResourceGroupName</span></span>
<span data-ttu-id="09db5-120">Określa nazwę grupy zasobów, dla której ten aplet polecenia usunie harmonogram.</span><span class="sxs-lookup"><span data-stu-id="09db5-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="09db5-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09db5-121">-Confirm</span></span>
<span data-ttu-id="09db5-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09db5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09db5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09db5-123">-WhatIf</span></span>
<span data-ttu-id="09db5-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09db5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09db5-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="09db5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09db5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09db5-126">CommonParameters</span></span>
<span data-ttu-id="09db5-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09db5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09db5-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09db5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09db5-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09db5-129">INPUTS</span></span>

### <span data-ttu-id="09db5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="09db5-130">System.String</span></span>

## <span data-ttu-id="09db5-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09db5-131">OUTPUTS</span></span>

### <span data-ttu-id="09db5-132">System. void</span><span class="sxs-lookup"><span data-stu-id="09db5-132">System.Void</span></span>

## <span data-ttu-id="09db5-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09db5-133">NOTES</span></span>

## <span data-ttu-id="09db5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09db5-134">RELATED LINKS</span></span>

[<span data-ttu-id="09db5-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="09db5-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="09db5-136">Nowe — AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="09db5-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="09db5-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="09db5-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


