---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 81276c0896d6cb6685d3ce3ee71bb72cb39b690a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955825"
---
# <span data-ttu-id="21610-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="21610-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="21610-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21610-102">SYNOPSIS</span></span>
<span data-ttu-id="21610-103">Pobiera klucze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="21610-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="21610-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="21610-104">SYNTAX</span></span>

### <span data-ttu-id="21610-105">ByVaultName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="21610-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="21610-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="21610-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-108">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="21610-108">HsmByKeyName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-109">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="21610-109">HsmByVaultName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-110">HsmByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="21610-110">HsmByKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-111">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="21610-111">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-112">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="21610-112">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-113">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="21610-113">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-114">HsmByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="21610-114">HsmByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-115">HsmByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="21610-115">HsmByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-116">HsmByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="21610-116">HsmByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-117">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="21610-117">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-118">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="21610-118">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-119">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="21610-119">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-120">HsmByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="21610-120">HsmByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-121">HsmByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="21610-121">HsmByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21610-122">HsmByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="21610-122">HsmByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21610-123">OPIS</span><span class="sxs-lookup"><span data-stu-id="21610-123">DESCRIPTION</span></span>
<span data-ttu-id="21610-124">Polecenie **cmdlet Get-AzKeyVaultKey** pobiera klucze magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21610-124">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="21610-125">To polecenie cmdlet pobiera określoną usługę **Microsoft.Azure.Commands.KeyVault.Models.Key Jednakdle** lub listę wszystkich obiektów **Key Jednakdle** w magazynie kluczy lub według wersji.</span><span class="sxs-lookup"><span data-stu-id="21610-125">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="21610-126">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="21610-126">EXAMPLES</span></span>

### <span data-ttu-id="21610-127">Przykład 1. Uzyskiwanie wszystkich kluczy w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="21610-127">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso'

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="21610-128">To polecenie pobiera wszystkie klucze z magazynu kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="21610-128">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="21610-129">Przykład 2. Uzyskiwanie bieżącej wersji klucza</span><span class="sxs-lookup"><span data-stu-id="21610-129">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="21610-130">To polecenie pobiera bieżącą wersję klucza o nazwie test1 w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="21610-130">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="21610-131">Przykład 3. Uzyskiwanie wszystkich wersji klucza</span><span class="sxs-lookup"><span data-stu-id="21610-131">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="21610-132">To polecenie pobiera wszystkie wersje klucza o nazwie ITPfx w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="21610-132">This command gets all versions the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="21610-133">Przykład 4. Uzyskiwanie określonej wersji klucza</span><span class="sxs-lookup"><span data-stu-id="21610-133">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="21610-134">To polecenie pobiera określoną wersję klucza o nazwie test1 w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="21610-134">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="21610-135">Po uruchomieniu tego polecenia możesz sprawdzać różne właściwości klucza, poruszając się po $Key obiektu.</span><span class="sxs-lookup"><span data-stu-id="21610-135">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="21610-136">Przykład 5. Uzyskiwanie wszystkich kluczy, które zostały usunięte, ale nie są czyszone dla tego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="21610-136">Example 5: Get all the keys that have been deleted but not purged for this key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="21610-137">To polecenie pobiera wszystkie klucze, które zostały wcześniej usunięte, ale nie przeczyszono, w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="21610-137">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="21610-138">Przykład 6. Pobiera klucz ITPfx, który został usunięty, ale nie przeczyszczony dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="21610-138">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3/1af807cc331a49d0b52b7c75e1b2366e
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="21610-139">To polecenie pobiera test klucza3, który został wcześniej usunięty, ale nie przeczyszczony, w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="21610-139">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="21610-140">To polecenie zwróci metadane, takie jak data usunięcia i zaplanowana data usunięcia tego usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="21610-140">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="21610-141">Przykład 7. Uzyskiwanie wszystkich kluczy w magazynie kluczy przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="21610-141">Example 7: Get all the keys in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName "test*"

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="21610-142">To polecenie pobiera wszystkie klucze w magazynie kluczy o nazwie Contoso, które zaczynają się od "testu".</span><span class="sxs-lookup"><span data-stu-id="21610-142">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="21610-143">Przykład 8. Pobieranie klucza publicznego jako pliku pem</span><span class="sxs-lookup"><span data-stu-id="21610-143">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="21610-144">Klucz publiczny klucza RSA można pobrać, określając `-OutFile` parametr.</span><span class="sxs-lookup"><span data-stu-id="21610-144">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="21610-145">Jest to jeden z kroków importowania kluczy chronionych przez HSM do magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21610-145">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="21610-146">Zobacz https://docs.microsoft.com/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="21610-146">See https://docs.microsoft.com/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="21610-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21610-147">PARAMETERS</span></span>

