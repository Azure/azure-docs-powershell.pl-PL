---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 938fde14fb62ea7f7fd4e04baf5e309615957799
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710497"
---
# <span data-ttu-id="efd4c-101">Remove-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="efd4c-101">Remove-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="efd4c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="efd4c-102">SYNOPSIS</span></span>
<span data-ttu-id="efd4c-103">Usuwa metadane z konfiguracji węzłów DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="efd4c-103">Removes metadata from DSC node configurations in Automation.</span></span>

## <span data-ttu-id="efd4c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="efd4c-104">SYNTAX</span></span>

```
Remove-AzAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efd4c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="efd4c-105">DESCRIPTION</span></span>
<span data-ttu-id="efd4c-106">Polecenie cmdlet **Remove-AzAutomationDscNodeConfiguration** usuwa metadane z konfiguracji węzłów konfiguracji stanu żądanego (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="efd4c-106">The **Remove-AzAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="efd4c-107">Konfiguracja węzła DSC jest przechowywana w dokumencie konfiguracyjnym Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="efd4c-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="efd4c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="efd4c-108">EXAMPLES</span></span>

## <span data-ttu-id="efd4c-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="efd4c-109">PARAMETERS</span></span>

### <span data-ttu-id="efd4c-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="efd4c-110">-AutomationAccountName</span></span>
<span data-ttu-id="efd4c-111">Określa nazwę konta usługi Automation, które zawiera konfiguracje węzła DSC, dla których to polecenie cmdlet usuwa metadane.</span><span class="sxs-lookup"><span data-stu-id="efd4c-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="efd4c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd4c-112">-DefaultProfile</span></span>
<span data-ttu-id="efd4c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="efd4c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efd4c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="efd4c-114">-Force</span></span>
<span data-ttu-id="efd4c-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="efd4c-115">ps_force</span></span>

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

### <span data-ttu-id="efd4c-116">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="efd4c-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="efd4c-117">Wskazuje, że ten aplet polecenia ignoruje mapowania węzłów.</span><span class="sxs-lookup"><span data-stu-id="efd4c-117">Indicates that this cmdlet ignores node mappings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd4c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="efd4c-118">-Name</span></span>
<span data-ttu-id="efd4c-119">Określa nazwę konfiguracji węzła DSC, dla której to polecenie cmdlet usuwa metadane.</span><span class="sxs-lookup"><span data-stu-id="efd4c-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efd4c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efd4c-120">-ResourceGroupName</span></span>
<span data-ttu-id="efd4c-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="efd4c-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="efd4c-122">To polecenie cmdlet usuwa metadane konfiguracji węzłów DSC w grupie zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="efd4c-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="efd4c-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="efd4c-123">-Confirm</span></span>
<span data-ttu-id="efd4c-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efd4c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efd4c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efd4c-125">-WhatIf</span></span>
<span data-ttu-id="efd4c-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efd4c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efd4c-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="efd4c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efd4c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd4c-128">CommonParameters</span></span>
<span data-ttu-id="efd4c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efd4c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd4c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efd4c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd4c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efd4c-131">INPUTS</span></span>

### <span data-ttu-id="efd4c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="efd4c-132">System.String</span></span>

## <span data-ttu-id="efd4c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="efd4c-133">OUTPUTS</span></span>

### <span data-ttu-id="efd4c-134">System. void</span><span class="sxs-lookup"><span data-stu-id="efd4c-134">System.Void</span></span>

## <span data-ttu-id="efd4c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="efd4c-135">NOTES</span></span>

## <span data-ttu-id="efd4c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efd4c-136">RELATED LINKS</span></span>

[<span data-ttu-id="efd4c-137">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="efd4c-137">Get-AzAutomationDscNodeConfiguration</span></span>](./Get-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="efd4c-138">Import — AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="efd4c-138">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="efd4c-139">Polecenia cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="efd4c-139">Azure Automation Cmdlets</span></span>](./Az.Automation.md)


