---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
ms.openlocfilehash: 6d264ff7e2f12777845edbf2d56cae3d8b59ddb0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185370"
---
# <span data-ttu-id="cb372-101">Update-AzKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb372-101">Update-AzKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="cb372-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb372-102">SYNOPSIS</span></span>
<span data-ttu-id="cb372-103">Aktualizuje zestaw reguł sieciowych w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="cb372-103">Updates the network rule set on a key vault.</span></span>

## <span data-ttu-id="cb372-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cb372-104">SYNTAX</span></span>

### <span data-ttu-id="cb372-105">ByVaultName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="cb372-105">ByVaultName (Default)</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb372-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cb372-106">ByInputObject</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb372-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cb372-107">ByResourceId</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb372-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cb372-108">DESCRIPTION</span></span>
<span data-ttu-id="cb372-109">Polecenie **Update-AzKeyVaultNetworkRuleSet** aktualizuje reguły sieciowe obowiązujące w określonym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="cb372-109">The **Update-AzKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="cb372-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cb372-110">EXAMPLES</span></span>

### <span data-ttu-id="cb372-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cb372-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myRG
Location                         : West US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myrg/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="cb372-112">To polecenie aktualizuje zestaw reguł sieciowych w magazynie o nazwie "myVault" dla określonego zakresu adresów IP i sieci wirtualnej, co pozwala na pominięcie reguły sieciowej dla usług Azure.</span><span class="sxs-lookup"><span data-stu-id="cb372-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

### <span data-ttu-id="cb372-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cb372-113">Example 2</span></span>

<span data-ttu-id="cb372-114">Aktualizuje zestaw reguł sieciowych w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="cb372-114">Updates the network rule set on a key vault.</span></span> <span data-ttu-id="cb372-115">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="cb372-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultNetworkRuleSet -DefaultAction Allow -VaultName 'myVault'
```

## <span data-ttu-id="cb372-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb372-116">PARAMETERS</span></span>

### <span data-ttu-id="cb372-117">— Obejście</span><span class="sxs-lookup"><span data-stu-id="cb372-117">-Bypass</span></span>
<span data-ttu-id="cb372-118">Określa obejście reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="cb372-118">Specifies bypass of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum]
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb372-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="cb372-119">-DefaultAction</span></span>
<span data-ttu-id="cb372-120">Określa domyślną akcję reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="cb372-120">Specifies default action of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum]
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb372-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb372-121">-DefaultProfile</span></span>
<span data-ttu-id="cb372-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb372-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb372-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb372-123">-InputObject</span></span>
<span data-ttu-id="cb372-124">Obiekt KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb372-124">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb372-125">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="cb372-125">-IpAddressRange</span></span>
<span data-ttu-id="cb372-126">Określa dozwolony zakres adresów IP sieci reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="cb372-126">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb372-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb372-127">-PassThru</span></span>
<span data-ttu-id="cb372-128">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="cb372-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cb372-129">Jeśli ten przełącznik jest określony, zwracany jest obiekt zaktualizowanego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cb372-129">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="cb372-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb372-130">-ResourceGroupName</span></span>
<span data-ttu-id="cb372-131">Określa nazwę grupy zasobów skojarzonej z magazynem kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="cb372-131">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb372-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb372-132">-ResourceId</span></span>
<span data-ttu-id="cb372-133">Identyfikator zasobu KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb372-133">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb372-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cb372-134">-VaultName</span></span>
<span data-ttu-id="cb372-135">Określa nazwę magazynu kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="cb372-135">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb372-136">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="cb372-136">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="cb372-137">Określa dozwolony identyfikator zasobu sieci wirtualnej reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="cb372-137">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb372-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb372-138">-Confirm</span></span>
<span data-ttu-id="cb372-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cb372-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb372-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb372-140">-WhatIf</span></span>
<span data-ttu-id="cb372-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb372-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb372-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cb372-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb372-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb372-143">CommonParameters</span></span>
<span data-ttu-id="cb372-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb372-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb372-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb372-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb372-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb372-146">INPUTS</span></span>

### <span data-ttu-id="cb372-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="cb372-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="cb372-148">System.String</span><span class="sxs-lookup"><span data-stu-id="cb372-148">System.String</span></span>

### <span data-ttu-id="cb372-149">System.Nullable'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlet.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="cb372-149">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cb372-150">System.Nullable'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlet.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="cb372-150">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cb372-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb372-151">OUTPUTS</span></span>

### <span data-ttu-id="cb372-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="cb372-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="cb372-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cb372-153">NOTES</span></span>

## <span data-ttu-id="cb372-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb372-154">RELATED LINKS</span></span>
