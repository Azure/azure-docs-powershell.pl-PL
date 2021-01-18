---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: feca8adfbfe24ce006c2fc5f52618f43591fa0b4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502303"
---
# <span data-ttu-id="6fa4b-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6fa4b-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="6fa4b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fa4b-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa4b-103">Umożliwia opublikowanie elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="6fa4b-103">Publishes a runbook.</span></span>

## <span data-ttu-id="6fa4b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fa4b-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fa4b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6fa4b-105">DESCRIPTION</span></span>
<span data-ttu-id="6fa4b-106">Polecenie cmdlet **Publish-AzAutomationRunbook** umożliwia publikowanie elementu Runbook do użycia w środowisku produkcyjnym usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6fa4b-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="6fa4b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fa4b-107">EXAMPLES</span></span>

### <span data-ttu-id="6fa4b-108">Przykład 1. publikowanie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="6fa4b-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6fa4b-109">To polecenie umożliwia opublikowanie elementu Runbook o nazwie Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6fa4b-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="6fa4b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fa4b-110">PARAMETERS</span></span>

### <span data-ttu-id="6fa4b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6fa4b-111">-AutomationAccountName</span></span>
<span data-ttu-id="6fa4b-112">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet publikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="6fa4b-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="6fa4b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fa4b-113">-DefaultProfile</span></span>
<span data-ttu-id="6fa4b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6fa4b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fa4b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6fa4b-115">-Name</span></span>
<span data-ttu-id="6fa4b-116">Określa nazwę elementu Runbook, który jest publikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fa4b-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="6fa4b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fa4b-117">-ResourceGroupName</span></span>
<span data-ttu-id="6fa4b-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet publikuje element Runbook.</span><span class="sxs-lookup"><span data-stu-id="6fa4b-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="6fa4b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fa4b-119">CommonParameters</span></span>
<span data-ttu-id="6fa4b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fa4b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fa4b-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fa4b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fa4b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fa4b-122">INPUTS</span></span>

### <span data-ttu-id="6fa4b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6fa4b-123">System.String</span></span>

## <span data-ttu-id="6fa4b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fa4b-124">OUTPUTS</span></span>

### <span data-ttu-id="6fa4b-125">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="6fa4b-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="6fa4b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fa4b-126">NOTES</span></span>

## <span data-ttu-id="6fa4b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fa4b-127">RELATED LINKS</span></span>

[<span data-ttu-id="6fa4b-128">Eksportowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6fa4b-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="6fa4b-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6fa4b-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="6fa4b-130">Import — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6fa4b-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="6fa4b-131">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6fa4b-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="6fa4b-132">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6fa4b-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="6fa4b-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6fa4b-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="6fa4b-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6fa4b-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="6fa4b-135">Start — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6fa4b-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


