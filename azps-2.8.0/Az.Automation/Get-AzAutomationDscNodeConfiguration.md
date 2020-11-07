---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: a3b0b53146703a13f0ae8ea1627d2d9722c85eeb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706825"
---
# <span data-ttu-id="4252b-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4252b-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="4252b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4252b-102">SYNOPSIS</span></span>
<span data-ttu-id="4252b-103">Pobiera metadane konfiguracji węzłów DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="4252b-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="4252b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4252b-104">SYNTAX</span></span>

### <span data-ttu-id="4252b-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4252b-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4252b-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4252b-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4252b-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4252b-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4252b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4252b-108">DESCRIPTION</span></span>
<span data-ttu-id="4252b-109">Polecenie cmdlet **Get-AzAutomationDscNodeConfiguration** pobiera metadane konfiguracji węzła APS (Konfiguracja stanu żądanego) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4252b-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="4252b-110">Konfiguracja węzła DSC jest przechowywana w dokumencie konfiguracyjnym Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4252b-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="4252b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4252b-111">EXAMPLES</span></span>

### <span data-ttu-id="4252b-112">Przykład 1: pobieranie wszystkich konfiguracji węzłów DSC</span><span class="sxs-lookup"><span data-stu-id="4252b-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="4252b-113">To polecenie pobiera metadane wszystkich konfiguracji węzłów DSC na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4252b-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4252b-114">Przykład 2: pobieranie wszystkich konfiguracji węzłów DSC dla konfiguracji DSC</span><span class="sxs-lookup"><span data-stu-id="4252b-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="4252b-115">To polecenie pobiera metadane wszystkich konfiguracji węzłów DSC na koncie usługi Automation o nazwie Contoso17, aby została wygenerowana Konfiguracja DSC o nazwie ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4252b-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="4252b-116">Przykład 3: Pobieranie konfiguracji węzła DSC według nazwy</span><span class="sxs-lookup"><span data-stu-id="4252b-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="4252b-117">To polecenie pobiera metadane konfiguracji węzła DSC z nazwą ContosoConfiguration. WebServer na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4252b-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4252b-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4252b-118">PARAMETERS</span></span>

### <span data-ttu-id="4252b-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4252b-119">-AutomationAccountName</span></span>
<span data-ttu-id="4252b-120">Określa nazwę konta usługi Automation, które zawiera konfiguracje węzła DSC, dla których to polecenie cmdlet pobiera metadane.</span><span class="sxs-lookup"><span data-stu-id="4252b-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="4252b-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4252b-121">-ConfigurationName</span></span>
<span data-ttu-id="4252b-122">Określa nazwę konfiguracji DSC, dla której to polecenie cmdlet pobiera metadane konfiguracji węzła.</span><span class="sxs-lookup"><span data-stu-id="4252b-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="4252b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4252b-123">-DefaultProfile</span></span>
<span data-ttu-id="4252b-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4252b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4252b-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4252b-125">-Name</span></span>
<span data-ttu-id="4252b-126">Określa nazwę konfiguracji węzła DSC, dla której to polecenie cmdlet pobiera metadane.</span><span class="sxs-lookup"><span data-stu-id="4252b-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="4252b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4252b-127">-ResourceGroupName</span></span>
<span data-ttu-id="4252b-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4252b-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4252b-129">To polecenie cmdlet umożliwia pobieranie metadanych dla konfiguracji węzłów DSC w grupie zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="4252b-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4252b-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="4252b-130">-RollupStatus</span></span>
<span data-ttu-id="4252b-131">Określa stan zestawienia konfiguracji węzłów DSC, które ma być pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4252b-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="4252b-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="4252b-132">Valid values are:</span></span> 
- <span data-ttu-id="4252b-133">Właściwy</span><span class="sxs-lookup"><span data-stu-id="4252b-133">Bad</span></span> 
- <span data-ttu-id="4252b-134">Wyrob</span><span class="sxs-lookup"><span data-stu-id="4252b-134">Good</span></span>

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

### <span data-ttu-id="4252b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4252b-135">CommonParameters</span></span>
<span data-ttu-id="4252b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4252b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4252b-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4252b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4252b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4252b-138">INPUTS</span></span>

### <span data-ttu-id="4252b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4252b-139">System.String</span></span>

## <span data-ttu-id="4252b-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4252b-140">OUTPUTS</span></span>

### <span data-ttu-id="4252b-141">Microsoft. Azure. Commands. Automation. model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="4252b-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="4252b-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4252b-142">NOTES</span></span>

## <span data-ttu-id="4252b-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4252b-143">RELATED LINKS</span></span>

[<span data-ttu-id="4252b-144">Import — AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4252b-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


