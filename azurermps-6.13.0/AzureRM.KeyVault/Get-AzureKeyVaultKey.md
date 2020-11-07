---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: e8763fcb74c3177e91992996f00c670b32ffbbb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718319"
---
# <span data-ttu-id="55923-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="55923-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="55923-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55923-102">SYNOPSIS</span></span>
<span data-ttu-id="55923-103">Pobiera klucze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="55923-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55923-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55923-104">SYNTAX</span></span>

### <span data-ttu-id="55923-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="55923-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55923-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="55923-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55923-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="55923-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55923-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="55923-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55923-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="55923-109">ByInputObjectKeyName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55923-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="55923-110">ByInputObjectKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55923-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="55923-111">ByResourceIdVaultName</span></span>
```
Get-AzureKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55923-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="55923-112">ByResourceIdKeyName</span></span>
```
Get-AzureKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55923-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="55923-113">ByResourceIdKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55923-114">Opis</span><span class="sxs-lookup"><span data-stu-id="55923-114">DESCRIPTION</span></span>
<span data-ttu-id="55923-115">Polecenie cmdlet **Get-AzureKeyVaultKey** pobiera klucze magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="55923-115">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="55923-116">To polecenie cmdlet umożliwia pobieranie określonego pakietu **Microsoft. Azure. Commands. Key. MODELES** lub lista wszystkich obiektów **pakietu** kluczy w magazynie kluczy lub według wersji.</span><span class="sxs-lookup"><span data-stu-id="55923-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="55923-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55923-117">EXAMPLES</span></span>

### <span data-ttu-id="55923-118">Przykład 1. pobieranie wszystkich kluczy w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="55923-118">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'contoso'

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

<span data-ttu-id="55923-119">To polecenie pobiera wszystkie klucze w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="55923-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="55923-120">Przykład 2: uzyskiwanie bieżącej wersji klucza</span><span class="sxs-lookup"><span data-stu-id="55923-120">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

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

<span data-ttu-id="55923-121">To polecenie pobiera aktualną wersję klucza o nazwie TEST1 w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="55923-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="55923-122">Przykład 3: pobieranie wszystkich wersji klucza</span><span class="sxs-lookup"><span data-stu-id="55923-122">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

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

<span data-ttu-id="55923-123">To polecenie pobiera wszystkie wersje klucza o nazwie ITPfx w kluczu vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="55923-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="55923-124">Przykład 4: uzyskiwanie określonej wersji klucza</span><span class="sxs-lookup"><span data-stu-id="55923-124">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

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

<span data-ttu-id="55923-125">To polecenie pobiera określoną wersję klucza o nazwie TEST1 w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="55923-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="55923-126">Po uruchomieniu tego polecenia możesz sprawdzić różne właściwości klucza, przechodząc do obiektu $Key.</span><span class="sxs-lookup"><span data-stu-id="55923-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="55923-127">Przykład 5: Uzyskaj wszystkie klucze, które zostały usunięte, ale nie zostały oczyszczone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="55923-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'contoso' -InRemovedState

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

<span data-ttu-id="55923-128">To polecenie pobiera wszystkie klucze, które zostały wcześniej usunięte, ale nie zostały oczyszczone w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="55923-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="55923-129">Przykład 6: Pobiera klucze ITPfx, które zostały usunięte, ale nie zostały oczyszczone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="55923-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

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

<span data-ttu-id="55923-130">To polecenie pobiera klucze test3, które zostały wcześniej usunięte, ale nie zostały oczyszczone w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="55923-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="55923-131">To polecenie zwróci metadane, takie jak Data usunięcia, oraz zaplanowaną datę przeczyszczania tego usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="55923-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="55923-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55923-132">PARAMETERS</span></span>

### <span data-ttu-id="55923-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55923-133">-DefaultProfile</span></span>
<span data-ttu-id="55923-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="55923-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55923-135">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="55923-135">-IncludeVersions</span></span>
<span data-ttu-id="55923-136">Wskazuje, że to polecenie cmdlet pobiera wszystkie wersje klucza.</span><span class="sxs-lookup"><span data-stu-id="55923-136">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="55923-137">Bieżąca wersja klucza to pierwsza z nich na liście.</span><span class="sxs-lookup"><span data-stu-id="55923-137">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="55923-138">W przypadku określenia tego parametru należy również określić *nazwę* i parametry *magazynu* .</span><span class="sxs-lookup"><span data-stu-id="55923-138">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="55923-139">Jeśli nie określisz parametru *IncludeVersions* , to polecenie cmdlet pobiera bieżącą wersję klucza o określonej *nazwie*.</span><span class="sxs-lookup"><span data-stu-id="55923-139">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, ByInputObjectKeyVersions, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55923-140">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="55923-140">-InputObject</span></span>
<span data-ttu-id="55923-141">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="55923-141">KeyVault object.</span></span>

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

### <span data-ttu-id="55923-142">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="55923-142">-InRemovedState</span></span>
<span data-ttu-id="55923-143">Określa, czy w wyniku mają być pokazywane uprzednio usunięte klucze.</span><span class="sxs-lookup"><span data-stu-id="55923-143">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55923-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="55923-144">-Name</span></span>
<span data-ttu-id="55923-145">Określa nazwę pakietu kluczy, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="55923-145">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55923-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55923-146">-ResourceId</span></span>
<span data-ttu-id="55923-147">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="55923-147">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55923-148">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="55923-148">-VaultName</span></span>
<span data-ttu-id="55923-149">Określa nazwę magazynu kluczy, z którego to polecenie cmdlet pobiera klucze.</span><span class="sxs-lookup"><span data-stu-id="55923-149">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="55923-150">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy, jaką ten parametr określa i wybrane środowisko.</span><span class="sxs-lookup"><span data-stu-id="55923-150">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="55923-151">-Version</span><span class="sxs-lookup"><span data-stu-id="55923-151">-Version</span></span>
<span data-ttu-id="55923-152">Określa wersję klucza.</span><span class="sxs-lookup"><span data-stu-id="55923-152">Specifies the key version.</span></span>
<span data-ttu-id="55923-153">To polecenie cmdlet konstruuje nazwę FQDN klucza na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, nazwy klucza i wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="55923-153">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByInputObjectKeyName, ByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55923-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55923-154">CommonParameters</span></span>
<span data-ttu-id="55923-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55923-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55923-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55923-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55923-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55923-157">INPUTS</span></span>

### <span data-ttu-id="55923-158">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="55923-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="55923-159">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="55923-159">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="55923-160">System. String</span><span class="sxs-lookup"><span data-stu-id="55923-160">System.String</span></span>

## <span data-ttu-id="55923-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55923-161">OUTPUTS</span></span>

### <span data-ttu-id="55923-162">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="55923-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="55923-163">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="55923-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="55923-164">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="55923-164">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="55923-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="55923-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="55923-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55923-166">NOTES</span></span>

## <span data-ttu-id="55923-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55923-167">RELATED LINKS</span></span>

[<span data-ttu-id="55923-168">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="55923-168">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="55923-169">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="55923-169">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="55923-170">Cofanie — AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="55923-170">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="55923-171">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="55923-171">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

