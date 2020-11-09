---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: c437611603bab6b2c4b9fff5cd0696e306182afa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304632"
---
# <span data-ttu-id="94bbf-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="94bbf-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="94bbf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="94bbf-103">Dodaje regułę ograniczającą dostęp do magazynu kluczy na podstawie adresu internetowego klienta.</span><span class="sxs-lookup"><span data-stu-id="94bbf-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="94bbf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94bbf-104">SYNTAX</span></span>

### <span data-ttu-id="94bbf-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="94bbf-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94bbf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="94bbf-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94bbf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="94bbf-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94bbf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="94bbf-108">DESCRIPTION</span></span>
<span data-ttu-id="94bbf-109">Polecenie cmdlet **Add-AzKeyVaultNetworkRule** udziela lub ogranicza dostęp do magazynu kluczy zestawowi rozmówcy wyznaczonym przez adresy IP lub sieć wirtualną, do której należą.</span><span class="sxs-lookup"><span data-stu-id="94bbf-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="94bbf-110">Reguła ma możliwość ograniczenia dostępu dla innych użytkowników, aplikacji lub grup zabezpieczeń, którym udzielono uprawnień za pośrednictwem zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="94bbf-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

<span data-ttu-id="94bbf-111">Pamiętaj, że w `10.0.0.0-10.255.255.255` celu dodania reguł sieciowych nie można użyć żadnego zakresu adresów IP w zakresie (prywatne adresy IP).</span><span class="sxs-lookup"><span data-stu-id="94bbf-111">Please note that any IP range inside `10.0.0.0-10.255.255.255` (private IP addresses) cannot be used to add network rules.</span></span>

## <span data-ttu-id="94bbf-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94bbf-112">EXAMPLES</span></span>

### <span data-ttu-id="94bbf-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94bbf-113">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Add-AzKeyVaultNetworkRule -VaultName myvault -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myvault
Resource Group Name              : myRG
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myRG/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
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
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myRG/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="94bbf-114">To polecenie dodaje regułę sieciową do określonego magazynu, umożliwiając dostęp do określonego adresu IP z sieci wirtualnej określonej przez $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="94bbf-114">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="94bbf-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94bbf-115">PARAMETERS</span></span>

### <span data-ttu-id="94bbf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94bbf-116">-DefaultProfile</span></span>
<span data-ttu-id="94bbf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94bbf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94bbf-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="94bbf-118">-InputObject</span></span>
<span data-ttu-id="94bbf-119">Obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="94bbf-119">KeyVault object</span></span>

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

### <span data-ttu-id="94bbf-120">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="94bbf-120">-IpAddressRange</span></span>
<span data-ttu-id="94bbf-121">Określa dozwolony zakres adresów IP sieci w regule sieci.</span><span class="sxs-lookup"><span data-stu-id="94bbf-121">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="94bbf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94bbf-122">-PassThru</span></span>
<span data-ttu-id="94bbf-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="94bbf-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="94bbf-124">Jeśli ten przełącznik jest określony, zwraca zaktualizowany obiekt magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="94bbf-124">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="94bbf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94bbf-125">-ResourceGroupName</span></span>
<span data-ttu-id="94bbf-126">Określa nazwę grupy zasobów skojarzonej z magazynem kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="94bbf-126">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="94bbf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94bbf-127">-ResourceId</span></span>
<span data-ttu-id="94bbf-128">Identyfikator zasobu magazynu</span><span class="sxs-lookup"><span data-stu-id="94bbf-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="94bbf-129">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="94bbf-129">-VaultName</span></span>
<span data-ttu-id="94bbf-130">Określa nazwę magazynu kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="94bbf-130">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="94bbf-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="94bbf-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="94bbf-132">Określa dozwolony identyfikator zasobu sieci wirtualnej reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="94bbf-132">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="94bbf-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94bbf-133">-Confirm</span></span>
<span data-ttu-id="94bbf-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94bbf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94bbf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94bbf-135">-WhatIf</span></span>
<span data-ttu-id="94bbf-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94bbf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94bbf-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="94bbf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94bbf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94bbf-138">CommonParameters</span></span>
<span data-ttu-id="94bbf-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94bbf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94bbf-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94bbf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94bbf-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94bbf-141">INPUTS</span></span>

### <span data-ttu-id="94bbf-142">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="94bbf-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="94bbf-143">System. String</span><span class="sxs-lookup"><span data-stu-id="94bbf-143">System.String</span></span>

## <span data-ttu-id="94bbf-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94bbf-144">OUTPUTS</span></span>

### <span data-ttu-id="94bbf-145">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="94bbf-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="94bbf-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94bbf-146">NOTES</span></span>

## <span data-ttu-id="94bbf-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94bbf-147">RELATED LINKS</span></span>