### <span data-ttu-id="21610-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21610-148">-DefaultProfile</span></span>
<span data-ttu-id="21610-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="21610-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21610-150">-HsmName</span><span class="sxs-lookup"><span data-stu-id="21610-150">-HsmName</span></span>
<span data-ttu-id="21610-151">Nazwa HSM.</span><span class="sxs-lookup"><span data-stu-id="21610-151">HSM name.</span></span> <span data-ttu-id="21610-152">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="21610-152">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName, HsmByVaultName, HsmByKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21610-153">- HsmObject</span><span class="sxs-lookup"><span data-stu-id="21610-153">-HsmObject</span></span>
<span data-ttu-id="21610-154">Obiekt HSM.</span><span class="sxs-lookup"><span data-stu-id="21610-154">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObjectVaultName, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21610-155">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="21610-155">-HsmResourceId</span></span>
<span data-ttu-id="21610-156">Identyfikator zasobu HSM.</span><span class="sxs-lookup"><span data-stu-id="21610-156">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceIdVaultName, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21610-157">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="21610-157">-IncludeVersions</span></span>
<span data-ttu-id="21610-158">Wskazuje, że to polecenie cmdlet pobiera wszystkie wersje klucza.</span><span class="sxs-lookup"><span data-stu-id="21610-158">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="21610-159">Bieżąca wersja klucza jest pierwszą wersją na liście.</span><span class="sxs-lookup"><span data-stu-id="21610-159">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="21610-160">Jeśli określisz ten parametr, musisz również określić parametry *Name (Nazwa) i* *VaultName (Nazwa magazynu).*</span><span class="sxs-lookup"><span data-stu-id="21610-160">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="21610-161">Jeśli parametr *IncludeVersions* nie zostanie określony, to polecenie cmdlet pobiera bieżącą wersję klucza o określonej *nazwie.*</span><span class="sxs-lookup"><span data-stu-id="21610-161">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, HsmByKeyVersions, ByInputObjectKeyVersions, HsmByInputObjectKeyVersions, ByResourceIdKeyVersions, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21610-162">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21610-162">-InputObject</span></span>
<span data-ttu-id="21610-163">Obiekt KeyVault.</span><span class="sxs-lookup"><span data-stu-id="21610-163">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21610-164">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="21610-164">-InRemovedState</span></span>
<span data-ttu-id="21610-165">Określa, czy poprzednio usunięte klucze mają być wyświetlane w wynikach</span><span class="sxs-lookup"><span data-stu-id="21610-165">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21610-166">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="21610-166">-Name</span></span>
<span data-ttu-id="21610-167">Określa nazwę pakietu kluczy do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="21610-167">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, HsmByKeyName, HsmByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="21610-168">-OutFile</span><span class="sxs-lookup"><span data-stu-id="21610-168">-OutFile</span></span>
<span data-ttu-id="21610-169">Określa plik wyjściowy, dla którego to polecenie cmdlet zapisuje klucz.</span><span class="sxs-lookup"><span data-stu-id="21610-169">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="21610-170">Klucz publiczny jest domyślnie zapisywany w formacie PEM.</span><span class="sxs-lookup"><span data-stu-id="21610-170">The public key is saved in PEM format by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21610-171">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21610-171">-ResourceId</span></span>
<span data-ttu-id="21610-172">Identyfikator zasobu KeyVault.</span><span class="sxs-lookup"><span data-stu-id="21610-172">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21610-173">-VaultName</span><span class="sxs-lookup"><span data-stu-id="21610-173">-VaultName</span></span>
<span data-ttu-id="21610-174">Określa nazwę magazynu kluczy, z którego to polecenie cmdlet pobiera klucze.</span><span class="sxs-lookup"><span data-stu-id="21610-174">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="21610-175">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy, która jest określana przez ten parametr i wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="21610-175">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21610-176">— Wersja</span><span class="sxs-lookup"><span data-stu-id="21610-176">-Version</span></span>
<span data-ttu-id="21610-177">Określa wersję klucza.</span><span class="sxs-lookup"><span data-stu-id="21610-177">Specifies the key version.</span></span>
<span data-ttu-id="21610-178">To polecenie cmdlet konstruuje nazwę FQDN klucza na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, nazwy klucza i wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="21610-178">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName, ByInputObjectKeyName, HsmByInputObjectKeyName, ByResourceIdKeyName, HsmByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21610-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21610-179">CommonParameters</span></span>
<span data-ttu-id="21610-180">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21610-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21610-181">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21610-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21610-182">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21610-182">INPUTS</span></span>

### <span data-ttu-id="21610-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="21610-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="21610-184">System.String</span><span class="sxs-lookup"><span data-stu-id="21610-184">System.String</span></span>

## <span data-ttu-id="21610-185">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21610-185">OUTPUTS</span></span>

### <span data-ttu-id="21610-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="21610-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="21610-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="21610-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="21610-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="21610-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="21610-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="21610-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="21610-190">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="21610-190">NOTES</span></span>

## <span data-ttu-id="21610-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21610-191">RELATED LINKS</span></span>

[<span data-ttu-id="21610-192">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="21610-192">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="21610-193">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="21610-193">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="21610-194">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="21610-194">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="21610-195">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="21610-195">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

