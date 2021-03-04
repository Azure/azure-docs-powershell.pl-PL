---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: 6949de15168043e9ede9e8a023f6f5fcec333557
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952506"
---
# <span data-ttu-id="f9133-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f9133-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="f9133-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9133-102">SYNOPSIS</span></span>
<span data-ttu-id="f9133-103">Usuwa regułę sieciową z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f9133-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="f9133-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f9133-104">SYNTAX</span></span>

### <span data-ttu-id="f9133-105">ByVaultName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="f9133-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9133-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f9133-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9133-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f9133-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9133-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f9133-108">DESCRIPTION</span></span>
<span data-ttu-id="f9133-109">Usuwa regułę sieciową z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f9133-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="f9133-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f9133-110">EXAMPLES</span></span>

### <span data-ttu-id="f9133-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9133-111">Example 1</span></span>
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

<span data-ttu-id="f9133-112">To polecenie usuwa regułę sieciową z określonego magazynu pod warunkiem, że znaleziono regułę pasującą do określonego adresu IP i identyfikatora zasobu sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f9133-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="f9133-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9133-113">PARAMETERS</span></span>

### <span data-ttu-id="f9133-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9133-114">-DefaultProfile</span></span>
<span data-ttu-id="f9133-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9133-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9133-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9133-116">-InputObject</span></span>
<span data-ttu-id="f9133-117">Obiekt KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9133-117">KeyVault object</span></span>

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

### <span data-ttu-id="f9133-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="f9133-118">-IpAddressRange</span></span>
<span data-ttu-id="f9133-119">Określa dozwolony zakres adresów IP sieci reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="f9133-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="f9133-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9133-120">-PassThru</span></span>
<span data-ttu-id="f9133-121">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="f9133-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f9133-122">Jeśli ten przełącznik jest określony, zwraca obiekt zaktualizowanego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f9133-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="f9133-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9133-123">-ResourceGroupName</span></span>
<span data-ttu-id="f9133-124">Określa nazwę grupy zasobów skojarzonej z magazynem kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="f9133-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="f9133-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9133-125">-ResourceId</span></span>
<span data-ttu-id="f9133-126">Identyfikator zasobu KeyVault</span><span class="sxs-lookup"><span data-stu-id="f9133-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="f9133-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f9133-127">-VaultName</span></span>
<span data-ttu-id="f9133-128">Określa nazwę magazynu kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="f9133-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="f9133-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f9133-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="f9133-130">Określa dozwolony identyfikator zasobu sieci wirtualnej reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="f9133-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="f9133-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9133-131">-Confirm</span></span>
<span data-ttu-id="f9133-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f9133-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9133-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9133-133">-WhatIf</span></span>
<span data-ttu-id="f9133-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9133-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9133-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f9133-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9133-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9133-136">CommonParameters</span></span>
<span data-ttu-id="f9133-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9133-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9133-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9133-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9133-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9133-139">INPUTS</span></span>

### <span data-ttu-id="f9133-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f9133-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="f9133-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f9133-141">System.String</span></span>

## <span data-ttu-id="f9133-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9133-142">OUTPUTS</span></span>

### <span data-ttu-id="f9133-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f9133-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="f9133-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f9133-144">NOTES</span></span>

## <span data-ttu-id="f9133-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9133-145">RELATED LINKS</span></span>
