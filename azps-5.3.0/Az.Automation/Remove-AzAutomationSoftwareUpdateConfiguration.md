---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: bd5e51b8951d2b246036b45ddddf3d1bbe4b8e4e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502281"
---
# <span data-ttu-id="bf320-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf320-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="bf320-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf320-102">SYNOPSIS</span></span>
<span data-ttu-id="bf320-103">Usuwa konfigurację aktualizacji oprogramowania Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="bf320-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="bf320-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf320-104">SYNTAX</span></span>

### <span data-ttu-id="bf320-105">BySucName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bf320-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf320-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="bf320-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf320-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bf320-107">DESCRIPTION</span></span>
<span data-ttu-id="bf320-108">To polecenie cmdlet usunęło konfigurację aktualizacji oprogramowania Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="bf320-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="bf320-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf320-109">EXAMPLES</span></span>

### <span data-ttu-id="bf320-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bf320-110">Example 1</span></span>
<span data-ttu-id="bf320-111">W tym przykładzie pokazano, jak usunąć MyUpdateConfiguration ' z konta usługi Automation</span><span class="sxs-lookup"><span data-stu-id="bf320-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="bf320-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf320-112">PARAMETERS</span></span>

### <span data-ttu-id="bf320-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bf320-113">-AutomationAccountName</span></span>
<span data-ttu-id="bf320-114">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="bf320-114">The automation account name.</span></span>

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

### <span data-ttu-id="bf320-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf320-115">-DefaultProfile</span></span>
<span data-ttu-id="bf320-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf320-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf320-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf320-117">-Name</span></span>
<span data-ttu-id="bf320-118">Nazwa konfiguracji aktualizacji oprogramowania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="bf320-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="bf320-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf320-119">-PassThru</span></span>
<span data-ttu-id="bf320-120">PassThru zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="bf320-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="bf320-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="bf320-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf320-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf320-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf320-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf320-123">The resource group name.</span></span>

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

### <span data-ttu-id="bf320-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf320-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="bf320-125">Konfiguracja aktualizacji oprogramowania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="bf320-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="bf320-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf320-126">-Confirm</span></span>
<span data-ttu-id="bf320-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf320-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf320-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf320-128">-WhatIf</span></span>
<span data-ttu-id="bf320-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf320-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf320-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bf320-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf320-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf320-131">CommonParameters</span></span>
<span data-ttu-id="bf320-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf320-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf320-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf320-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf320-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf320-134">INPUTS</span></span>

### <span data-ttu-id="bf320-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bf320-135">System.String</span></span>

### <span data-ttu-id="bf320-136">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf320-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="bf320-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf320-137">OUTPUTS</span></span>

### <span data-ttu-id="bf320-138">System. void</span><span class="sxs-lookup"><span data-stu-id="bf320-138">System.Void</span></span>

### <span data-ttu-id="bf320-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf320-139">System.Boolean</span></span>

## <span data-ttu-id="bf320-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf320-140">NOTES</span></span>

## <span data-ttu-id="bf320-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf320-141">RELATED LINKS</span></span>
