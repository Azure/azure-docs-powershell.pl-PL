---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 46c77e1538c367e38220a022bf3b84e796dd0ec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550700"
---
# <span data-ttu-id="3d226-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3d226-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="3d226-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d226-102">SYNOPSIS</span></span>
<span data-ttu-id="3d226-103">Modyfikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="3d226-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d226-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d226-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d226-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3d226-105">DESCRIPTION</span></span>
<span data-ttu-id="3d226-106">Polecenie cmdlet **Set-AzureRmAutomationRunbook** modyfikuje konfigurację elementu Runbook usługi Azure Automation w usłudze APS.</span><span class="sxs-lookup"><span data-stu-id="3d226-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="3d226-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d226-107">EXAMPLES</span></span>

### <span data-ttu-id="3d226-108">Przykład 1: Włączanie pełnego rejestrowania elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="3d226-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3d226-109">To polecenie umożliwia pełne rejestrowanie informacji o zadaniach określonego elementu Runbook na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3d226-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="3d226-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d226-110">PARAMETERS</span></span>

### <span data-ttu-id="3d226-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3d226-111">-AutomationAccountName</span></span>
<span data-ttu-id="3d226-112">Określa nazwę konta automatyzacji, w którym polecenie cmdlet modyfikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="3d226-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="3d226-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d226-113">-DefaultProfile</span></span>
<span data-ttu-id="3d226-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3d226-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d226-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="3d226-115">-Description</span></span>
<span data-ttu-id="3d226-116">Określa opis elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="3d226-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="3d226-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="3d226-117">-LogProgress</span></span>
<span data-ttu-id="3d226-118">Określa, czy element Runbook rejestruje postęp.</span><span class="sxs-lookup"><span data-stu-id="3d226-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="3d226-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="3d226-119">-LogVerbose</span></span>
<span data-ttu-id="3d226-120">Określa, czy rejestrowanie zawiera szczegółowe informacje.</span><span class="sxs-lookup"><span data-stu-id="3d226-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="3d226-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d226-121">-Name</span></span>
<span data-ttu-id="3d226-122">Określa nazwę elementu Runbook, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d226-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3d226-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d226-123">-ResourceGroupName</span></span>
<span data-ttu-id="3d226-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="3d226-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="3d226-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="3d226-125">-Tag</span></span>
<span data-ttu-id="3d226-126">Znaczniki elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="3d226-126">The runbook tags.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d226-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d226-127">CommonParameters</span></span>
<span data-ttu-id="3d226-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d226-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d226-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d226-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d226-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d226-130">INPUTS</span></span>

### <span data-ttu-id="3d226-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3d226-131">None</span></span>
<span data-ttu-id="3d226-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3d226-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d226-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d226-133">OUTPUTS</span></span>

### <span data-ttu-id="3d226-134">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="3d226-134">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="3d226-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d226-135">NOTES</span></span>

## <span data-ttu-id="3d226-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d226-136">RELATED LINKS</span></span>

[<span data-ttu-id="3d226-137">Eksportowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3d226-137">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3d226-138">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3d226-138">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3d226-139">Import — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3d226-139">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3d226-140">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3d226-140">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3d226-141">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3d226-141">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3d226-142">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3d226-142">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3d226-143">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3d226-143">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3d226-144">Start — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3d226-144">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


