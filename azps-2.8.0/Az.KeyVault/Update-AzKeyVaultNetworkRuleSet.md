---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
ms.openlocfilehash: f20099fbd9dd2aa7a9fd6774892d29fbde7ce34b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705087"
---
# <span data-ttu-id="09a57-101">Update-AzKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="09a57-101">Update-AzKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="09a57-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09a57-102">SYNOPSIS</span></span>
<span data-ttu-id="09a57-103">Umożliwia zaktualizowanie zestawu reguł sieci w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="09a57-103">Updates the network rule set on a key vault.</span></span>

## <span data-ttu-id="09a57-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09a57-104">SYNTAX</span></span>

### <span data-ttu-id="09a57-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="09a57-105">ByVaultName (Default)</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09a57-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="09a57-106">ByInputObject</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09a57-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="09a57-107">ByResourceId</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09a57-108">Opis</span><span class="sxs-lookup"><span data-stu-id="09a57-108">DESCRIPTION</span></span>
<span data-ttu-id="09a57-109">Polecenie **Update-AzKeyVaultNetworkRuleSet** powoduje zaktualizowanie reguł sieciowych dotyczących określonego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="09a57-109">The **Update-AzKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="09a57-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09a57-110">EXAMPLES</span></span>

### <span data-ttu-id="09a57-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="09a57-111">Example 1</span></span>
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

<span data-ttu-id="09a57-112">To polecenie aktualizuje zestaw reguł sieci w magazynie o nazwie "Moja magazyn" dla określonego zakresu adresów IP i sieci wirtualnej, umożliwiając ominięcie reguły sieci dla usług platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="09a57-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

## <span data-ttu-id="09a57-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09a57-113">PARAMETERS</span></span>

### <span data-ttu-id="09a57-114">-Bypass</span><span class="sxs-lookup"><span data-stu-id="09a57-114">-Bypass</span></span>
<span data-ttu-id="09a57-115">Określa ominięcie reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="09a57-115">Specifies bypass of network rule.</span></span>

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

### <span data-ttu-id="09a57-116">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="09a57-116">-DefaultAction</span></span>
<span data-ttu-id="09a57-117">Określa domyślną akcję reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="09a57-117">Specifies default action of network rule.</span></span>

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

### <span data-ttu-id="09a57-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09a57-118">-DefaultProfile</span></span>
<span data-ttu-id="09a57-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09a57-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09a57-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="09a57-120">-InputObject</span></span>
<span data-ttu-id="09a57-121">Obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="09a57-121">KeyVault object</span></span>

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

### <span data-ttu-id="09a57-122">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="09a57-122">-IpAddressRange</span></span>
<span data-ttu-id="09a57-123">Określa dozwolony zakres adresów IP sieci w regule sieci.</span><span class="sxs-lookup"><span data-stu-id="09a57-123">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="09a57-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09a57-124">-PassThru</span></span>
<span data-ttu-id="09a57-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="09a57-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="09a57-126">Jeśli ten przełącznik jest określony, zwraca zaktualizowany obiekt magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="09a57-126">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="09a57-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09a57-127">-ResourceGroupName</span></span>
<span data-ttu-id="09a57-128">Określa nazwę grupy zasobów skojarzonej z magazynem kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="09a57-128">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="09a57-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09a57-129">-ResourceId</span></span>
<span data-ttu-id="09a57-130">Identyfikator zasobu magazynu</span><span class="sxs-lookup"><span data-stu-id="09a57-130">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="09a57-131">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="09a57-131">-VaultName</span></span>
<span data-ttu-id="09a57-132">Określa nazwę magazynu kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="09a57-132">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="09a57-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="09a57-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="09a57-134">Określa dozwolony identyfikator zasobu sieci wirtualnej reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="09a57-134">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="09a57-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09a57-135">-Confirm</span></span>
<span data-ttu-id="09a57-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09a57-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09a57-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09a57-137">-WhatIf</span></span>
<span data-ttu-id="09a57-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09a57-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09a57-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="09a57-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09a57-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a57-140">CommonParameters</span></span>
<span data-ttu-id="09a57-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09a57-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a57-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09a57-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a57-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09a57-143">INPUTS</span></span>

### <span data-ttu-id="09a57-144">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="09a57-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="09a57-145">System. String</span><span class="sxs-lookup"><span data-stu-id="09a57-145">System.String</span></span>

### <span data-ttu-id="09a57-146">System. Nullable "1 [[Microsoft. Azure. Commands. platforming.. models. PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft. Azure. PowerShell. PowerShell... magazyn, wersja = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="09a57-146">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="09a57-147">System. Nullable "1 [[Microsoft. Azure. Commands. platforming.. models. PSKeyVaultNetworkRuleBypassEnum, Microsoft. Azure. PowerShell. PowerShell... magazyn, wersja = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="09a57-147">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="09a57-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09a57-148">OUTPUTS</span></span>

### <span data-ttu-id="09a57-149">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="09a57-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="09a57-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09a57-150">NOTES</span></span>

## <span data-ttu-id="09a57-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09a57-151">RELATED LINKS</span></span>
