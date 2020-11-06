---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 664bfb83be4394c5aa50213177eda9f16f5ec6b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547115"
---
# <span data-ttu-id="168ed-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="168ed-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="168ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="168ed-102">SYNOPSIS</span></span>
<span data-ttu-id="168ed-103">Tworzy element Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="168ed-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="168ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="168ed-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="168ed-105">Opis</span><span class="sxs-lookup"><span data-stu-id="168ed-105">DESCRIPTION</span></span>
<span data-ttu-id="168ed-106">Polecenie cmdlet **New-AzureRmAutomationRunbook** tworzy pusty element Runbook usługi Azure Automation za pomocą funkcji APS.</span><span class="sxs-lookup"><span data-stu-id="168ed-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="168ed-107">Określ nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="168ed-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="168ed-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="168ed-108">EXAMPLES</span></span>

### <span data-ttu-id="168ed-109">Przykład 1. Tworzenie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="168ed-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="168ed-110">To polecenie tworzy element Runbook o nazwie Runbook02 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="168ed-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="168ed-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="168ed-111">PARAMETERS</span></span>

### <span data-ttu-id="168ed-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="168ed-112">-AutomationAccountName</span></span>
<span data-ttu-id="168ed-113">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet tworzy element Runbook.</span><span class="sxs-lookup"><span data-stu-id="168ed-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="168ed-114">— Opis</span><span class="sxs-lookup"><span data-stu-id="168ed-114">-Description</span></span>
<span data-ttu-id="168ed-115">Określa opis elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="168ed-115">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="168ed-116">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="168ed-116">-LogProgress</span></span>
<span data-ttu-id="168ed-117">Określa, czy element Runbook rejestruje postęp.</span><span class="sxs-lookup"><span data-stu-id="168ed-117">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="168ed-118">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="168ed-118">-LogVerbose</span></span>
<span data-ttu-id="168ed-119">Określa, czy rejestrowanie zawiera szczegółowe informacje.</span><span class="sxs-lookup"><span data-stu-id="168ed-119">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="168ed-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="168ed-120">-Name</span></span>
<span data-ttu-id="168ed-121">Określa nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="168ed-121">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="168ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="168ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="168ed-123">Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy element Runbook.</span><span class="sxs-lookup"><span data-stu-id="168ed-123">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="168ed-124">-Tagi</span><span class="sxs-lookup"><span data-stu-id="168ed-124">-Tags</span></span>
<span data-ttu-id="168ed-125">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="168ed-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="168ed-126">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="168ed-126">For example:</span></span>

<span data-ttu-id="168ed-127">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="168ed-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="168ed-128">-Type</span><span class="sxs-lookup"><span data-stu-id="168ed-128">-Type</span></span>
<span data-ttu-id="168ed-129">Określa typ elementu Runbook tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="168ed-129">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="168ed-130">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="168ed-130">Valid values are:</span></span>

- <span data-ttu-id="168ed-131">Narzędzia</span><span class="sxs-lookup"><span data-stu-id="168ed-131">PowerShell</span></span>
- <span data-ttu-id="168ed-132">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="168ed-132">GraphicalPowerShell</span></span>
- <span data-ttu-id="168ed-133">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="168ed-133">PowerShellWorkflow</span></span>
- <span data-ttu-id="168ed-134">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="168ed-134">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="168ed-135">Graf</span><span class="sxs-lookup"><span data-stu-id="168ed-135">Graph</span></span>

<span data-ttu-id="168ed-136">Wykres wartości jest przestarzały.</span><span class="sxs-lookup"><span data-stu-id="168ed-136">The value Graph is obsolete.</span></span>
<span data-ttu-id="168ed-137">Jest to równoznaczne z GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="168ed-137">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="168ed-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="168ed-138">-DefaultProfile</span></span>
<span data-ttu-id="168ed-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="168ed-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="168ed-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="168ed-140">CommonParameters</span></span>
<span data-ttu-id="168ed-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="168ed-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="168ed-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="168ed-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="168ed-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="168ed-143">INPUTS</span></span>

## <span data-ttu-id="168ed-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="168ed-144">OUTPUTS</span></span>

### <span data-ttu-id="168ed-145">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="168ed-145">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="168ed-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="168ed-146">NOTES</span></span>

## <span data-ttu-id="168ed-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="168ed-147">RELATED LINKS</span></span>

[<span data-ttu-id="168ed-148">Eksportowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="168ed-148">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="168ed-149">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="168ed-149">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="168ed-150">Import — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="168ed-150">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="168ed-151">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="168ed-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="168ed-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="168ed-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="168ed-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="168ed-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="168ed-154">Start — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="168ed-154">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
