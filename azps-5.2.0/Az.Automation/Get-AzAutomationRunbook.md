---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373807"
---
# <span data-ttu-id="cefff-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cefff-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="cefff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cefff-102">SYNOPSIS</span></span>
<span data-ttu-id="cefff-103">Pobiera element Runbook.</span><span class="sxs-lookup"><span data-stu-id="cefff-103">Gets a runbook.</span></span>

## <span data-ttu-id="cefff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cefff-104">SYNTAX</span></span>

### <span data-ttu-id="cefff-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cefff-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cefff-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="cefff-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cefff-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cefff-107">DESCRIPTION</span></span>
<span data-ttu-id="cefff-108">Polecenie cmdlet **Get-AzAutomationRunbook** Pobiera elementy Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="cefff-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="cefff-109">Aby uzyskać określony element Runbook, określ jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="cefff-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="cefff-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cefff-110">EXAMPLES</span></span>

### <span data-ttu-id="cefff-111">Przykład 1. pobieranie wszystkich elementów Runbook</span><span class="sxs-lookup"><span data-stu-id="cefff-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cefff-112">To polecenie pobiera wszystkie elementy Runbook z konta usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cefff-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="cefff-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cefff-113">PARAMETERS</span></span>

### <span data-ttu-id="cefff-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cefff-114">-AutomationAccountName</span></span>
<span data-ttu-id="cefff-115">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet pobiera elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="cefff-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="cefff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cefff-116">-DefaultProfile</span></span>
<span data-ttu-id="cefff-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cefff-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cefff-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cefff-118">-Name</span></span>
<span data-ttu-id="cefff-119">Określa nazwę elementu Runbook, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cefff-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cefff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cefff-120">-ResourceGroupName</span></span>
<span data-ttu-id="cefff-121">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="cefff-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="cefff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cefff-122">CommonParameters</span></span>
<span data-ttu-id="cefff-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cefff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cefff-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cefff-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cefff-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cefff-125">INPUTS</span></span>

### <span data-ttu-id="cefff-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cefff-126">System.String</span></span>

## <span data-ttu-id="cefff-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cefff-127">OUTPUTS</span></span>

### <span data-ttu-id="cefff-128">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="cefff-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="cefff-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cefff-129">NOTES</span></span>

## <span data-ttu-id="cefff-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cefff-130">RELATED LINKS</span></span>

[<span data-ttu-id="cefff-131">Eksportowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cefff-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="cefff-132">Import — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cefff-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="cefff-133">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cefff-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="cefff-134">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cefff-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="cefff-135">Publikowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cefff-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="cefff-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cefff-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="cefff-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cefff-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="cefff-138">Start — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cefff-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


