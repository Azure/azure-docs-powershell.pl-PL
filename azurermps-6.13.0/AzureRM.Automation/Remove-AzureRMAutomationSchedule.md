---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: cce9b4eff96be34521af58ec85f7abb93d39b3cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549451"
---
# <span data-ttu-id="6a733-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6a733-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="6a733-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a733-102">SYNOPSIS</span></span>
<span data-ttu-id="6a733-103">Usuwa harmonogram automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="6a733-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a733-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a733-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a733-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a733-105">DESCRIPTION</span></span>
<span data-ttu-id="6a733-106">Polecenie cmdlet **Remove-AzureRmAutomationSchedule** usuwa harmonogram z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6a733-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="6a733-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a733-107">EXAMPLES</span></span>

### <span data-ttu-id="6a733-108">Przykład 1. Usuń harmonogram</span><span class="sxs-lookup"><span data-stu-id="6a733-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6a733-109">To polecenie usuwa harmonogram o nazwie Schedule01 na koncie usługi Automation Contoso17 w grupie zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6a733-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="6a733-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a733-110">PARAMETERS</span></span>

### <span data-ttu-id="6a733-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6a733-111">-AutomationAccountName</span></span>
<span data-ttu-id="6a733-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet usuwa harmonogram.</span><span class="sxs-lookup"><span data-stu-id="6a733-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="6a733-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a733-113">-DefaultProfile</span></span>
<span data-ttu-id="6a733-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6a733-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a733-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6a733-115">-Force</span></span>
<span data-ttu-id="6a733-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="6a733-116">ps_force</span></span>

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

### <span data-ttu-id="6a733-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6a733-117">-Name</span></span>
<span data-ttu-id="6a733-118">Określa nazwę harmonogramu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a733-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6a733-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a733-119">-ResourceGroupName</span></span>
<span data-ttu-id="6a733-120">Określa nazwę grupy zasobów, dla której ten aplet polecenia usunie harmonogram.</span><span class="sxs-lookup"><span data-stu-id="6a733-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="6a733-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a733-121">-Confirm</span></span>
<span data-ttu-id="6a733-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a733-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a733-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a733-123">-WhatIf</span></span>
<span data-ttu-id="6a733-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a733-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a733-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6a733-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a733-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a733-126">CommonParameters</span></span>
<span data-ttu-id="6a733-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a733-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a733-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a733-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a733-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a733-129">INPUTS</span></span>

### <span data-ttu-id="6a733-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6a733-130">System.String</span></span>

## <span data-ttu-id="6a733-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a733-131">OUTPUTS</span></span>

### <span data-ttu-id="6a733-132">System. void</span><span class="sxs-lookup"><span data-stu-id="6a733-132">System.Void</span></span>

## <span data-ttu-id="6a733-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a733-133">NOTES</span></span>

## <span data-ttu-id="6a733-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a733-134">RELATED LINKS</span></span>

[<span data-ttu-id="6a733-135">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6a733-135">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="6a733-136">Nowe — AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6a733-136">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="6a733-137">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6a733-137">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


