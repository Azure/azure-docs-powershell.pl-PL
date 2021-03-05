---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: fa10c44186de06de758e4f7878bb7c8da61c4d6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004801"
---
# <span data-ttu-id="fe425-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fe425-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="fe425-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe425-102">SYNOPSIS</span></span>
<span data-ttu-id="fe425-103">Publikuje podręcznik.</span><span class="sxs-lookup"><span data-stu-id="fe425-103">Publishes a runbook.</span></span>

## <span data-ttu-id="fe425-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe425-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe425-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe425-105">DESCRIPTION</span></span>
<span data-ttu-id="fe425-106">Polecenie cmdlet **Publish-AzAutomationRunbook** publikuje podręcznik do użycia w środowisku produkcyjnym usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="fe425-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="fe425-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe425-107">EXAMPLES</span></span>

### <span data-ttu-id="fe425-108">Przykład 1. Publikowanie podręcznika</span><span class="sxs-lookup"><span data-stu-id="fe425-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fe425-109">To polecenie publikuje podręcznik Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="fe425-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="fe425-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe425-110">PARAMETERS</span></span>

### <span data-ttu-id="fe425-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fe425-111">-AutomationAccountName</span></span>
<span data-ttu-id="fe425-112">Określa nazwę konta automatyzacji, na którym to polecenie cmdlet publikuje podręcznik.</span><span class="sxs-lookup"><span data-stu-id="fe425-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="fe425-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe425-113">-DefaultProfile</span></span>
<span data-ttu-id="fe425-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fe425-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe425-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fe425-115">-Name</span></span>
<span data-ttu-id="fe425-116">Określa nazwę podręcznika, który jest publikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe425-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="fe425-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe425-117">-ResourceGroupName</span></span>
<span data-ttu-id="fe425-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet publikuje podręcznik.</span><span class="sxs-lookup"><span data-stu-id="fe425-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="fe425-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe425-119">CommonParameters</span></span>
<span data-ttu-id="fe425-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe425-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe425-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe425-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe425-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe425-122">INPUTS</span></span>

### <span data-ttu-id="fe425-123">System.String</span><span class="sxs-lookup"><span data-stu-id="fe425-123">System.String</span></span>

## <span data-ttu-id="fe425-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe425-124">OUTPUTS</span></span>

### <span data-ttu-id="fe425-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="fe425-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="fe425-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe425-126">NOTES</span></span>

## <span data-ttu-id="fe425-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe425-127">RELATED LINKS</span></span>

[<span data-ttu-id="fe425-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fe425-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="fe425-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fe425-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="fe425-130">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fe425-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="fe425-131">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fe425-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="fe425-132">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fe425-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="fe425-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fe425-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="fe425-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fe425-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="fe425-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fe425-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


