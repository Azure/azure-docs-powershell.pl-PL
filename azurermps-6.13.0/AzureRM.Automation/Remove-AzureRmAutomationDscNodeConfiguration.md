---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 60f80f92723bbb66d1bf88c9fd8efea66c8c4e55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542003"
---
# <span data-ttu-id="d6261-101">Remove-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6261-101">Remove-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="d6261-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6261-102">SYNOPSIS</span></span>
<span data-ttu-id="d6261-103">Usuwa metadane z konfiguracji węzłów DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d6261-103">Removes metadata from DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6261-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6261-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6261-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d6261-105">DESCRIPTION</span></span>
<span data-ttu-id="d6261-106">Polecenie cmdlet **Remove-AzureRmAutomationDscNodeConfiguration** usuwa metadane z konfiguracji węzłów konfiguracji stanu żądanego (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d6261-106">The **Remove-AzureRmAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="d6261-107">Konfiguracja węzła DSC jest przechowywana w dokumencie konfiguracyjnym Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="d6261-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="d6261-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6261-108">EXAMPLES</span></span>

## <span data-ttu-id="d6261-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6261-109">PARAMETERS</span></span>

### <span data-ttu-id="d6261-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d6261-110">-AutomationAccountName</span></span>
<span data-ttu-id="d6261-111">Określa nazwę konta usługi Automation, które zawiera konfiguracje węzła DSC, dla których to polecenie cmdlet usuwa metadane.</span><span class="sxs-lookup"><span data-stu-id="d6261-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="d6261-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6261-112">-DefaultProfile</span></span>
<span data-ttu-id="d6261-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d6261-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6261-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d6261-114">-Force</span></span>
<span data-ttu-id="d6261-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="d6261-115">ps_force</span></span>

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

### <span data-ttu-id="d6261-116">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="d6261-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="d6261-117">Wskazuje, że ten aplet polecenia ignoruje mapowania węzłów.</span><span class="sxs-lookup"><span data-stu-id="d6261-117">Indicates that this cmdlet ignores node mappings.</span></span>

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

### <span data-ttu-id="d6261-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d6261-118">-Name</span></span>
<span data-ttu-id="d6261-119">Określa nazwę konfiguracji węzła DSC, dla której to polecenie cmdlet usuwa metadane.</span><span class="sxs-lookup"><span data-stu-id="d6261-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="d6261-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6261-120">-ResourceGroupName</span></span>
<span data-ttu-id="d6261-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d6261-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d6261-122">To polecenie cmdlet usuwa metadane konfiguracji węzłów DSC w grupie zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d6261-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d6261-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6261-123">-Confirm</span></span>
<span data-ttu-id="d6261-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6261-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6261-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6261-125">-WhatIf</span></span>
<span data-ttu-id="d6261-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6261-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6261-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d6261-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6261-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6261-128">CommonParameters</span></span>
<span data-ttu-id="d6261-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6261-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6261-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6261-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6261-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6261-131">INPUTS</span></span>

### <span data-ttu-id="d6261-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d6261-132">System.String</span></span>

## <span data-ttu-id="d6261-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6261-133">OUTPUTS</span></span>

### <span data-ttu-id="d6261-134">System. void</span><span class="sxs-lookup"><span data-stu-id="d6261-134">System.Void</span></span>

## <span data-ttu-id="d6261-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6261-135">NOTES</span></span>

## <span data-ttu-id="d6261-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6261-136">RELATED LINKS</span></span>

[<span data-ttu-id="d6261-137">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6261-137">Get-AzureRmAutomationDscNodeConfiguration</span></span>](./Get-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="d6261-138">Import — AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6261-138">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="d6261-139">Polecenia cmdlet usługi Azure Automation</span><span class="sxs-lookup"><span data-stu-id="d6261-139">Azure Automation Cmdlets</span></span>](./AzureRM.Automation.md)


