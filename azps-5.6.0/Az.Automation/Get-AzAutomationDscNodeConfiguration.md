---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: b139ed5b67bbc36bad45ab2528ed74299d40c1b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969713"
---
# <span data-ttu-id="c915a-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c915a-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="c915a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c915a-102">SYNOPSIS</span></span>
<span data-ttu-id="c915a-103">Pobiera metadane dla konfiguracji węzła DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="c915a-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="c915a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c915a-104">SYNTAX</span></span>

### <span data-ttu-id="c915a-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c915a-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c915a-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c915a-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c915a-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c915a-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c915a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c915a-108">DESCRIPTION</span></span>
<span data-ttu-id="c915a-109">Polecenie **cmdlet Get-AzAutomationDscNodeConfiguration** pobiera metadane dla konfiguracji węzła APS Desired State Configuration (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c915a-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="c915a-110">W automatyzacji konfiguracja węzła dsc jest przechowywała jako dokument konfiguracji formatu MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="c915a-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="c915a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c915a-111">EXAMPLES</span></span>

### <span data-ttu-id="c915a-112">Przykład 1. Uzyskiwanie wszystkich konfiguracji węzła dsc</span><span class="sxs-lookup"><span data-stu-id="c915a-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="c915a-113">To polecenie pobiera metadane dla wszystkich konfiguracji węzła DSC w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c915a-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c915a-114">Przykład 2. Uzyskiwanie wszystkich konfiguracji węzła DSC dla konfiguracji dsc</span><span class="sxs-lookup"><span data-stu-id="c915a-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="c915a-115">To polecenie pobiera metadane dla wszystkich konfiguracji węzła DSC na koncie automatyzacji o nazwie Contoso17, wygenerowanej przez konfigurację dsC o nazwie ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c915a-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="c915a-116">Przykład 3. Uzyskiwanie konfiguracji węzła DSC według nazwy</span><span class="sxs-lookup"><span data-stu-id="c915a-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="c915a-117">To polecenie pobiera metadane dla konfiguracji węzła DSC o nazwie ContosoConfiguration.webserver na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c915a-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c915a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c915a-118">PARAMETERS</span></span>

### <span data-ttu-id="c915a-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c915a-119">-AutomationAccountName</span></span>
<span data-ttu-id="c915a-120">Określa nazwę konta automatyzacji zawierającego konfiguracje węzła DSC, dla którego to polecenie cmdlet pobiera metadane.</span><span class="sxs-lookup"><span data-stu-id="c915a-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="c915a-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c915a-121">-ConfigurationName</span></span>
<span data-ttu-id="c915a-122">Określa nazwę konfiguracji dsc, dla której to polecenie cmdlet pobiera metadane konfiguracji węzła.</span><span class="sxs-lookup"><span data-stu-id="c915a-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c915a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c915a-123">-DefaultProfile</span></span>
<span data-ttu-id="c915a-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c915a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c915a-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c915a-125">-Name</span></span>
<span data-ttu-id="c915a-126">Określa nazwę konfiguracji węzła DSC, dla której to polecenie cmdlet pobiera metadane.</span><span class="sxs-lookup"><span data-stu-id="c915a-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c915a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c915a-127">-ResourceGroupName</span></span>
<span data-ttu-id="c915a-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c915a-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c915a-129">To polecenie cmdlet pobiera metadane dla konfiguracji węzła DSC w grupie zasobów, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c915a-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c915a-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="c915a-130">-RollupStatus</span></span>
<span data-ttu-id="c915a-131">Określa stan rzutowania konfiguracji węzła DSC, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c915a-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="c915a-132">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="c915a-132">Valid values are:</span></span> 
- <span data-ttu-id="c915a-133">Bad</span><span class="sxs-lookup"><span data-stu-id="c915a-133">Bad</span></span> 
- <span data-ttu-id="c915a-134">Dobrze</span><span class="sxs-lookup"><span data-stu-id="c915a-134">Good</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c915a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c915a-135">CommonParameters</span></span>
<span data-ttu-id="c915a-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c915a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c915a-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c915a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c915a-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c915a-138">INPUTS</span></span>

### <span data-ttu-id="c915a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c915a-139">System.String</span></span>

## <span data-ttu-id="c915a-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c915a-140">OUTPUTS</span></span>

### <span data-ttu-id="c915a-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="c915a-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="c915a-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c915a-142">NOTES</span></span>

## <span data-ttu-id="c915a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c915a-143">RELATED LINKS</span></span>

[<span data-ttu-id="c915a-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c915a-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


