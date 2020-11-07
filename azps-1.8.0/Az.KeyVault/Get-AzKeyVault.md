---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: 795840d7580d1e7dabb15cf3211ef16d0ccfb7b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868003"
---
# <span data-ttu-id="fe3ee-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="fe3ee-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="fe3ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe3ee-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3ee-103">Pobiera kluczowe magazyny.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-103">Gets key vaults.</span></span>

## <span data-ttu-id="fe3ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe3ee-104">SYNTAX</span></span>

### <span data-ttu-id="fe3ee-105">GetVaultByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fe3ee-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3ee-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="fe3ee-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3ee-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="fe3ee-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe3ee-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fe3ee-108">DESCRIPTION</span></span>
<span data-ttu-id="fe3ee-109">Polecenie cmdlet **Get-AzKeyVault** pobiera informacje o najważniejszych magazynach w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="fe3ee-110">Możesz wyświetlić wszystkie wystąpienia najważniejszych magazynów w subskrypcji lub filtrować wyniki według grupy zasobów lub konkretnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="fe3ee-111">Należy zauważyć, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, w przypadku pojedynczego magazynu kluczy należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="fe3ee-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe3ee-112">EXAMPLES</span></span>

### <span data-ttu-id="fe3ee-113">Przykład 1: pobieranie wszystkich najważniejszych magazynów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fe3ee-113">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault

Vault Name          : myvault1
Resource Group Name : myrg
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.Ke
                      yVault/vaults/myvault1
Tags                :


Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="fe3ee-114">To polecenie pobiera wszystkie kluczowe magazyny w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="fe3ee-115">Przykład 2: uzyskiwanie określonego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="fe3ee-115">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault'

Vault Name                       : myvault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
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

Tags                             :
```

<span data-ttu-id="fe3ee-116">To polecenie umożliwia wyświetlenie magazynu kluczy o nazwie Moja magazyn w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="fe3ee-117">Przykład 3: uzyskiwanie najważniejszych magazynów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="fe3ee-117">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVault -ResourceGroupName 'myrg1'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="fe3ee-118">To polecenie pobiera wszystkie główne magazyny z grupy zasobów o nazwie ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="fe3ee-119">Przykład 4: pobieranie wszystkich usuniętych magazynów kluczy w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fe3ee-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="fe3ee-120">To polecenie pobiera wszystkie usunięte magazyny kluczy w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="fe3ee-121">Przykład 5: uzyskiwanie usuniętego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="fe3ee-121">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="fe3ee-122">To polecenie pobiera usunięte informacje o magazynie kluczy o nazwie myvault4 w bieżącej subskrypcji i w regionie zachód.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="fe3ee-123">Przykład 6: uzyskiwanie najważniejszych magazynów przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="fe3ee-123">Example 6: Get key vaults using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault*'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="fe3ee-124">To polecenie pobiera wszystkie główne magazyny w subskrypcji, która rozpoczyna się od "Moje magazyny".</span><span class="sxs-lookup"><span data-stu-id="fe3ee-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="fe3ee-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe3ee-125">PARAMETERS</span></span>

### <span data-ttu-id="fe3ee-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3ee-126">-DefaultProfile</span></span>
<span data-ttu-id="fe3ee-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fe3ee-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe3ee-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="fe3ee-128">-InRemovedState</span></span>
<span data-ttu-id="fe3ee-129">Określa, czy w wyniku mają być pokazywane uprzednio usunięte magazyny.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3ee-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fe3ee-130">-Location</span></span>
<span data-ttu-id="fe3ee-131">Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-131">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe3ee-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe3ee-132">-ResourceGroupName</span></span>
<span data-ttu-id="fe3ee-133">Określa nazwę grupy zasobów skojarzonej z badanym magazynem kluczy lub kluczami kluczy, których dotyczy zapytanie.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fe3ee-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe3ee-134">-Tag</span></span>
<span data-ttu-id="fe3ee-135">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fe3ee-136">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="fe3ee-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe3ee-137">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="fe3ee-137">-VaultName</span></span>
<span data-ttu-id="fe3ee-138">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fe3ee-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3ee-139">CommonParameters</span></span>
<span data-ttu-id="fe3ee-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3ee-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3ee-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe3ee-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3ee-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe3ee-142">INPUTS</span></span>

### <span data-ttu-id="fe3ee-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fe3ee-143">System.String</span></span>

### <span data-ttu-id="fe3ee-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fe3ee-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fe3ee-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe3ee-145">OUTPUTS</span></span>

### <span data-ttu-id="fe3ee-146">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="fe3ee-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="fe3ee-147">Microsoft. Azure. Commands. platforming. models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fe3ee-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="fe3ee-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="fe3ee-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="fe3ee-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe3ee-149">NOTES</span></span>

## <span data-ttu-id="fe3ee-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe3ee-150">RELATED LINKS</span></span>

[<span data-ttu-id="fe3ee-151">Nowe — AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="fe3ee-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="fe3ee-152">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="fe3ee-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
