---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurermkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultNetworkRule.md
ms.openlocfilehash: f1ff73a753c794ce7528c9af2b480f75d1460815
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545195"
---
# <span data-ttu-id="5d954-101">Remove-AzureRmKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5d954-101">Remove-AzureRmKeyVaultNetworkRule</span></span>

## <span data-ttu-id="5d954-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d954-102">SYNOPSIS</span></span>
<span data-ttu-id="5d954-103">Usuwa regułę sieciową z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="5d954-103">Removes a network rule from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d954-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d954-104">SYNTAX</span></span>

### <span data-ttu-id="5d954-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5d954-105">ByVaultName (Default)</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d954-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5d954-106">ByInputObject</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d954-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d954-107">ByResourceId</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d954-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5d954-108">DESCRIPTION</span></span>
<span data-ttu-id="5d954-109">Usuwa regułę sieciową z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="5d954-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="5d954-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d954-110">EXAMPLES</span></span>

### <span data-ttu-id="5d954-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d954-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzureRmKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

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

<span data-ttu-id="5d954-112">To polecenie usuwa regułę sieciową z określonego magazynu, pod warunkiem znalezienia reguły zgodnej z określonym adresem IP i identyfikatorem zasobu sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5d954-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="5d954-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d954-113">PARAMETERS</span></span>

### <span data-ttu-id="5d954-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d954-114">-DefaultProfile</span></span>
<span data-ttu-id="5d954-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d954-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d954-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5d954-116">-InputObject</span></span>
<span data-ttu-id="5d954-117">Obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="5d954-117">KeyVault object</span></span>

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

### <span data-ttu-id="5d954-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="5d954-118">-IpAddressRange</span></span>
<span data-ttu-id="5d954-119">Określa dozwolony zakres adresów IP sieci w regule sieci.</span><span class="sxs-lookup"><span data-stu-id="5d954-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="5d954-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d954-120">-PassThru</span></span>
<span data-ttu-id="5d954-121">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="5d954-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5d954-122">Jeśli ten przełącznik jest określony, zwraca zaktualizowany obiekt magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="5d954-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="5d954-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d954-123">-ResourceGroupName</span></span>
<span data-ttu-id="5d954-124">Określa nazwę grupy zasobów skojarzonej z magazynem kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="5d954-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="5d954-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d954-125">-ResourceId</span></span>
<span data-ttu-id="5d954-126">Identyfikator zasobu magazynu</span><span class="sxs-lookup"><span data-stu-id="5d954-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="5d954-127">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="5d954-127">-VaultName</span></span>
<span data-ttu-id="5d954-128">Określa nazwę magazynu kluczy, którego reguła sieciowa jest modyfikowana.</span><span class="sxs-lookup"><span data-stu-id="5d954-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="5d954-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5d954-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="5d954-130">Określa dozwolony identyfikator zasobu sieci wirtualnej reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="5d954-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="5d954-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d954-131">-Confirm</span></span>
<span data-ttu-id="5d954-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d954-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d954-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d954-133">-WhatIf</span></span>
<span data-ttu-id="5d954-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d954-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d954-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d954-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d954-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d954-136">CommonParameters</span></span>
<span data-ttu-id="5d954-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d954-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d954-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d954-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d954-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d954-139">INPUTS</span></span>

### <span data-ttu-id="5d954-140">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5d954-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="5d954-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d954-141">OUTPUTS</span></span>

### <span data-ttu-id="5d954-142">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5d954-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="5d954-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d954-143">NOTES</span></span>

## <span data-ttu-id="5d954-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d954-144">RELATED LINKS</span></span>
