---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurermkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureRmKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureRmKeyVaultNetworkRuleSet.md
ms.openlocfilehash: b1a0081f24932cf25026bdea4e9064e9dbb5a0cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543784"
---
# <span data-ttu-id="6b411-101">Update-AzureRmKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b411-101">Update-AzureRmKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="6b411-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b411-102">SYNOPSIS</span></span>
<span data-ttu-id="6b411-103">Umożliwia zaktualizowanie zestawu reguł sieci w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="6b411-103">Updates the network rule set on a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b411-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b411-104">SYNTAX</span></span>

### <span data-ttu-id="6b411-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6b411-105">ByVaultName (Default)</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b411-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6b411-106">ByInputObject</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b411-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6b411-107">ByResourceId</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b411-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6b411-108">DESCRIPTION</span></span>
<span data-ttu-id="6b411-109">Polecenie **Update-AzureRmKeyVaultNetworkRuleSet** powoduje zaktualizowanie reguł sieciowych dotyczących określonego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="6b411-109">The **Update-AzureRmKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="6b411-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b411-110">EXAMPLES</span></span>

### <span data-ttu-id="6b411-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6b411-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzureRmKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

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

<span data-ttu-id="6b411-112">To polecenie aktualizuje zestaw reguł sieci w magazynie o nazwie "Moja magazyn" dla określonego zakresu adresów IP i sieci wirtualnej, umożliwiając ominięcie reguły sieci dla usług platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6b411-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

## <span data-ttu-id="6b411-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b411-113">PARAMETERS</span></span>

### <span data-ttu-id="6b411-114">-Bypass</span><span class="sxs-lookup"><span data-stu-id="6b411-114">-Bypass</span></span>
<span data-ttu-id="6b411-115">Określa ominięcie reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="6b411-115">Specifies bypass of network rule.</span></span>

```yaml
Type: PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b411-116">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="6b411-116">-DefaultAction</span></span>
<span data-ttu-id="6b411-117">Określa domyślną akcję reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="6b411-117">Specifies default action of network rule.</span></span>

```yaml
Type: PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b411-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b411-118">-DefaultProfile</span></span>
<span data-ttu-id="6b411-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b411-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b411-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6b411-120">-InputObject</span></span>
<span data-ttu-id="6b411-121">Obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="6b411-121">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b411-122">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="6b411-122">-IpAddressRange</span></span>
<span data-ttu-id="6b411-123">Określa dozwolony zakres adresów IP sieci w regule sieci.</span><span class="sxs-lookup"><span data-stu-id="6b411-123">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b411-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b411-124">-PassThru</span></span>
<span data-ttu-id="6b411-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="6b411-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6b411-126">Jeśli ten przełącznik jest określony, zwraca zaktualizowany obiekt magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="6b411-126">If this switch is specified, it returns the updated key vault object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b411-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b411-127">-ResourceGroupName</span></span>
<span data-ttu-id="6b411-128">Określa nazwę grupy zasobów skojarzonej z magazynem kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="6b411-128">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b411-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b411-129">-ResourceId</span></span>
<span data-ttu-id="6b411-130">Identyfikator zasobu magazynu</span><span class="sxs-lookup"><span data-stu-id="6b411-130">KeyVault Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b411-131">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="6b411-131">-VaultName</span></span>
<span data-ttu-id="6b411-132">Określa nazwę magazynu kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="6b411-132">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b411-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="6b411-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="6b411-134">Określa dozwolony identyfikator zasobu sieci wirtualnej reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="6b411-134">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b411-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b411-135">-Confirm</span></span>
<span data-ttu-id="6b411-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b411-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b411-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b411-137">-WhatIf</span></span>
<span data-ttu-id="6b411-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b411-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b411-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6b411-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b411-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b411-140">CommonParameters</span></span>
<span data-ttu-id="6b411-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b411-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b411-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b411-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b411-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b411-143">INPUTS</span></span>

### <span data-ttu-id="6b411-144">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="6b411-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="6b411-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b411-145">OUTPUTS</span></span>

### <span data-ttu-id="6b411-146">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="6b411-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="6b411-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b411-147">NOTES</span></span>

## <span data-ttu-id="6b411-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b411-148">RELATED LINKS</span></span>
