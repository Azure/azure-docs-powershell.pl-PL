---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
ms.openlocfilehash: bbf86c6744e064b2958acaf5fe7928d537548805
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710530"
---
# <span data-ttu-id="af916-101">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="af916-101">New-AzAutomationRunbook</span></span>

## <span data-ttu-id="af916-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af916-102">SYNOPSIS</span></span>
<span data-ttu-id="af916-103">Tworzy element Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="af916-103">Creates an Automation runbook.</span></span>

## <span data-ttu-id="af916-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af916-104">SYNTAX</span></span>

```
New-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af916-105">Opis</span><span class="sxs-lookup"><span data-stu-id="af916-105">DESCRIPTION</span></span>
<span data-ttu-id="af916-106">Polecenie cmdlet **New-AzAutomationRunbook** tworzy pusty element Runbook usługi Azure Automation za pomocą funkcji APS.</span><span class="sxs-lookup"><span data-stu-id="af916-106">The **New-AzAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="af916-107">Określ nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="af916-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="af916-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af916-108">EXAMPLES</span></span>

### <span data-ttu-id="af916-109">Przykład 1. Tworzenie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="af916-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="af916-110">To polecenie tworzy element Runbook o nazwie Runbook02 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="af916-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="af916-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af916-111">PARAMETERS</span></span>

### <span data-ttu-id="af916-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="af916-112">-AutomationAccountName</span></span>
<span data-ttu-id="af916-113">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet tworzy element Runbook.</span><span class="sxs-lookup"><span data-stu-id="af916-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="af916-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af916-114">-DefaultProfile</span></span>
<span data-ttu-id="af916-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="af916-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af916-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="af916-116">-Description</span></span>
<span data-ttu-id="af916-117">Określa opis elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="af916-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="af916-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="af916-118">-LogProgress</span></span>
<span data-ttu-id="af916-119">Określa, czy element Runbook rejestruje postęp.</span><span class="sxs-lookup"><span data-stu-id="af916-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="af916-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="af916-120">-LogVerbose</span></span>
<span data-ttu-id="af916-121">Określa, czy rejestrowanie zawiera szczegółowe informacje.</span><span class="sxs-lookup"><span data-stu-id="af916-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="af916-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af916-122">-Name</span></span>
<span data-ttu-id="af916-123">Określa nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="af916-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="af916-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af916-124">-ResourceGroupName</span></span>
<span data-ttu-id="af916-125">Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy element Runbook.</span><span class="sxs-lookup"><span data-stu-id="af916-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="af916-126">-Tagi</span><span class="sxs-lookup"><span data-stu-id="af916-126">-Tags</span></span>
<span data-ttu-id="af916-127">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="af916-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="af916-128">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="af916-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af916-129">-Type</span><span class="sxs-lookup"><span data-stu-id="af916-129">-Type</span></span>
<span data-ttu-id="af916-130">Określa typ elementu Runbook tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af916-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="af916-131">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="af916-131">Valid values are:</span></span>
- <span data-ttu-id="af916-132">Narzędzia</span><span class="sxs-lookup"><span data-stu-id="af916-132">PowerShell</span></span>
- <span data-ttu-id="af916-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="af916-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="af916-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="af916-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="af916-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="af916-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="af916-136">Graf</span><span class="sxs-lookup"><span data-stu-id="af916-136">Graph</span></span>
- <span data-ttu-id="af916-137">Python2 wykres wartości jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="af916-137">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="af916-138">Jest to równoznaczne z GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="af916-138">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af916-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af916-139">CommonParameters</span></span>
<span data-ttu-id="af916-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af916-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af916-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af916-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af916-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af916-142">INPUTS</span></span>

### <span data-ttu-id="af916-143">System. String</span><span class="sxs-lookup"><span data-stu-id="af916-143">System.String</span></span>

### <span data-ttu-id="af916-144">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="af916-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="af916-145">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="af916-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="af916-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af916-146">OUTPUTS</span></span>

### <span data-ttu-id="af916-147">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="af916-147">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="af916-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af916-148">NOTES</span></span>

## <span data-ttu-id="af916-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af916-149">RELATED LINKS</span></span>

[<span data-ttu-id="af916-150">Eksportowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="af916-150">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="af916-151">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="af916-151">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="af916-152">Import — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="af916-152">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="af916-153">Publikowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="af916-153">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="af916-154">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="af916-154">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="af916-155">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="af916-155">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="af916-156">Start — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="af916-156">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
