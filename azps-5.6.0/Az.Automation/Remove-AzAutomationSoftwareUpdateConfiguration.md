---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 8ddc84e3fac5df9253ffdacb61d4f4c7a5568c6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957761"
---
# <span data-ttu-id="38197-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="38197-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="38197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38197-102">SYNOPSIS</span></span>
<span data-ttu-id="38197-103">Usuwa konfigurację aktualizacji oprogramowania Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="38197-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="38197-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="38197-104">SYNTAX</span></span>

### <span data-ttu-id="38197-105">BySucName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="38197-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38197-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="38197-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38197-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="38197-107">DESCRIPTION</span></span>
<span data-ttu-id="38197-108">To polecenie cmdlet usunąło konfigurację aktualizacji oprogramowania azure Automation.</span><span class="sxs-lookup"><span data-stu-id="38197-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="38197-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="38197-109">EXAMPLES</span></span>

### <span data-ttu-id="38197-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="38197-110">Example 1</span></span>
<span data-ttu-id="38197-111">W tym przykładzie pokazano, jak usunąć "MyUpdateConfiguration" z konta automatyzacji</span><span class="sxs-lookup"><span data-stu-id="38197-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="38197-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38197-112">PARAMETERS</span></span>

### <span data-ttu-id="38197-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="38197-113">-AutomationAccountName</span></span>
<span data-ttu-id="38197-114">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="38197-114">The automation account name.</span></span>

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

### <span data-ttu-id="38197-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38197-115">-DefaultProfile</span></span>
<span data-ttu-id="38197-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="38197-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38197-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="38197-117">-Name</span></span>
<span data-ttu-id="38197-118">Nazwa konfiguracji aktualizacji oprogramowania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="38197-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38197-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38197-119">-PassThru</span></span>
<span data-ttu-id="38197-120">Funkcja PassThru zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="38197-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="38197-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="38197-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38197-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38197-122">-ResourceGroupName</span></span>
<span data-ttu-id="38197-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="38197-123">The resource group name.</span></span>

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

### <span data-ttu-id="38197-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="38197-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="38197-125">Konfiguracja aktualizacji oprogramowania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="38197-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38197-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38197-126">-Confirm</span></span>
<span data-ttu-id="38197-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="38197-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38197-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38197-128">-WhatIf</span></span>
<span data-ttu-id="38197-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38197-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38197-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="38197-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38197-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38197-131">CommonParameters</span></span>
<span data-ttu-id="38197-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38197-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38197-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38197-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38197-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38197-134">INPUTS</span></span>

### <span data-ttu-id="38197-135">System.String</span><span class="sxs-lookup"><span data-stu-id="38197-135">System.String</span></span>

### <span data-ttu-id="38197-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="38197-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="38197-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38197-137">OUTPUTS</span></span>

### <span data-ttu-id="38197-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="38197-138">System.Void</span></span>

### <span data-ttu-id="38197-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38197-139">System.Boolean</span></span>

## <span data-ttu-id="38197-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="38197-140">NOTES</span></span>

## <span data-ttu-id="38197-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38197-141">RELATED LINKS</span></span>
