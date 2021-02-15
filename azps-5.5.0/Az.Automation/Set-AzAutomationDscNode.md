---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
ms.openlocfilehash: 02a6d7a129dc084b982f1827d678354265ddbc66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182139"
---
# <span data-ttu-id="ab921-101">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ab921-101">Set-AzAutomationDscNode</span></span>

## <span data-ttu-id="ab921-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab921-102">SYNOPSIS</span></span>
<span data-ttu-id="ab921-103">Modyfikuje konfigurację węzła, na który jest zamapowany węzeł DSC.</span><span class="sxs-lookup"><span data-stu-id="ab921-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

## <span data-ttu-id="ab921-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ab921-104">SYNTAX</span></span>

```
Set-AzAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab921-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ab921-105">DESCRIPTION</span></span>
<span data-ttu-id="ab921-106">Polecenie cmdlet **Set-AzAutomationDscNode** modyfikuje konfigurację węzła APS Desired State Configuration (DSC).</span><span class="sxs-lookup"><span data-stu-id="ab921-106">The **Set-AzAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="ab921-107">Usługa Azure Automation przechowuje konfigurację węzła DSC jako dokument konfiguracji formatu zarządzanego obiektu (MOF).</span><span class="sxs-lookup"><span data-stu-id="ab921-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="ab921-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ab921-108">EXAMPLES</span></span>

### <span data-ttu-id="ab921-109">Przykład 1. Modyfikowanie mapowania konfiguracji węzła</span><span class="sxs-lookup"><span data-stu-id="ab921-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="ab921-110">To polecenie przypisuje konfigurację węzła o nazwie Contoso.NodeConfiguration01 do węzła o określonym identyfikatorze GUID.</span><span class="sxs-lookup"><span data-stu-id="ab921-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="ab921-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab921-111">PARAMETERS</span></span>

### <span data-ttu-id="ab921-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ab921-112">-AutomationAccountName</span></span>
<span data-ttu-id="ab921-113">Określa nazwę konta automatyzacji zawierającego węzeł DSC, dla którego to polecenie cmdlet zmodyfikuje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="ab921-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="ab921-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab921-114">-DefaultProfile</span></span>
<span data-ttu-id="ab921-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ab921-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab921-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ab921-116">-Force</span></span>
<span data-ttu-id="ab921-117">ps_force uruchomić polecenie bez pytania o potwierdzenie od użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ab921-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab921-118">— Id</span><span class="sxs-lookup"><span data-stu-id="ab921-118">-Id</span></span>
<span data-ttu-id="ab921-119">Określa unikatowy identyfikator węzła DSC, dla którego to polecenie cmdlet modyfikuje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="ab921-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab921-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ab921-120">-NodeConfigurationName</span></span>
<span data-ttu-id="ab921-121">Określa nazwę konfiguracji węzła, do której to polecenie cmdlet mapuje węzeł.</span><span class="sxs-lookup"><span data-stu-id="ab921-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab921-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab921-122">-ResourceGroupName</span></span>
<span data-ttu-id="ab921-123">Określa nazwę grupy zasobów, w której to polecenie cmdlet modyfikuje konfigurację węzła DSC.</span><span class="sxs-lookup"><span data-stu-id="ab921-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="ab921-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab921-124">-Confirm</span></span>
<span data-ttu-id="ab921-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ab921-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab921-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab921-126">-WhatIf</span></span>
<span data-ttu-id="ab921-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab921-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab921-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ab921-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab921-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab921-129">CommonParameters</span></span>
<span data-ttu-id="ab921-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab921-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab921-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab921-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab921-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab921-132">INPUTS</span></span>

### <span data-ttu-id="ab921-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ab921-133">System.Guid</span></span>

### <span data-ttu-id="ab921-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ab921-134">System.String</span></span>

## <span data-ttu-id="ab921-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab921-135">OUTPUTS</span></span>

### <span data-ttu-id="ab921-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="ab921-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="ab921-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ab921-137">NOTES</span></span>

## <span data-ttu-id="ab921-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab921-138">RELATED LINKS</span></span>

[<span data-ttu-id="ab921-139">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ab921-139">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="ab921-140">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ab921-140">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="ab921-141">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ab921-141">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


