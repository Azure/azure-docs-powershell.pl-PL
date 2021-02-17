---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239547"
---
# <span data-ttu-id="6dd49-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6dd49-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="6dd49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dd49-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd49-103">Usuwa moduł z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="6dd49-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="6dd49-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6dd49-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6dd49-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6dd49-105">DESCRIPTION</span></span>
<span data-ttu-id="6dd49-106">Polecenie **cmdlet Remove-AzAutomationModule** usuwa moduł z konta automatyzacji w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6dd49-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="6dd49-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6dd49-107">EXAMPLES</span></span>

### <span data-ttu-id="6dd49-108">Przykład 1. Usuwanie modułu</span><span class="sxs-lookup"><span data-stu-id="6dd49-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6dd49-109">To polecenie usuwa moduł o nazwie ContosoModule z konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6dd49-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6dd49-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dd49-110">PARAMETERS</span></span>

### <span data-ttu-id="6dd49-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6dd49-111">-AutomationAccountName</span></span>
<span data-ttu-id="6dd49-112">Określa nazwę konta automatyzacji, z którego to polecenie cmdlet usuwa moduł.</span><span class="sxs-lookup"><span data-stu-id="6dd49-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="6dd49-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd49-113">-DefaultProfile</span></span>
<span data-ttu-id="6dd49-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6dd49-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6dd49-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6dd49-115">-Force</span></span>
<span data-ttu-id="6dd49-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="6dd49-116">ps_force</span></span>

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

### <span data-ttu-id="6dd49-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6dd49-117">-Name</span></span>
<span data-ttu-id="6dd49-118">Określa nazwę modułu, który zostanie usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dd49-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6dd49-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dd49-119">-ResourceGroupName</span></span>
<span data-ttu-id="6dd49-120">Określa nazwę grupy zasobów, w której to polecenie cmdlet usuwa moduł.</span><span class="sxs-lookup"><span data-stu-id="6dd49-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="6dd49-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6dd49-121">-Confirm</span></span>
<span data-ttu-id="6dd49-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6dd49-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dd49-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dd49-123">-WhatIf</span></span>
<span data-ttu-id="6dd49-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dd49-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dd49-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6dd49-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dd49-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd49-126">CommonParameters</span></span>
<span data-ttu-id="6dd49-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dd49-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd49-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dd49-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd49-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6dd49-129">INPUTS</span></span>

### <span data-ttu-id="6dd49-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6dd49-130">System.String</span></span>

## <span data-ttu-id="6dd49-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6dd49-131">OUTPUTS</span></span>

### <span data-ttu-id="6dd49-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="6dd49-132">System.Void</span></span>

## <span data-ttu-id="6dd49-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6dd49-133">NOTES</span></span>

## <span data-ttu-id="6dd49-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6dd49-134">RELATED LINKS</span></span>

[<span data-ttu-id="6dd49-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6dd49-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="6dd49-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6dd49-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="6dd49-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6dd49-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


