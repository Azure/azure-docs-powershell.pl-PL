---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
ms.openlocfilehash: 6d264ff7e2f12777845edbf2d56cae3d8b59ddb0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360479"
---
# <span data-ttu-id="86c89-101">Update-AzKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="86c89-101">Update-AzKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="86c89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86c89-102">SYNOPSIS</span></span>
<span data-ttu-id="86c89-103">Umożliwia zaktualizowanie zestawu reguł sieci w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="86c89-103">Updates the network rule set on a key vault.</span></span>

## <span data-ttu-id="86c89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86c89-104">SYNTAX</span></span>

### <span data-ttu-id="86c89-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="86c89-105">ByVaultName (Default)</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c89-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="86c89-106">ByInputObject</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c89-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="86c89-107">ByResourceId</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c89-108">Opis</span><span class="sxs-lookup"><span data-stu-id="86c89-108">DESCRIPTION</span></span>
<span data-ttu-id="86c89-109">Polecenie **Update-AzKeyVaultNetworkRuleSet** powoduje zaktualizowanie reguł sieciowych dotyczących określonego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="86c89-109">The **Update-AzKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="86c89-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86c89-110">EXAMPLES</span></span>

### <span data-ttu-id="86c89-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="86c89-111">Example 1</span></span>
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

<span data-ttu-id="86c89-112">To polecenie aktualizuje zestaw reguł sieci w magazynie o nazwie "Moja magazyn" dla określonego zakresu adresów IP i sieci wirtualnej, umożliwiając ominięcie reguły sieci dla usług platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="86c89-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

### <span data-ttu-id="86c89-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="86c89-113">Example 2</span></span>

<span data-ttu-id="86c89-114">Umożliwia zaktualizowanie zestawu reguł sieci w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="86c89-114">Updates the network rule set on a key vault.</span></span> <span data-ttu-id="86c89-115">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="86c89-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultNetworkRuleSet -DefaultAction Allow -VaultName 'myVault'
```

## <span data-ttu-id="86c89-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86c89-116">PARAMETERS</span></span>

### <span data-ttu-id="86c89-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="86c89-117">-Bypass</span></span>
<span data-ttu-id="86c89-118">Określa ominięcie reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="86c89-118">Specifies bypass of network rule.</span></span>

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

### <span data-ttu-id="86c89-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="86c89-119">-DefaultAction</span></span>
<span data-ttu-id="86c89-120">Określa domyślną akcję reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="86c89-120">Specifies default action of network rule.</span></span>

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

### <span data-ttu-id="86c89-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c89-121">-DefaultProfile</span></span>
<span data-ttu-id="86c89-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86c89-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86c89-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="86c89-123">-InputObject</span></span>
<span data-ttu-id="86c89-124">Obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="86c89-124">KeyVault object</span></span>

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

### <span data-ttu-id="86c89-125">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="86c89-125">-IpAddressRange</span></span>
<span data-ttu-id="86c89-126">Określa dozwolony zakres adresów IP sieci w regule sieci.</span><span class="sxs-lookup"><span data-stu-id="86c89-126">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="86c89-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86c89-127">-PassThru</span></span>
<span data-ttu-id="86c89-128">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="86c89-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="86c89-129">Jeśli ten przełącznik jest określony, zwraca zaktualizowany obiekt magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="86c89-129">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="86c89-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c89-130">-ResourceGroupName</span></span>
<span data-ttu-id="86c89-131">Określa nazwę grupy zasobów skojarzonej z magazynem kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="86c89-131">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="86c89-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86c89-132">-ResourceId</span></span>
<span data-ttu-id="86c89-133">Identyfikator zasobu magazynu</span><span class="sxs-lookup"><span data-stu-id="86c89-133">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="86c89-134">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="86c89-134">-VaultName</span></span>
<span data-ttu-id="86c89-135">Określa nazwę magazynu kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="86c89-135">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="86c89-136">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="86c89-136">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="86c89-137">Określa dozwolony identyfikator zasobu sieci wirtualnej reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="86c89-137">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="86c89-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86c89-138">-Confirm</span></span>
<span data-ttu-id="86c89-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86c89-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c89-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c89-140">-WhatIf</span></span>
<span data-ttu-id="86c89-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86c89-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86c89-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="86c89-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c89-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c89-143">CommonParameters</span></span>
<span data-ttu-id="86c89-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c89-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c89-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86c89-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c89-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86c89-146">INPUTS</span></span>

### <span data-ttu-id="86c89-147">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="86c89-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="86c89-148">System. String</span><span class="sxs-lookup"><span data-stu-id="86c89-148">System.String</span></span>

### <span data-ttu-id="86c89-149">System. Nullable "1 [[Microsoft. Azure. Commands. platforming.. models. PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft. Azure. PowerShell. PowerShell... magazyn, wersja = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="86c89-149">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="86c89-150">System. Nullable "1 [[Microsoft. Azure. Commands. platforming.. models. PSKeyVaultNetworkRuleBypassEnum, Microsoft. Azure. PowerShell. PowerShell... magazyn, wersja = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="86c89-150">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="86c89-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86c89-151">OUTPUTS</span></span>

### <span data-ttu-id="86c89-152">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="86c89-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="86c89-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86c89-153">NOTES</span></span>

## <span data-ttu-id="86c89-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86c89-154">RELATED LINKS</span></span>
