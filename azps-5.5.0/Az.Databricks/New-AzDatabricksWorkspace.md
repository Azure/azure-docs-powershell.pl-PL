---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 0626559fd80a9ebd212c8f6ebb032755d25ba59c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238120"
---
# <span data-ttu-id="9c53e-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="9c53e-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="9c53e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c53e-102">SYNOPSIS</span></span>
<span data-ttu-id="9c53e-103">Tworzy nowy obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="9c53e-103">Creates a new workspace.</span></span>

## <span data-ttu-id="9c53e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9c53e-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-EnableNoPublicIP] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c53e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9c53e-105">DESCRIPTION</span></span>
<span data-ttu-id="9c53e-106">Tworzy nowy obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="9c53e-106">Creates a new workspace.</span></span>

## <span data-ttu-id="9c53e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9c53e-107">EXAMPLES</span></span>

### <span data-ttu-id="9c53e-108">Przykład 1. Tworzenie obszaru roboczego programu Databricks</span><span class="sxs-lookup"><span data-stu-id="9c53e-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="9c53e-109">To polecenie umożliwia utworzenie obszaru roboczego programu Databricks.</span><span class="sxs-lookup"><span data-stu-id="9c53e-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="9c53e-110">Przykład 2. Tworzenie obszaru roboczego usługi Databricks przy użyciu dostosowanej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9c53e-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
```powershell
PS C:\> $dlg = New-AzDelegation -Name dbrdl -ServiceName "Microsoft.Databricks/workspaces"
PS C:\> $rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName testgroup -Location eastus -Name nsg-test -SecurityRules $rdpRule
PS C:\> $privSubnet = New-AzVirtualNetworkSubnetConfig -Name priv-sub -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $pubSubnet = New-AzVirtualNetworkSubnetConfig -Name pub-sub  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $testVN = New-AzVirtualNetwork -Name testvn -ResourceGroupName testgroup -Location eastus -AddressPrefix "10.0.0.0/16" -Subnet $privSubnet,$pubSubnet
PS C:\> New-AzDatabricksWorkspace -Name databricks-test-with-custom-vn -ResourceGroupName testgroup -Location eastus -VirtualNetworkId $testVN.Id -PrivateSubnetName $privSubnet.Name -PublicSubnetName $privSubnet.Name -Sku standard

Location Name                           Type
-------- ----                           ----
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="9c53e-111">To polecenie umożliwia utworzenie obszaru roboczego usługi Databricks z dostosowaną siecią wirtualną w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="9c53e-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="9c53e-112">Przykład 3. Tworzenie obszaru roboczego z włączym szyfrowaniem</span><span class="sxs-lookup"><span data-stu-id="9c53e-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="9c53e-113">To polecenie tworzy obszar roboczy programu Databricks i konfiguruje go do przygotowania do szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="9c53e-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="9c53e-114">Zapoznaj się z przykładami Update-AzDatabricksWorkspace, aby uzyskać więcej ustawień szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="9c53e-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="9c53e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c53e-115">PARAMETERS</span></span>

### <span data-ttu-id="9c53e-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9c53e-116">-AsJob</span></span>
<span data-ttu-id="9c53e-117">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="9c53e-117">Run the command as a job</span></span>

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

### <span data-ttu-id="9c53e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c53e-118">-DefaultProfile</span></span>
<span data-ttu-id="9c53e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c53e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c53e-120">-EnableNoPublicIP</span><span class="sxs-lookup"><span data-stu-id="9c53e-120">-EnableNoPublicIP</span></span>
<span data-ttu-id="9c53e-121">Wartość, która powinna być używana dla tego pola.</span><span class="sxs-lookup"><span data-stu-id="9c53e-121">The value which should be used for this field.</span></span>

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

### <span data-ttu-id="9c53e-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9c53e-122">-Location</span></span>
<span data-ttu-id="9c53e-123">Lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="9c53e-123">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c53e-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c53e-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="9c53e-125">Nazwa grupy zasobów zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="9c53e-125">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c53e-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9c53e-126">-Name</span></span>
<span data-ttu-id="9c53e-127">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9c53e-127">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c53e-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9c53e-128">-NoWait</span></span>
<span data-ttu-id="9c53e-129">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="9c53e-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9c53e-130">- PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="9c53e-130">-PrepareEncryption</span></span>
<span data-ttu-id="9c53e-131">Przygotowywanie obszaru roboczego do szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="9c53e-131">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="9c53e-132">Włącza tożsamość zarządzaną dla konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="9c53e-132">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="9c53e-133">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="9c53e-133">-PrivateSubnetName</span></span>
<span data-ttu-id="9c53e-134">Nazwa prywatnej podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c53e-134">The name of the Private Subnet within the Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c53e-135">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="9c53e-135">-PublicSubnetName</span></span>
<span data-ttu-id="9c53e-136">Nazwa publicznej podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c53e-136">The name of a Public Subnet within the Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c53e-137">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="9c53e-137">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="9c53e-138">Wartość logiczna wskazująca, czy główny system plików DBFS zostanie włączony z pomocniczą warstwą szyfrowania z kluczami zarządzanymi platformy dla danych w spoczynku.</span><span class="sxs-lookup"><span data-stu-id="9c53e-138">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="9c53e-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c53e-139">-ResourceGroupName</span></span>
<span data-ttu-id="9c53e-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9c53e-140">The name of the resource group.</span></span>
<span data-ttu-id="9c53e-141">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="9c53e-141">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c53e-142">- SKU</span><span class="sxs-lookup"><span data-stu-id="9c53e-142">-Sku</span></span>
<span data-ttu-id="9c53e-143">Nazwa sku.</span><span class="sxs-lookup"><span data-stu-id="9c53e-143">The SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c53e-144">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c53e-144">-SubscriptionId</span></span>
<span data-ttu-id="9c53e-145">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9c53e-145">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c53e-146">— Tag</span><span class="sxs-lookup"><span data-stu-id="9c53e-146">-Tag</span></span>
<span data-ttu-id="9c53e-147">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="9c53e-147">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c53e-148">- VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="9c53e-148">-VirtualNetworkId</span></span>
<span data-ttu-id="9c53e-149">Identyfikator sieci wirtualnej, w której należy utworzyć ten klaster danych.</span><span class="sxs-lookup"><span data-stu-id="9c53e-149">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c53e-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c53e-150">-Confirm</span></span>
<span data-ttu-id="9c53e-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9c53e-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c53e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c53e-152">-WhatIf</span></span>
<span data-ttu-id="9c53e-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c53e-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c53e-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9c53e-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c53e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c53e-155">CommonParameters</span></span>
<span data-ttu-id="9c53e-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c53e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c53e-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c53e-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c53e-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c53e-158">INPUTS</span></span>

## <span data-ttu-id="9c53e-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9c53e-159">OUTPUTS</span></span>

### <span data-ttu-id="9c53e-160">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="9c53e-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="9c53e-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9c53e-161">NOTES</span></span>

<span data-ttu-id="9c53e-162">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9c53e-162">ALIASES</span></span>

## <span data-ttu-id="9c53e-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c53e-163">RELATED LINKS</span></span>

