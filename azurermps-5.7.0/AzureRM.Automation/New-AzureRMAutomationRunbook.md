---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 77c089e4ab46972892a7fe9ad3cc519dc7f20551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718660"
---
# <span data-ttu-id="e89c3-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e89c3-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="e89c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e89c3-102">SYNOPSIS</span></span>
<span data-ttu-id="e89c3-103">Tworzy element Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="e89c3-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e89c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e89c3-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e89c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e89c3-105">DESCRIPTION</span></span>
<span data-ttu-id="e89c3-106">Polecenie cmdlet **New-AzureRmAutomationRunbook** tworzy pusty element Runbook usługi Azure Automation za pomocą funkcji APS.</span><span class="sxs-lookup"><span data-stu-id="e89c3-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="e89c3-107">Określ nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e89c3-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="e89c3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e89c3-108">EXAMPLES</span></span>

### <span data-ttu-id="e89c3-109">Przykład 1. Tworzenie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="e89c3-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e89c3-110">To polecenie tworzy element Runbook o nazwie Runbook02 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e89c3-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e89c3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e89c3-111">PARAMETERS</span></span>

### <span data-ttu-id="e89c3-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e89c3-112">-AutomationAccountName</span></span>
<span data-ttu-id="e89c3-113">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet tworzy element Runbook.</span><span class="sxs-lookup"><span data-stu-id="e89c3-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e89c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e89c3-114">-DefaultProfile</span></span>
<span data-ttu-id="e89c3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e89c3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e89c3-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="e89c3-116">-Description</span></span>
<span data-ttu-id="e89c3-117">Określa opis elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e89c3-117">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e89c3-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="e89c3-118">-LogProgress</span></span>
<span data-ttu-id="e89c3-119">Określa, czy element Runbook rejestruje postęp.</span><span class="sxs-lookup"><span data-stu-id="e89c3-119">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e89c3-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="e89c3-120">-LogVerbose</span></span>
<span data-ttu-id="e89c3-121">Określa, czy rejestrowanie zawiera szczegółowe informacje.</span><span class="sxs-lookup"><span data-stu-id="e89c3-121">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e89c3-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e89c3-122">-Name</span></span>
<span data-ttu-id="e89c3-123">Określa nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="e89c3-123">Specifies a name for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e89c3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e89c3-124">-ResourceGroupName</span></span>
<span data-ttu-id="e89c3-125">Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy element Runbook.</span><span class="sxs-lookup"><span data-stu-id="e89c3-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e89c3-126">-Tagi</span><span class="sxs-lookup"><span data-stu-id="e89c3-126">-Tags</span></span>
<span data-ttu-id="e89c3-127">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="e89c3-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e89c3-128">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="e89c3-128">For example:</span></span>

<span data-ttu-id="e89c3-129">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="e89c3-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e89c3-130">-Type</span><span class="sxs-lookup"><span data-stu-id="e89c3-130">-Type</span></span>
<span data-ttu-id="e89c3-131">Określa typ elementu Runbook tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e89c3-131">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="e89c3-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e89c3-132">Valid values are:</span></span>

- <span data-ttu-id="e89c3-133">Narzędzia</span><span class="sxs-lookup"><span data-stu-id="e89c3-133">PowerShell</span></span>
- <span data-ttu-id="e89c3-134">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="e89c3-134">GraphicalPowerShell</span></span>
- <span data-ttu-id="e89c3-135">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="e89c3-135">PowerShellWorkflow</span></span>
- <span data-ttu-id="e89c3-136">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="e89c3-136">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="e89c3-137">Graf</span><span class="sxs-lookup"><span data-stu-id="e89c3-137">Graph</span></span>

<span data-ttu-id="e89c3-138">Wykres wartości jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="e89c3-138">The value Graph is obsolete.</span></span>
<span data-ttu-id="e89c3-139">Jest to równoznaczne z GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="e89c3-139">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e89c3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e89c3-140">CommonParameters</span></span>
<span data-ttu-id="e89c3-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e89c3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e89c3-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e89c3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e89c3-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e89c3-143">INPUTS</span></span>

### <span data-ttu-id="e89c3-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e89c3-144">None</span></span>
<span data-ttu-id="e89c3-145">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e89c3-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e89c3-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e89c3-146">OUTPUTS</span></span>

### <span data-ttu-id="e89c3-147">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="e89c3-147">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="e89c3-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e89c3-148">NOTES</span></span>

## <span data-ttu-id="e89c3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e89c3-149">RELATED LINKS</span></span>

[<span data-ttu-id="e89c3-150">Eksportowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e89c3-150">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="e89c3-151">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e89c3-151">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="e89c3-152">Import — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e89c3-152">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="e89c3-153">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e89c3-153">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="e89c3-154">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e89c3-154">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="e89c3-155">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e89c3-155">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="e89c3-156">Start — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e89c3-156">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
