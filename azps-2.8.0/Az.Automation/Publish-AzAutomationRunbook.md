---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: 1d3ea7321efaae0f9d1107e3d1e87fd3c432656f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706747"
---
# <span data-ttu-id="0b8ee-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0b8ee-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="0b8ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="0b8ee-103">Umożliwia opublikowanie elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="0b8ee-103">Publishes a runbook.</span></span>

## <span data-ttu-id="0b8ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b8ee-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b8ee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0b8ee-105">DESCRIPTION</span></span>
<span data-ttu-id="0b8ee-106">Polecenie cmdlet **Publish-AzAutomationRunbook** umożliwia publikowanie elementu Runbook do użycia w środowisku produkcyjnym usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0b8ee-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="0b8ee-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b8ee-107">EXAMPLES</span></span>

### <span data-ttu-id="0b8ee-108">Przykład 1. publikowanie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="0b8ee-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0b8ee-109">To polecenie umożliwia opublikowanie elementu Runbook o nazwie Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0b8ee-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="0b8ee-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b8ee-110">PARAMETERS</span></span>

### <span data-ttu-id="0b8ee-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0b8ee-111">-AutomationAccountName</span></span>
<span data-ttu-id="0b8ee-112">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet publikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="0b8ee-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="0b8ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b8ee-113">-DefaultProfile</span></span>
<span data-ttu-id="0b8ee-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0b8ee-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b8ee-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0b8ee-115">-Name</span></span>
<span data-ttu-id="0b8ee-116">Określa nazwę elementu Runbook, który jest publikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b8ee-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="0b8ee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b8ee-117">-ResourceGroupName</span></span>
<span data-ttu-id="0b8ee-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet publikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="0b8ee-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="0b8ee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b8ee-119">CommonParameters</span></span>
<span data-ttu-id="0b8ee-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b8ee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b8ee-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b8ee-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b8ee-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b8ee-122">INPUTS</span></span>

### <span data-ttu-id="0b8ee-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0b8ee-123">System.String</span></span>

## <span data-ttu-id="0b8ee-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b8ee-124">OUTPUTS</span></span>

### <span data-ttu-id="0b8ee-125">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="0b8ee-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="0b8ee-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b8ee-126">NOTES</span></span>

## <span data-ttu-id="0b8ee-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b8ee-127">RELATED LINKS</span></span>

[<span data-ttu-id="0b8ee-128">Eksportowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0b8ee-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="0b8ee-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0b8ee-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="0b8ee-130">Import — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0b8ee-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="0b8ee-131">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0b8ee-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="0b8ee-132">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0b8ee-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="0b8ee-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0b8ee-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="0b8ee-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0b8ee-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="0b8ee-135">Start — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0b8ee-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)

