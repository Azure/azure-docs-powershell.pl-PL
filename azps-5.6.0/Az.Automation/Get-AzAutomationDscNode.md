---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
ms.openlocfilehash: 790c280d139f2770f08d5ecfed64acf42d0fc1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990557"
---
# <span data-ttu-id="57232-101">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="57232-101">Get-AzAutomationDscNode</span></span>

## <span data-ttu-id="57232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57232-102">SYNOPSIS</span></span>
<span data-ttu-id="57232-103">Pobiera węzły dsc z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="57232-103">Gets DSC nodes from Automation.</span></span>

## <span data-ttu-id="57232-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="57232-104">SYNTAX</span></span>

### <span data-ttu-id="57232-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="57232-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57232-106">ById</span><span class="sxs-lookup"><span data-stu-id="57232-106">ById</span></span>
```
Get-AzAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57232-107">ByName</span><span class="sxs-lookup"><span data-stu-id="57232-107">ByName</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57232-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="57232-108">ByNodeConfiguration</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57232-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="57232-109">ByConfiguration</span></span>
```
Get-AzAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57232-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="57232-110">DESCRIPTION</span></span>
<span data-ttu-id="57232-111">Polecenie **cmdlet Get-AzAutomationDscNode** pobiera węzły APS Desired State Configuration (DSC) z automatyzacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="57232-111">The **Get-AzAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="57232-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="57232-112">EXAMPLES</span></span>

### <span data-ttu-id="57232-113">Przykład 1. Uzyskiwanie wszystkich węzłów dsc</span><span class="sxs-lookup"><span data-stu-id="57232-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="57232-114">To polecenie pobiera metadane dla wszystkich węzłów dsc w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="57232-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="57232-115">Przykład 2. Uzyskiwanie wszystkich węzłów dsc dla konfiguracji dsc</span><span class="sxs-lookup"><span data-stu-id="57232-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="57232-116">To polecenie pobiera metadane dla wszystkich węzłów DSC na koncie automatyzacji o nazwie Contoso17, które zostały zamapowane na konfigurację węzła DSC wygenerowaną przez konfigurację DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="57232-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="57232-117">Przykład 3. Uzyskiwanie węzła DSC według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="57232-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="57232-118">To polecenie pobiera metadane w węźle DSC o określonym identyfikatorze konta automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="57232-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="57232-119">Przykład 4. Uzyskiwanie węzła DSC według nazwy</span><span class="sxs-lookup"><span data-stu-id="57232-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="57232-120">To polecenie pobiera metadane w węźle DSC o nazwie Komputer14 w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="57232-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="57232-121">Przykład 5. Uzyskiwanie wszystkich węzłów dsc zamapowanych na konfigurację węzła DSC</span><span class="sxs-lookup"><span data-stu-id="57232-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="57232-122">To polecenie pobiera metadane dla wszystkich węzłów DSC na koncie automatyzacji o nazwie Contoso17, które są mapowane na konfigurację węzła DSC o nazwie ContosoConfiguration.webserver.</span><span class="sxs-lookup"><span data-stu-id="57232-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="57232-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57232-123">PARAMETERS</span></span>

### <span data-ttu-id="57232-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="57232-124">-AutomationAccountName</span></span>
<span data-ttu-id="57232-125">Określa nazwę konta automatyzacji zawierającego węzły dsc, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57232-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="57232-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="57232-126">-ConfigurationName</span></span>
<span data-ttu-id="57232-127">Określa nazwę konfiguracji dsc.</span><span class="sxs-lookup"><span data-stu-id="57232-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="57232-128">To polecenie cmdlet pobiera węzły DSC zgodne z konfiguracjami węzła wygenerowanymi na podstawie konfiguracji, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="57232-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57232-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57232-129">-DefaultProfile</span></span>
<span data-ttu-id="57232-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="57232-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57232-131">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="57232-131">-Id</span></span>
<span data-ttu-id="57232-132">Określa unikatowy identyfikator węzła DSC, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57232-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57232-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="57232-133">-Name</span></span>
<span data-ttu-id="57232-134">Określa nazwę węzła DSC, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57232-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57232-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="57232-135">-NodeConfigurationName</span></span>
<span data-ttu-id="57232-136">Określa nazwę konfiguracji węzła, która pobiera to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57232-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57232-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57232-137">-ResourceGroupName</span></span>
<span data-ttu-id="57232-138">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera węzły DSC.</span><span class="sxs-lookup"><span data-stu-id="57232-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="57232-139">— Status</span><span class="sxs-lookup"><span data-stu-id="57232-139">-Status</span></span>
<span data-ttu-id="57232-140">Określa stan węzłów DSC, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57232-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="57232-141">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="57232-141">Valid values are:</span></span> 
- <span data-ttu-id="57232-142">Zgodny</span><span class="sxs-lookup"><span data-stu-id="57232-142">Compliant</span></span> 
- <span data-ttu-id="57232-143">NotCompliant</span><span class="sxs-lookup"><span data-stu-id="57232-143">NotCompliant</span></span>
- <span data-ttu-id="57232-144">Niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="57232-144">Failed</span></span>
- <span data-ttu-id="57232-145">Oczekiwanie</span><span class="sxs-lookup"><span data-stu-id="57232-145">Pending</span></span> 
- <span data-ttu-id="57232-146">Odebrano</span><span class="sxs-lookup"><span data-stu-id="57232-146">Received</span></span>
- <span data-ttu-id="57232-147">Nie odpowiada</span><span class="sxs-lookup"><span data-stu-id="57232-147">Unresponsive</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases:
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57232-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57232-148">CommonParameters</span></span>
<span data-ttu-id="57232-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57232-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57232-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57232-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57232-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57232-151">INPUTS</span></span>

### <span data-ttu-id="57232-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="57232-152">System.Guid</span></span>

### <span data-ttu-id="57232-153">System.String</span><span class="sxs-lookup"><span data-stu-id="57232-153">System.String</span></span>

## <span data-ttu-id="57232-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57232-154">OUTPUTS</span></span>

### <span data-ttu-id="57232-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="57232-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="57232-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="57232-156">NOTES</span></span>

## <span data-ttu-id="57232-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57232-157">RELATED LINKS</span></span>

[<span data-ttu-id="57232-158">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="57232-158">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="57232-159">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="57232-159">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="57232-160">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="57232-160">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


