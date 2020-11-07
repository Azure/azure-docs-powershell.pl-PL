---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: d79c28b09c9f6ca36ae163566574555bb3c50459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718314"
---
# <span data-ttu-id="d7273-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="d7273-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="d7273-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7273-102">SYNOPSIS</span></span>
<span data-ttu-id="d7273-103">Pobiera kluczowe magazyny.</span><span class="sxs-lookup"><span data-stu-id="d7273-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7273-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7273-104">SYNTAX</span></span>

### <span data-ttu-id="d7273-105">ListAllVaultsInSubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d7273-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7273-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="d7273-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7273-107">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="d7273-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7273-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="d7273-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7273-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d7273-109">DESCRIPTION</span></span>
<span data-ttu-id="d7273-110">Polecenie cmdlet **Get-AzureRmKeyVault** pobiera informacje o najważniejszych magazynach w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="d7273-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="d7273-111">Możesz wyświetlić wszystkie wystąpienia najważniejszych magazynów w subskrypcji lub filtrować wyniki według grupy zasobów lub konkretnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d7273-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="d7273-112">Należy zauważyć, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, w przypadku pojedynczego magazynu kluczy należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="d7273-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="d7273-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7273-113">EXAMPLES</span></span>

### <span data-ttu-id="d7273-114">Przykład 1: pobieranie wszystkich najważniejszych magazynów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d7273-114">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault

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

<span data-ttu-id="d7273-115">To polecenie pobiera wszystkie kluczowe magazyny w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d7273-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="d7273-116">Przykład 2: uzyskiwanie określonego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="d7273-116">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault -VaultName 'myvault'

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

<span data-ttu-id="d7273-117">To polecenie umożliwia wyświetlenie magazynu kluczy o nazwie Moja magazyn w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d7273-117">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="d7273-118">Przykład 3: uzyskiwanie najważniejszych magazynów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="d7273-118">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzureRmKeyVault -ResourceGroupName 'myrg1'

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

<span data-ttu-id="d7273-119">To polecenie pobiera wszystkie główne magazyny z grupy zasobów o nazwie ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d7273-119">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="d7273-120">Przykład 4: pobieranie wszystkich usuniętych magazynów kluczy w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d7273-120">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzureRmKeyVault -InRemovedState

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

<span data-ttu-id="d7273-121">To polecenie pobiera wszystkie usunięte magazyny kluczy w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d7273-121">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="d7273-122">Przykład 5: uzyskiwanie usuniętego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="d7273-122">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

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

<span data-ttu-id="d7273-123">To polecenie pobiera usunięte informacje o magazynie kluczy o nazwie myvault4 w bieżącej subskrypcji i w regionie zachód.</span><span class="sxs-lookup"><span data-stu-id="d7273-123">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

## <span data-ttu-id="d7273-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7273-124">PARAMETERS</span></span>

### <span data-ttu-id="d7273-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7273-125">-DefaultProfile</span></span>
<span data-ttu-id="d7273-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d7273-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7273-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d7273-127">-InRemovedState</span></span>
<span data-ttu-id="d7273-128">Określa, czy w wyniku mają być pokazywane uprzednio usunięte magazyny.</span><span class="sxs-lookup"><span data-stu-id="d7273-128">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="d7273-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d7273-129">-Location</span></span>
<span data-ttu-id="d7273-130">Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="d7273-130">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="d7273-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7273-131">-ResourceGroupName</span></span>
<span data-ttu-id="d7273-132">Określa nazwę grupy zasobów skojarzonej z badanym magazynem kluczy lub kluczami kluczy, których dotyczy zapytanie.</span><span class="sxs-lookup"><span data-stu-id="d7273-132">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7273-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="d7273-133">-Tag</span></span>
<span data-ttu-id="d7273-134">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d7273-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d7273-135">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d7273-135">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7273-136">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="d7273-136">-VaultName</span></span>
<span data-ttu-id="d7273-137">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d7273-137">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7273-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7273-138">CommonParameters</span></span>
<span data-ttu-id="d7273-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7273-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7273-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7273-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7273-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7273-141">INPUTS</span></span>

### <span data-ttu-id="d7273-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d7273-142">System.String</span></span>

### <span data-ttu-id="d7273-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d7273-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d7273-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7273-144">OUTPUTS</span></span>

### <span data-ttu-id="d7273-145">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d7273-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d7273-146">Microsoft. Azure. Commands. platforming. models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d7273-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="d7273-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="d7273-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="d7273-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7273-148">NOTES</span></span>

## <span data-ttu-id="d7273-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7273-149">RELATED LINKS</span></span>

[<span data-ttu-id="d7273-150">Nowe — AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="d7273-150">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="d7273-151">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="d7273-151">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
