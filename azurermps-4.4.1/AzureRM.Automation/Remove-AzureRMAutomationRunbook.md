---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
ms.openlocfilehash: 96a82f4cc39952517bf5cfaeca24191cc4dd2d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548388"
---
# <span data-ttu-id="b7e8f-101">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7e8f-101">Remove-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="b7e8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e8f-103">Usuwa element Runbook.</span><span class="sxs-lookup"><span data-stu-id="b7e8f-103">Removes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7e8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7e8f-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7e8f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b7e8f-105">DESCRIPTION</span></span>
<span data-ttu-id="b7e8f-106">Polecenie cmdlet **Remove-AzureRmAutomationRunbook** usuwa element Runbook z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b7e8f-106">The **Remove-AzureRmAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="b7e8f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7e8f-107">EXAMPLES</span></span>

### <span data-ttu-id="b7e8f-108">Przykład 1. Usuń element Runbook</span><span class="sxs-lookup"><span data-stu-id="b7e8f-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b7e8f-109">To polecenie usuwa element Runbook o nazwie Runbook03 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b7e8f-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="b7e8f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7e8f-110">PARAMETERS</span></span>

### <span data-ttu-id="b7e8f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b7e8f-111">-AutomationAccountName</span></span>
<span data-ttu-id="b7e8f-112">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet usuwa element Runbook.</span><span class="sxs-lookup"><span data-stu-id="b7e8f-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="b7e8f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b7e8f-113">-Force</span></span>
<span data-ttu-id="b7e8f-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="b7e8f-114">ps_force</span></span>

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

### <span data-ttu-id="b7e8f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7e8f-115">-Name</span></span>
<span data-ttu-id="b7e8f-116">Określa nazwę elementu Runbook usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7e8f-116">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e8f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7e8f-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7e8f-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet publikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="b7e8f-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="b7e8f-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7e8f-119">-Confirm</span></span>
<span data-ttu-id="b7e8f-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7e8f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7e8f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7e8f-121">-WhatIf</span></span>
<span data-ttu-id="b7e8f-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7e8f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7e8f-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b7e8f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7e8f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e8f-124">-DefaultProfile</span></span>
<span data-ttu-id="b7e8f-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7e8f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7e8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e8f-126">CommonParameters</span></span>
<span data-ttu-id="b7e8f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7e8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e8f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7e8f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e8f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7e8f-129">INPUTS</span></span>

## <span data-ttu-id="b7e8f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7e8f-130">OUTPUTS</span></span>

## <span data-ttu-id="b7e8f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7e8f-131">NOTES</span></span>

## <span data-ttu-id="b7e8f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7e8f-132">RELATED LINKS</span></span>

[<span data-ttu-id="b7e8f-133">Eksportowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7e8f-133">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7e8f-134">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7e8f-134">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7e8f-135">Import — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7e8f-135">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7e8f-136">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7e8f-136">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7e8f-137">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7e8f-137">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7e8f-138">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7e8f-138">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7e8f-139">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7e8f-139">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7e8f-140">Start — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7e8f-140">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


