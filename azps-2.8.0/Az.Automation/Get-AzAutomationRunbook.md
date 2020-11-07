---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: 1b07ff07008c0af80a72c32ed64d6845d632db15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706804"
---
# <span data-ttu-id="a8ffe-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8ffe-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="a8ffe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ffe-103">Pobiera element Runbook.</span><span class="sxs-lookup"><span data-stu-id="a8ffe-103">Gets a runbook.</span></span>

## <span data-ttu-id="a8ffe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8ffe-104">SYNTAX</span></span>

### <span data-ttu-id="a8ffe-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a8ffe-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8ffe-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="a8ffe-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8ffe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a8ffe-107">DESCRIPTION</span></span>
<span data-ttu-id="a8ffe-108">Polecenie cmdlet **Get-AzAutomationRunbook** Pobiera elementy Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a8ffe-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="a8ffe-109">Aby uzyskać określony element Runbook, określ jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="a8ffe-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="a8ffe-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8ffe-110">EXAMPLES</span></span>

### <span data-ttu-id="a8ffe-111">Przykład 1. pobieranie wszystkich elementów Runbook</span><span class="sxs-lookup"><span data-stu-id="a8ffe-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a8ffe-112">To polecenie pobiera wszystkie elementy Runbook z konta usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a8ffe-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a8ffe-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8ffe-113">PARAMETERS</span></span>

### <span data-ttu-id="a8ffe-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a8ffe-114">-AutomationAccountName</span></span>
<span data-ttu-id="a8ffe-115">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet pobiera elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="a8ffe-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="a8ffe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ffe-116">-DefaultProfile</span></span>
<span data-ttu-id="a8ffe-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a8ffe-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8ffe-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a8ffe-118">-Name</span></span>
<span data-ttu-id="a8ffe-119">Określa nazwę elementu Runbook, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ffe-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a8ffe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ffe-120">-ResourceGroupName</span></span>
<span data-ttu-id="a8ffe-121">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="a8ffe-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="a8ffe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ffe-122">CommonParameters</span></span>
<span data-ttu-id="a8ffe-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ffe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ffe-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8ffe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ffe-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8ffe-125">INPUTS</span></span>

### <span data-ttu-id="a8ffe-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a8ffe-126">System.String</span></span>

## <span data-ttu-id="a8ffe-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8ffe-127">OUTPUTS</span></span>

### <span data-ttu-id="a8ffe-128">Microsoft. Azure. Commands. Automation. model. Runbook</span><span class="sxs-lookup"><span data-stu-id="a8ffe-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="a8ffe-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8ffe-129">NOTES</span></span>

## <span data-ttu-id="a8ffe-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8ffe-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8ffe-131">Eksportowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8ffe-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="a8ffe-132">Import — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8ffe-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="a8ffe-133">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8ffe-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a8ffe-134">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8ffe-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a8ffe-135">Publikowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8ffe-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="a8ffe-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8ffe-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="a8ffe-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8ffe-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="a8ffe-138">Start — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a8ffe-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


