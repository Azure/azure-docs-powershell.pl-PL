---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 73945c02c5c5802e169e0868908874374080b344
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547659"
---
# <span data-ttu-id="98d2c-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98d2c-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="98d2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="98d2c-103">Tworzy element Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="98d2c-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98d2c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98d2c-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98d2c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="98d2c-105">DESCRIPTION</span></span>
<span data-ttu-id="98d2c-106">Polecenie cmdlet **New-AzureRmAutomationRunbook** tworzy pusty element Runbook usługi Azure Automation za pomocą funkcji APS.</span><span class="sxs-lookup"><span data-stu-id="98d2c-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="98d2c-107">Określ nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="98d2c-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="98d2c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98d2c-108">EXAMPLES</span></span>

### <span data-ttu-id="98d2c-109">Przykład 1. Tworzenie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="98d2c-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="98d2c-110">To polecenie tworzy element Runbook o nazwie Runbook02 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="98d2c-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="98d2c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98d2c-111">PARAMETERS</span></span>

### <span data-ttu-id="98d2c-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="98d2c-112">-AutomationAccountName</span></span>
<span data-ttu-id="98d2c-113">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet tworzy element Runbook.</span><span class="sxs-lookup"><span data-stu-id="98d2c-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="98d2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d2c-114">-DefaultProfile</span></span>
<span data-ttu-id="98d2c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="98d2c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98d2c-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="98d2c-116">-Description</span></span>
<span data-ttu-id="98d2c-117">Określa opis elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="98d2c-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="98d2c-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="98d2c-118">-LogProgress</span></span>
<span data-ttu-id="98d2c-119">Określa, czy element Runbook rejestruje postęp.</span><span class="sxs-lookup"><span data-stu-id="98d2c-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="98d2c-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="98d2c-120">-LogVerbose</span></span>
<span data-ttu-id="98d2c-121">Określa, czy rejestrowanie zawiera szczegółowe informacje.</span><span class="sxs-lookup"><span data-stu-id="98d2c-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="98d2c-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98d2c-122">-Name</span></span>
<span data-ttu-id="98d2c-123">Określa nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="98d2c-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="98d2c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98d2c-124">-ResourceGroupName</span></span>
<span data-ttu-id="98d2c-125">Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy element Runbook.</span><span class="sxs-lookup"><span data-stu-id="98d2c-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="98d2c-126">-Tagi</span><span class="sxs-lookup"><span data-stu-id="98d2c-126">-Tags</span></span>
<span data-ttu-id="98d2c-127">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="98d2c-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="98d2c-128">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="98d2c-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="98d2c-129">-Type</span><span class="sxs-lookup"><span data-stu-id="98d2c-129">-Type</span></span>
<span data-ttu-id="98d2c-130">Określa typ elementu Runbook tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98d2c-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="98d2c-131">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="98d2c-131">Valid values are:</span></span>
- <span data-ttu-id="98d2c-132">Narzędzia</span><span class="sxs-lookup"><span data-stu-id="98d2c-132">PowerShell</span></span>
- <span data-ttu-id="98d2c-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="98d2c-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="98d2c-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="98d2c-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="98d2c-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="98d2c-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="98d2c-136">Wykres wartość jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="98d2c-136">Graph The value Graph is obsolete.</span></span>
<span data-ttu-id="98d2c-137">Jest to równoznaczne z GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="98d2c-137">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d2c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d2c-138">CommonParameters</span></span>
<span data-ttu-id="98d2c-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98d2c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d2c-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98d2c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d2c-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98d2c-141">INPUTS</span></span>

### <span data-ttu-id="98d2c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="98d2c-142">System.String</span></span>

### <span data-ttu-id="98d2c-143">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="98d2c-143">System.Collections.IDictionary</span></span>

### <span data-ttu-id="98d2c-144">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="98d2c-144">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="98d2c-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98d2c-145">OUTPUTS</span></span>

### <span data-ttu-id="98d2c-146">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="98d2c-146">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="98d2c-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98d2c-147">NOTES</span></span>

## <span data-ttu-id="98d2c-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98d2c-148">RELATED LINKS</span></span>

[<span data-ttu-id="98d2c-149">Eksportowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98d2c-149">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="98d2c-150">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98d2c-150">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="98d2c-151">Import — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98d2c-151">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="98d2c-152">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98d2c-152">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="98d2c-153">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98d2c-153">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="98d2c-154">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98d2c-154">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="98d2c-155">Start — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="98d2c-155">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
