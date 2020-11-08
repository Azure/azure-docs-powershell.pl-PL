---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 09f1cd27e9af0c6442afa00d5301975cae8fbdeb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062281"
---
# <span data-ttu-id="952e2-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="952e2-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="952e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="952e2-102">SYNOPSIS</span></span>
<span data-ttu-id="952e2-103">Tworzy nowy obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="952e2-103">Creates a new workspace.</span></span>

## <span data-ttu-id="952e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="952e2-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="952e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="952e2-105">DESCRIPTION</span></span>
<span data-ttu-id="952e2-106">Tworzy nowy obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="952e2-106">Creates a new workspace.</span></span>

## <span data-ttu-id="952e2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="952e2-107">EXAMPLES</span></span>

### <span data-ttu-id="952e2-108">Przykład 1. Tworzenie obszaru roboczego datakostki</span><span class="sxs-lookup"><span data-stu-id="952e2-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="952e2-109">To polecenie umożliwia utworzenie obszaru roboczego datakostki.</span><span class="sxs-lookup"><span data-stu-id="952e2-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="952e2-110">Przykład 2: Tworzenie obszaru roboczego datakostki z dostosowanej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="952e2-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
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

<span data-ttu-id="952e2-111">To polecenie umożliwia utworzenie obszaru roboczego datakostki z dostosowanej sieci wirtualnej w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="952e2-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="952e2-112">Przykład 3: Tworzenie obszaru roboczego datakostki z włączonym włączeniem szyfrowania</span><span class="sxs-lookup"><span data-stu-id="952e2-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="952e2-113">To polecenie tworzy obszar roboczy datakostki i ustawia go w celu przygotowania do szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="952e2-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="952e2-114">Aby uzyskać więcej ustawień szyfrowania, zapoznaj się z przykładami Update-AzDatabricksWorkspace.</span><span class="sxs-lookup"><span data-stu-id="952e2-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="952e2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="952e2-115">PARAMETERS</span></span>

### <span data-ttu-id="952e2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="952e2-116">-AsJob</span></span>
<span data-ttu-id="952e2-117">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="952e2-117">Run the command as a job</span></span>

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

### <span data-ttu-id="952e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="952e2-118">-DefaultProfile</span></span>
<span data-ttu-id="952e2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="952e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="952e2-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="952e2-120">-Location</span></span>
<span data-ttu-id="952e2-121">Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="952e2-121">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="952e2-122">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="952e2-122">-ManagedResourceGroupName</span></span>
<span data-ttu-id="952e2-123">Nazwa grupy zarządzanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="952e2-123">The managed resource group name.</span></span>

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

### <span data-ttu-id="952e2-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="952e2-124">-Name</span></span>
<span data-ttu-id="952e2-125">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="952e2-125">The name of the workspace.</span></span>

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

### <span data-ttu-id="952e2-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="952e2-126">-NoWait</span></span>
<span data-ttu-id="952e2-127">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="952e2-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="952e2-128">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="952e2-128">-PrepareEncryption</span></span>
<span data-ttu-id="952e2-129">Przygotuj obszar roboczy do szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="952e2-129">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="952e2-130">Umożliwia administrowanie tożsamością zarządzanych kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="952e2-130">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="952e2-131">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="952e2-131">-PrivateSubnetName</span></span>
<span data-ttu-id="952e2-132">Nazwa podsieci prywatnej w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="952e2-132">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="952e2-133">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="952e2-133">-PublicSubnetName</span></span>
<span data-ttu-id="952e2-134">Nazwa podsieci publicznej w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="952e2-134">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="952e2-135">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="952e2-135">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="952e2-136">Wartość logiczna wskazująca, czy DBFS główny system plików jest włączony z pomocniczą warstwą szyfrowania za pomocą klawiszy zarządzanych platformy dla danych w stanie spoczynku.</span><span class="sxs-lookup"><span data-stu-id="952e2-136">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="952e2-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="952e2-137">-ResourceGroupName</span></span>
<span data-ttu-id="952e2-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="952e2-138">The name of the resource group.</span></span>
<span data-ttu-id="952e2-139">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="952e2-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="952e2-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="952e2-140">-Sku</span></span>
<span data-ttu-id="952e2-141">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="952e2-141">The SKU name.</span></span>

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

### <span data-ttu-id="952e2-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="952e2-142">-SubscriptionId</span></span>
<span data-ttu-id="952e2-143">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="952e2-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="952e2-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="952e2-144">-Tag</span></span>
<span data-ttu-id="952e2-145">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="952e2-145">Resource tags.</span></span>

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

### <span data-ttu-id="952e2-146">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="952e2-146">-VirtualNetworkId</span></span>
<span data-ttu-id="952e2-147">Identyfikator sieci wirtualnej, w której ma zostać utworzony klaster z datakostką.</span><span class="sxs-lookup"><span data-stu-id="952e2-147">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="952e2-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="952e2-148">-Confirm</span></span>
<span data-ttu-id="952e2-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="952e2-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="952e2-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="952e2-150">-WhatIf</span></span>
<span data-ttu-id="952e2-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="952e2-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="952e2-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="952e2-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="952e2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="952e2-153">CommonParameters</span></span>
<span data-ttu-id="952e2-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="952e2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="952e2-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="952e2-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="952e2-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="952e2-156">INPUTS</span></span>

## <span data-ttu-id="952e2-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="952e2-157">OUTPUTS</span></span>

### <span data-ttu-id="952e2-158">Microsoft. Azure. PowerShell. polecenia. datakosteks. models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="952e2-158">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="952e2-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="952e2-159">NOTES</span></span>

<span data-ttu-id="952e2-160">PISUJE</span><span class="sxs-lookup"><span data-stu-id="952e2-160">ALIASES</span></span>

## <span data-ttu-id="952e2-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="952e2-161">RELATED LINKS</span></span>

