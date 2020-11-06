---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: f5de98b4f64b4f9adb03493638cdf4e1e613e10f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547160"
---
# <span data-ttu-id="8647e-101">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8647e-101">Get-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="8647e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8647e-102">SYNOPSIS</span></span>
<span data-ttu-id="8647e-103">Pobiera metadane konfiguracji węzłów DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="8647e-103">Gets metadata for DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8647e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8647e-104">SYNTAX</span></span>

### <span data-ttu-id="8647e-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8647e-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8647e-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8647e-106">ByNodeConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8647e-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8647e-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8647e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8647e-108">DESCRIPTION</span></span>
<span data-ttu-id="8647e-109">Polecenie cmdlet **Get-AzureRmAutomationDscNodeConfiguration** pobiera metadane konfiguracji węzła APS (Konfiguracja stanu żądanego) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8647e-109">The **Get-AzureRmAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="8647e-110">Konfiguracja węzła DSC jest przechowywana w dokumencie konfiguracyjnym Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8647e-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="8647e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8647e-111">EXAMPLES</span></span>

### <span data-ttu-id="8647e-112">Przykład 1: pobieranie wszystkich konfiguracji węzłów DSC</span><span class="sxs-lookup"><span data-stu-id="8647e-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="8647e-113">To polecenie pobiera metadane wszystkich konfiguracji węzłów DSC na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8647e-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8647e-114">Przykład 2: pobieranie wszystkich konfiguracji węzłów DSC dla konfiguracji DSC</span><span class="sxs-lookup"><span data-stu-id="8647e-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="8647e-115">To polecenie pobiera metadane wszystkich konfiguracji węzłów DSC na koncie usługi Automation o nazwie Contoso17, aby została wygenerowana Konfiguracja DSC o nazwie ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8647e-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="8647e-116">Przykład 3: Pobieranie konfiguracji węzła DSC według nazwy</span><span class="sxs-lookup"><span data-stu-id="8647e-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="8647e-117">To polecenie pobiera metadane konfiguracji węzła DSC z nazwą ContosoConfiguration. WebServer na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8647e-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8647e-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8647e-118">PARAMETERS</span></span>

### <span data-ttu-id="8647e-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8647e-119">-AutomationAccountName</span></span>
<span data-ttu-id="8647e-120">Określa nazwę konta usługi Automation, które zawiera konfiguracje węzła DSC, dla których to polecenie cmdlet pobiera metadane.</span><span class="sxs-lookup"><span data-stu-id="8647e-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="8647e-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8647e-121">-ConfigurationName</span></span>
<span data-ttu-id="8647e-122">Określa nazwę konfiguracji DSC, dla której to polecenie cmdlet pobiera metadane konfiguracji węzła.</span><span class="sxs-lookup"><span data-stu-id="8647e-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="8647e-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8647e-123">-Name</span></span>
<span data-ttu-id="8647e-124">Określa nazwę konfiguracji węzła DSC, dla której to polecenie cmdlet pobiera metadane.</span><span class="sxs-lookup"><span data-stu-id="8647e-124">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="8647e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8647e-125">-ResourceGroupName</span></span>
<span data-ttu-id="8647e-126">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8647e-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8647e-127">To polecenie cmdlet umożliwia pobieranie metadanych dla konfiguracji węzłów DSC w grupie zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="8647e-127">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8647e-128">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="8647e-128">-RollupStatus</span></span>
<span data-ttu-id="8647e-129">Określa stan zestawienia konfiguracji węzłów DSC, które ma być pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8647e-129">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="8647e-130">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="8647e-130">Valid values are:</span></span> 

- <span data-ttu-id="8647e-131">Właściwy</span><span class="sxs-lookup"><span data-stu-id="8647e-131">Bad</span></span> 
- <span data-ttu-id="8647e-132">Wyrob</span><span class="sxs-lookup"><span data-stu-id="8647e-132">Good</span></span>

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

### <span data-ttu-id="8647e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8647e-133">-DefaultProfile</span></span>
<span data-ttu-id="8647e-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8647e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8647e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8647e-135">CommonParameters</span></span>
<span data-ttu-id="8647e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8647e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8647e-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8647e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8647e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8647e-138">INPUTS</span></span>

## <span data-ttu-id="8647e-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8647e-139">OUTPUTS</span></span>

### <span data-ttu-id="8647e-140">Microsoft. Azure. Commands. Automation. model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="8647e-140">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="8647e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8647e-141">NOTES</span></span>

## <span data-ttu-id="8647e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8647e-142">RELATED LINKS</span></span>

[<span data-ttu-id="8647e-143">Import — AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8647e-143">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)


