---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 4dd1eee278adcced1dbace9a30e88b5767037746
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706699"
---
# <span data-ttu-id="4e08e-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4e08e-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="4e08e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e08e-102">SYNOPSIS</span></span>
<span data-ttu-id="4e08e-103">Modyfikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="4e08e-103">Modifies a runbook.</span></span>

## <span data-ttu-id="4e08e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e08e-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e08e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4e08e-105">DESCRIPTION</span></span>
<span data-ttu-id="4e08e-106">Polecenie cmdlet **Set-AzAutomationRunbook** modyfikuje konfigurację elementu Runbook usługi Azure Automation w usłudze APS.</span><span class="sxs-lookup"><span data-stu-id="4e08e-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="4e08e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e08e-107">EXAMPLES</span></span>

### <span data-ttu-id="4e08e-108">Przykład 1: Włączanie pełnego rejestrowania elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="4e08e-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4e08e-109">To polecenie umożliwia pełne rejestrowanie informacji o zadaniach określonego elementu Runbook na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4e08e-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="4e08e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e08e-110">PARAMETERS</span></span>

### <span data-ttu-id="4e08e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4e08e-111">-AutomationAccountName</span></span>
<span data-ttu-id="4e08e-112">Określa nazwę konta automatyzacji, w którym polecenie cmdlet modyfikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="4e08e-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="4e08e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e08e-113">-DefaultProfile</span></span>
<span data-ttu-id="4e08e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4e08e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e08e-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="4e08e-115">-Description</span></span>
<span data-ttu-id="4e08e-116">Określa opis elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="4e08e-116">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e08e-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="4e08e-117">-LogProgress</span></span>
<span data-ttu-id="4e08e-118">Określa, czy element Runbook rejestruje postęp.</span><span class="sxs-lookup"><span data-stu-id="4e08e-118">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e08e-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="4e08e-119">-LogVerbose</span></span>
<span data-ttu-id="4e08e-120">Określa, czy rejestrowanie zawiera szczegółowe informacje.</span><span class="sxs-lookup"><span data-stu-id="4e08e-120">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e08e-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4e08e-121">-Name</span></span>
<span data-ttu-id="4e08e-122">Określa nazwę elementu Runbook, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e08e-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4e08e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e08e-123">-ResourceGroupName</span></span>
<span data-ttu-id="4e08e-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="4e08e-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="4e08e-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e08e-125">-Tag</span></span>
<span data-ttu-id="4e08e-126">Znaczniki elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="4e08e-126">The runbook tags.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e08e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e08e-127">CommonParameters</span></span>
<span data-ttu-id="4e08e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e08e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e08e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e08e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e08e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e08e-130">INPUTS</span></span>

### <span data-ttu-id="4e08e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4e08e-131">System.String</span></span>

### <span data-ttu-id="4e08e-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="4e08e-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="4e08e-133">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4e08e-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4e08e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e08e-134">OUTPUTS</span></span>

### <span data-ttu-id="4e08e-135">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="4e08e-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="4e08e-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e08e-136">NOTES</span></span>

## <span data-ttu-id="4e08e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e08e-137">RELATED LINKS</span></span>

[<span data-ttu-id="4e08e-138">Eksportowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4e08e-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="4e08e-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4e08e-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="4e08e-140">Import — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4e08e-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="4e08e-141">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4e08e-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="4e08e-142">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4e08e-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="4e08e-143">Publikowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4e08e-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="4e08e-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4e08e-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="4e08e-145">Start — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4e08e-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


