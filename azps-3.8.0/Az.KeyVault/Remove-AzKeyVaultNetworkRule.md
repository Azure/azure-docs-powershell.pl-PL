---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: b1c0326be98efed91ce53c9cf04cdee6fce658f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050600"
---
# <span data-ttu-id="fbadf-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fbadf-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="fbadf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbadf-102">SYNOPSIS</span></span>
<span data-ttu-id="fbadf-103">Usuwa regułę sieciową z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fbadf-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="fbadf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbadf-104">SYNTAX</span></span>

### <span data-ttu-id="fbadf-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fbadf-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbadf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fbadf-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbadf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fbadf-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbadf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fbadf-108">DESCRIPTION</span></span>
<span data-ttu-id="fbadf-109">Usuwa regułę sieciową z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fbadf-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="fbadf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbadf-110">EXAMPLES</span></span>

### <span data-ttu-id="fbadf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fbadf-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myrg
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
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="fbadf-112">To polecenie usuwa regułę sieciową z określonego magazynu, pod warunkiem znalezienia reguły zgodnej z określonym adresem IP i identyfikatorem zasobu sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fbadf-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="fbadf-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbadf-113">PARAMETERS</span></span>

### <span data-ttu-id="fbadf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbadf-114">-DefaultProfile</span></span>
<span data-ttu-id="fbadf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbadf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbadf-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fbadf-116">-InputObject</span></span>
<span data-ttu-id="fbadf-117">Obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="fbadf-117">KeyVault object</span></span>

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

### <span data-ttu-id="fbadf-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="fbadf-118">-IpAddressRange</span></span>
<span data-ttu-id="fbadf-119">Określa dozwolony zakres adresów IP sieci w regule sieci.</span><span class="sxs-lookup"><span data-stu-id="fbadf-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="fbadf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbadf-120">-PassThru</span></span>
<span data-ttu-id="fbadf-121">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="fbadf-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fbadf-122">Jeśli ten przełącznik jest określony, zwraca zaktualizowany obiekt magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fbadf-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="fbadf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbadf-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbadf-124">Określa nazwę grupy zasobów skojarzonej z magazynem kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="fbadf-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="fbadf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbadf-125">-ResourceId</span></span>
<span data-ttu-id="fbadf-126">Identyfikator zasobu magazynu</span><span class="sxs-lookup"><span data-stu-id="fbadf-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="fbadf-127">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="fbadf-127">-VaultName</span></span>
<span data-ttu-id="fbadf-128">Określa nazwę magazynu kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="fbadf-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="fbadf-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="fbadf-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="fbadf-130">Określa dozwolony identyfikator zasobu sieci wirtualnej reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="fbadf-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="fbadf-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbadf-131">-Confirm</span></span>
<span data-ttu-id="fbadf-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbadf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbadf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbadf-133">-WhatIf</span></span>
<span data-ttu-id="fbadf-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbadf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbadf-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fbadf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbadf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbadf-136">CommonParameters</span></span>
<span data-ttu-id="fbadf-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbadf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbadf-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbadf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbadf-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbadf-139">INPUTS</span></span>

### <span data-ttu-id="fbadf-140">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="fbadf-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="fbadf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fbadf-141">System.String</span></span>

## <span data-ttu-id="fbadf-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbadf-142">OUTPUTS</span></span>

### <span data-ttu-id="fbadf-143">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="fbadf-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="fbadf-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbadf-144">NOTES</span></span>

## <span data-ttu-id="fbadf-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbadf-145">RELATED LINKS</span></span>
