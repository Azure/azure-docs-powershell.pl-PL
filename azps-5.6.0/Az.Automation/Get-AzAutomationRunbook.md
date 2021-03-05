---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: 00d6908e244a54fb2dbd501f0d944fc9cfdbdff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014273"
---
# <span data-ttu-id="16dbc-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dbc-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="16dbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="16dbc-103">Otrzymuje podręcznik.</span><span class="sxs-lookup"><span data-stu-id="16dbc-103">Gets a runbook.</span></span>

## <span data-ttu-id="16dbc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="16dbc-104">SYNTAX</span></span>

### <span data-ttu-id="16dbc-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="16dbc-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16dbc-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="16dbc-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16dbc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="16dbc-107">DESCRIPTION</span></span>
<span data-ttu-id="16dbc-108">Polecenie **cmdlet Get-AzAutomationRunbook** otrzymuje uruchamianie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="16dbc-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="16dbc-109">Aby uzyskać określony podręcznik, określ jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="16dbc-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="16dbc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="16dbc-110">EXAMPLES</span></span>

### <span data-ttu-id="16dbc-111">Przykład 1. Uzyskiwanie wszystkich runbooków</span><span class="sxs-lookup"><span data-stu-id="16dbc-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="16dbc-112">To polecenie pobiera wszystkie podręczniki runbooks na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="16dbc-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="16dbc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16dbc-113">PARAMETERS</span></span>

### <span data-ttu-id="16dbc-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="16dbc-114">-AutomationAccountName</span></span>
<span data-ttu-id="16dbc-115">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet pobiera runbooks.</span><span class="sxs-lookup"><span data-stu-id="16dbc-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="16dbc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16dbc-116">-DefaultProfile</span></span>
<span data-ttu-id="16dbc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="16dbc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16dbc-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="16dbc-118">-Name</span></span>
<span data-ttu-id="16dbc-119">Określa nazwę podręcznika, do których otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16dbc-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="16dbc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16dbc-120">-ResourceGroupName</span></span>
<span data-ttu-id="16dbc-121">Określa nazwę grupy zasobów, dla której to polecenie cmdlet uzyskuje runbooks.</span><span class="sxs-lookup"><span data-stu-id="16dbc-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="16dbc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16dbc-122">CommonParameters</span></span>
<span data-ttu-id="16dbc-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16dbc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16dbc-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16dbc-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16dbc-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16dbc-125">INPUTS</span></span>

### <span data-ttu-id="16dbc-126">System.String</span><span class="sxs-lookup"><span data-stu-id="16dbc-126">System.String</span></span>

## <span data-ttu-id="16dbc-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16dbc-127">OUTPUTS</span></span>

### <span data-ttu-id="16dbc-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="16dbc-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="16dbc-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="16dbc-129">NOTES</span></span>

## <span data-ttu-id="16dbc-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16dbc-130">RELATED LINKS</span></span>

[<span data-ttu-id="16dbc-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dbc-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="16dbc-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dbc-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="16dbc-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dbc-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="16dbc-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dbc-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="16dbc-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dbc-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="16dbc-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dbc-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="16dbc-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dbc-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="16dbc-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="16dbc-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


