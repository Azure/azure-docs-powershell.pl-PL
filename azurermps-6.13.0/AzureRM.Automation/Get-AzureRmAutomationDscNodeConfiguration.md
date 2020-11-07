---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: ae3a1d02e17aac12a96f74eec6ecfd1213f3d7c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716966"
---
# <span data-ttu-id="7907a-101">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="7907a-101">Get-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="7907a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7907a-102">SYNOPSIS</span></span>
<span data-ttu-id="7907a-103">Pobiera metadane konfiguracji węzłów DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="7907a-103">Gets metadata for DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7907a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7907a-104">SYNTAX</span></span>

### <span data-ttu-id="7907a-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7907a-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7907a-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7907a-106">ByNodeConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7907a-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7907a-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7907a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7907a-108">DESCRIPTION</span></span>
<span data-ttu-id="7907a-109">Polecenie cmdlet **Get-AzureRmAutomationDscNodeConfiguration** pobiera metadane konfiguracji węzła APS (Konfiguracja stanu żądanego) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7907a-109">The **Get-AzureRmAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="7907a-110">Konfiguracja węzła DSC jest przechowywana w dokumencie konfiguracyjnym Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="7907a-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="7907a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7907a-111">EXAMPLES</span></span>

### <span data-ttu-id="7907a-112">Przykład 1: pobieranie wszystkich konfiguracji węzłów DSC</span><span class="sxs-lookup"><span data-stu-id="7907a-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="7907a-113">To polecenie pobiera metadane wszystkich konfiguracji węzłów DSC na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7907a-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7907a-114">Przykład 2: pobieranie wszystkich konfiguracji węzłów DSC dla konfiguracji DSC</span><span class="sxs-lookup"><span data-stu-id="7907a-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="7907a-115">To polecenie pobiera metadane wszystkich konfiguracji węzłów DSC na koncie usługi Automation o nazwie Contoso17, aby została wygenerowana Konfiguracja DSC o nazwie ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7907a-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="7907a-116">Przykład 3: Pobieranie konfiguracji węzła DSC według nazwy</span><span class="sxs-lookup"><span data-stu-id="7907a-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="7907a-117">To polecenie pobiera metadane konfiguracji węzła DSC z nazwą ContosoConfiguration. WebServer na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7907a-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7907a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7907a-118">PARAMETERS</span></span>

### <span data-ttu-id="7907a-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7907a-119">-AutomationAccountName</span></span>
<span data-ttu-id="7907a-120">Określa nazwę konta usługi Automation, które zawiera konfiguracje węzła DSC, dla których to polecenie cmdlet pobiera metadane.</span><span class="sxs-lookup"><span data-stu-id="7907a-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="7907a-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7907a-121">-ConfigurationName</span></span>
<span data-ttu-id="7907a-122">Określa nazwę konfiguracji DSC, dla której to polecenie cmdlet pobiera metadane konfiguracji węzła.</span><span class="sxs-lookup"><span data-stu-id="7907a-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="7907a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7907a-123">-DefaultProfile</span></span>
<span data-ttu-id="7907a-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7907a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7907a-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7907a-125">-Name</span></span>
<span data-ttu-id="7907a-126">Określa nazwę konfiguracji węzła DSC, dla której to polecenie cmdlet pobiera metadane.</span><span class="sxs-lookup"><span data-stu-id="7907a-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="7907a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7907a-127">-ResourceGroupName</span></span>
<span data-ttu-id="7907a-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7907a-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7907a-129">To polecenie cmdlet umożliwia pobieranie metadanych dla konfiguracji węzłów DSC w grupie zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="7907a-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7907a-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="7907a-130">-RollupStatus</span></span>
<span data-ttu-id="7907a-131">Określa stan zestawienia konfiguracji węzłów DSC, które ma być pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7907a-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="7907a-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="7907a-132">Valid values are:</span></span> 
- <span data-ttu-id="7907a-133">Właściwy</span><span class="sxs-lookup"><span data-stu-id="7907a-133">Bad</span></span> 
- <span data-ttu-id="7907a-134">Wyrob</span><span class="sxs-lookup"><span data-stu-id="7907a-134">Good</span></span>

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

### <span data-ttu-id="7907a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7907a-135">CommonParameters</span></span>
<span data-ttu-id="7907a-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7907a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7907a-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7907a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7907a-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7907a-138">INPUTS</span></span>

### <span data-ttu-id="7907a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7907a-139">System.String</span></span>

## <span data-ttu-id="7907a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7907a-140">OUTPUTS</span></span>

### <span data-ttu-id="7907a-141">Microsoft. Azure. Commands. Automation. model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="7907a-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="7907a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7907a-142">NOTES</span></span>

## <span data-ttu-id="7907a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7907a-143">RELATED LINKS</span></span>

[<span data-ttu-id="7907a-144">Import — AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="7907a-144">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)


