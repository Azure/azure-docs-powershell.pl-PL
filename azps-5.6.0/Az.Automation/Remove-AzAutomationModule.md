---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 9fa84ffed6352dfb566ad02aa2393a7cba7f393b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009898"
---
# <span data-ttu-id="0bf90-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0bf90-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="0bf90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bf90-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf90-103">Usuwa moduł z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="0bf90-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="0bf90-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0bf90-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0bf90-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0bf90-105">DESCRIPTION</span></span>
<span data-ttu-id="0bf90-106">Polecenie **cmdlet Remove-AzAutomationModule** usuwa moduł z konta automatyzacji w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0bf90-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="0bf90-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0bf90-107">EXAMPLES</span></span>

### <span data-ttu-id="0bf90-108">Przykład 1. Usuwanie modułu</span><span class="sxs-lookup"><span data-stu-id="0bf90-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0bf90-109">To polecenie usuwa moduł o nazwie ContosoModule z konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0bf90-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0bf90-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bf90-110">PARAMETERS</span></span>

### <span data-ttu-id="0bf90-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0bf90-111">-AutomationAccountName</span></span>
<span data-ttu-id="0bf90-112">Określa nazwę konta automatyzacji, z którego to polecenie cmdlet usuwa moduł.</span><span class="sxs-lookup"><span data-stu-id="0bf90-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="0bf90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bf90-113">-DefaultProfile</span></span>
<span data-ttu-id="0bf90-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0bf90-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bf90-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0bf90-115">-Force</span></span>
<span data-ttu-id="0bf90-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="0bf90-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bf90-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0bf90-117">-Name</span></span>
<span data-ttu-id="0bf90-118">Określa nazwę modułu, który zostanie usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bf90-118">Specifies the name of the module that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bf90-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bf90-119">-ResourceGroupName</span></span>
<span data-ttu-id="0bf90-120">Określa nazwę grupy zasobów, w której to polecenie cmdlet usuwa moduł.</span><span class="sxs-lookup"><span data-stu-id="0bf90-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="0bf90-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0bf90-121">-Confirm</span></span>
<span data-ttu-id="0bf90-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0bf90-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bf90-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bf90-123">-WhatIf</span></span>
<span data-ttu-id="0bf90-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bf90-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bf90-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0bf90-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bf90-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf90-126">CommonParameters</span></span>
<span data-ttu-id="0bf90-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bf90-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf90-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bf90-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf90-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bf90-129">INPUTS</span></span>

### <span data-ttu-id="0bf90-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0bf90-130">System.String</span></span>

## <span data-ttu-id="0bf90-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bf90-131">OUTPUTS</span></span>

### <span data-ttu-id="0bf90-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="0bf90-132">System.Void</span></span>

## <span data-ttu-id="0bf90-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0bf90-133">NOTES</span></span>

## <span data-ttu-id="0bf90-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0bf90-134">RELATED LINKS</span></span>

[<span data-ttu-id="0bf90-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0bf90-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="0bf90-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0bf90-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="0bf90-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0bf90-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


