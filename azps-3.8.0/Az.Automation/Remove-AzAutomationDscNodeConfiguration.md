---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 28add3b4bffe808be5391de3ddbac759c36f5820
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053898"
---
# <span data-ttu-id="8e9b8-101">Remove-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e9b8-101">Remove-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="8e9b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e9b8-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9b8-103">Usuwa metadane z konfiguracji węzłów DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="8e9b8-103">Removes metadata from DSC node configurations in Automation.</span></span>

## <span data-ttu-id="8e9b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e9b8-104">SYNTAX</span></span>

```
Remove-AzAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e9b8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8e9b8-105">DESCRIPTION</span></span>
<span data-ttu-id="8e9b8-106">Polecenie cmdlet **Remove-AzAutomationDscNodeConfiguration** usuwa metadane z konfiguracji węzłów konfiguracji stanu żądanego (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8e9b8-106">The **Remove-AzAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="8e9b8-107">Konfiguracja węzła DSC jest przechowywana w dokumencie konfiguracyjnym Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8e9b8-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="8e9b8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e9b8-108">EXAMPLES</span></span>

## <span data-ttu-id="8e9b8-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e9b8-109">PARAMETERS</span></span>

### <span data-ttu-id="8e9b8-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8e9b8-110">-AutomationAccountName</span></span>
<span data-ttu-id="8e9b8-111">Określa nazwę konta usługi Automation, które zawiera konfiguracje węzła DSC, dla których to polecenie cmdlet usuwa metadane.</span><span class="sxs-lookup"><span data-stu-id="8e9b8-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="8e9b8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9b8-112">-DefaultProfile</span></span>
<span data-ttu-id="8e9b8-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8e9b8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e9b8-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8e9b8-114">-Force</span></span>
<span data-ttu-id="8e9b8-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="8e9b8-115">ps_force</span></span>

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

### <span data-ttu-id="8e9b8-116">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="8e9b8-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="8e9b8-117">Wskazuje, że ten aplet polecenia ignoruje mapowania węzłów.</span><span class="sxs-lookup"><span data-stu-id="8e9b8-117">Indicates that this cmdlet ignores node mappings.</span></span>

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

### <span data-ttu-id="8e9b8-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e9b8-118">-Name</span></span>
<span data-ttu-id="8e9b8-119">Określa nazwę konfiguracji węzła DSC, dla której to polecenie cmdlet usuwa metadane.</span><span class="sxs-lookup"><span data-stu-id="8e9b8-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="8e9b8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e9b8-120">-ResourceGroupName</span></span>
<span data-ttu-id="8e9b8-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8e9b8-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8e9b8-122">To polecenie cmdlet usuwa metadane konfiguracji węzłów DSC w grupie zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="8e9b8-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e9b8-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e9b8-123">-Confirm</span></span>
<span data-ttu-id="8e9b8-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e9b8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e9b8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e9b8-125">-WhatIf</span></span>
<span data-ttu-id="8e9b8-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e9b8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e9b8-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e9b8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e9b8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9b8-128">CommonParameters</span></span>
<span data-ttu-id="8e9b8-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e9b8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9b8-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e9b8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9b8-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e9b8-131">INPUTS</span></span>

### <span data-ttu-id="8e9b8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8e9b8-132">System.String</span></span>

## <span data-ttu-id="8e9b8-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e9b8-133">OUTPUTS</span></span>

### <span data-ttu-id="8e9b8-134">System. void</span><span class="sxs-lookup"><span data-stu-id="8e9b8-134">System.Void</span></span>

## <span data-ttu-id="8e9b8-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e9b8-135">NOTES</span></span>

## <span data-ttu-id="8e9b8-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e9b8-136">RELATED LINKS</span></span>

[<span data-ttu-id="8e9b8-137">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e9b8-137">Get-AzAutomationDscNodeConfiguration</span></span>](./Get-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="8e9b8-138">Import — AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e9b8-138">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="8e9b8-139">Polecenia cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="8e9b8-139">Azure Automation Cmdlets</span></span>](./Az.Automation.md)


