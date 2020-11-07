---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
ms.openlocfilehash: a902c88c53736f1e0db238cdb53ea381e5e887a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524649"
---
# <span data-ttu-id="b9c68-101">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b9c68-101">Get-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="b9c68-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9c68-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c68-103">Pobiera węzły DSC z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="b9c68-103">Gets DSC nodes from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c68-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9c68-104">SYNTAX</span></span>

### <span data-ttu-id="b9c68-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b9c68-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c68-106">ById</span><span class="sxs-lookup"><span data-stu-id="b9c68-106">ById</span></span>
```
Get-AzureRmAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c68-107">ByName</span><span class="sxs-lookup"><span data-stu-id="b9c68-107">ByName</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c68-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9c68-108">ByNodeConfiguration</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9c68-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9c68-109">ByConfiguration</span></span>
```
Get-AzureRmAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c68-110">Opis</span><span class="sxs-lookup"><span data-stu-id="b9c68-110">DESCRIPTION</span></span>
<span data-ttu-id="b9c68-111">Polecenie cmdlet **Get-AzureRmAutomationDscNode** pobiera węzły konfiguracji stanu żądanego (DSC) z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b9c68-111">The **Get-AzureRmAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="b9c68-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9c68-112">EXAMPLES</span></span>

### <span data-ttu-id="b9c68-113">Przykład 1: uzyskiwanie wszystkich węzłów DSC</span><span class="sxs-lookup"><span data-stu-id="b9c68-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="b9c68-114">To polecenie pobiera metadane wszystkich węzłów DSC na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b9c68-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b9c68-115">Przykład 2: uzyskiwanie wszystkich węzłów DSC dla konfiguracji DSC</span><span class="sxs-lookup"><span data-stu-id="b9c68-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="b9c68-116">To polecenie pobiera metadane wszystkich węzłów DSC na koncie usługi Automation o nazwie Contoso17, które są mapowane na konfigurację węzła DSC wygenerowaną przez ContosoConfiguration konfiguracji DSC.</span><span class="sxs-lookup"><span data-stu-id="b9c68-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="b9c68-117">Przykład 3: pobieranie węzła DSC o IDENTYFIKATORze</span><span class="sxs-lookup"><span data-stu-id="b9c68-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="b9c68-118">To polecenie pobiera metadane z węzła DSC o określonym IDENTYFIKATORze w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b9c68-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b9c68-119">Przykład 4: pobieranie węzła DSC według nazwy</span><span class="sxs-lookup"><span data-stu-id="b9c68-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="b9c68-120">To polecenie pobiera metadane z węzła DSC o nazwie Computer14 na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b9c68-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b9c68-121">Przykład 5: uzyskiwanie wszystkich węzłów DSC zamapowanych na konfigurację węzła DSC</span><span class="sxs-lookup"><span data-stu-id="b9c68-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="b9c68-122">To polecenie pobiera metadane we wszystkich węzłach DSC na koncie usługi Automation o nazwie Contoso17, które są mapowane na konfigurację węzła DSC o nazwie ContosoConfiguration. WebServer.</span><span class="sxs-lookup"><span data-stu-id="b9c68-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="b9c68-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9c68-123">PARAMETERS</span></span>

### <span data-ttu-id="b9c68-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b9c68-124">-AutomationAccountName</span></span>
<span data-ttu-id="b9c68-125">Określa nazwę konta automatyzacji zawierającego węzły DSC, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9c68-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b9c68-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b9c68-126">-ConfigurationName</span></span>
<span data-ttu-id="b9c68-127">Określa nazwę konfiguracji DSC.</span><span class="sxs-lookup"><span data-stu-id="b9c68-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="b9c68-128">To polecenie cmdlet spowoduje wyświetlenie węzłów DSC zgodnych z konfiguracją węzła wygenerowaną na podstawie konfiguracji, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b9c68-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9c68-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c68-129">-DefaultProfile</span></span>
<span data-ttu-id="b9c68-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b9c68-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9c68-131">-ID</span><span class="sxs-lookup"><span data-stu-id="b9c68-131">-Id</span></span>
<span data-ttu-id="b9c68-132">Określa unikatowy identyfikator węzła DSC, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9c68-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b9c68-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b9c68-133">-Name</span></span>
<span data-ttu-id="b9c68-134">Określa nazwę węzła DSC, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9c68-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b9c68-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b9c68-135">-NodeConfigurationName</span></span>
<span data-ttu-id="b9c68-136">Określa nazwę konfiguracji węzła, którą to polecenie cmdlet pobiera.</span><span class="sxs-lookup"><span data-stu-id="b9c68-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b9c68-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c68-137">-ResourceGroupName</span></span>
<span data-ttu-id="b9c68-138">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera węzły DSC.</span><span class="sxs-lookup"><span data-stu-id="b9c68-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="b9c68-139">-Status</span><span class="sxs-lookup"><span data-stu-id="b9c68-139">-Status</span></span>
<span data-ttu-id="b9c68-140">Określa stan węzłów DSC, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9c68-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="b9c68-141">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="b9c68-141">Valid values are:</span></span> 
- <span data-ttu-id="b9c68-142">Star</span><span class="sxs-lookup"><span data-stu-id="b9c68-142">Compliant</span></span> 
- <span data-ttu-id="b9c68-143">NotCompliant</span><span class="sxs-lookup"><span data-stu-id="b9c68-143">NotCompliant</span></span>
- <span data-ttu-id="b9c68-144">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="b9c68-144">Failed</span></span>
- <span data-ttu-id="b9c68-145">Wybranego</span><span class="sxs-lookup"><span data-stu-id="b9c68-145">Pending</span></span> 
- <span data-ttu-id="b9c68-146">Odebrał</span><span class="sxs-lookup"><span data-stu-id="b9c68-146">Received</span></span>
- <span data-ttu-id="b9c68-147">Odpowiadać</span><span class="sxs-lookup"><span data-stu-id="b9c68-147">Unresponsive</span></span>

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

### <span data-ttu-id="b9c68-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c68-148">CommonParameters</span></span>
<span data-ttu-id="b9c68-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c68-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c68-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c68-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c68-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9c68-151">INPUTS</span></span>

### <span data-ttu-id="b9c68-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b9c68-152">System.Guid</span></span>

### <span data-ttu-id="b9c68-153">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c68-153">System.String</span></span>

## <span data-ttu-id="b9c68-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9c68-154">OUTPUTS</span></span>

### <span data-ttu-id="b9c68-155">Microsoft. Azure. Commands. Automation. model. DscNode</span><span class="sxs-lookup"><span data-stu-id="b9c68-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="b9c68-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9c68-156">NOTES</span></span>

## <span data-ttu-id="b9c68-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9c68-157">RELATED LINKS</span></span>

[<span data-ttu-id="b9c68-158">Rejestr — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b9c68-158">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="b9c68-159">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b9c68-159">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="b9c68-160">Wyrejestrowanie — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b9c68-160">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)

