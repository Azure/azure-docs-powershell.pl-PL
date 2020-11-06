---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/publish-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: e3d60cf277402ac23764b538ba6492ef5c424219
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547639"
---
# <span data-ttu-id="32d10-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32d10-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="32d10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32d10-102">SYNOPSIS</span></span>
<span data-ttu-id="32d10-103">Umożliwia opublikowanie elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="32d10-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32d10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32d10-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32d10-105">Opis</span><span class="sxs-lookup"><span data-stu-id="32d10-105">DESCRIPTION</span></span>
<span data-ttu-id="32d10-106">Polecenie cmdlet **Publish-AzureRmAutomationRunbook** umożliwia publikowanie elementu Runbook do użycia w środowisku produkcyjnym usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="32d10-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="32d10-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32d10-107">EXAMPLES</span></span>

### <span data-ttu-id="32d10-108">Przykład 1. publikowanie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="32d10-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="32d10-109">To polecenie umożliwia opublikowanie elementu Runbook o nazwie Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="32d10-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="32d10-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32d10-110">PARAMETERS</span></span>

### <span data-ttu-id="32d10-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="32d10-111">-AutomationAccountName</span></span>
<span data-ttu-id="32d10-112">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet publikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="32d10-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="32d10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d10-113">-DefaultProfile</span></span>
<span data-ttu-id="32d10-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="32d10-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32d10-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="32d10-115">-Name</span></span>
<span data-ttu-id="32d10-116">Określa nazwę elementu Runbook, który jest publikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32d10-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="32d10-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32d10-117">-ResourceGroupName</span></span>
<span data-ttu-id="32d10-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet publikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="32d10-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="32d10-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d10-119">CommonParameters</span></span>
<span data-ttu-id="32d10-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32d10-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d10-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32d10-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d10-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32d10-122">INPUTS</span></span>

### <span data-ttu-id="32d10-123">System. String</span><span class="sxs-lookup"><span data-stu-id="32d10-123">System.String</span></span>

## <span data-ttu-id="32d10-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32d10-124">OUTPUTS</span></span>

### <span data-ttu-id="32d10-125">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="32d10-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="32d10-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32d10-126">NOTES</span></span>

## <span data-ttu-id="32d10-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32d10-127">RELATED LINKS</span></span>

[<span data-ttu-id="32d10-128">Eksportowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32d10-128">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32d10-129">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32d10-129">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32d10-130">Import — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32d10-130">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32d10-131">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32d10-131">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32d10-132">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32d10-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32d10-133">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32d10-133">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32d10-134">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32d10-134">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="32d10-135">Start — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="32d10-135">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


