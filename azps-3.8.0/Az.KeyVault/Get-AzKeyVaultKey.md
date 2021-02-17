---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: cab778247e6e3ae9db3549beae7fcd7495526757
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412099"
---
# <span data-ttu-id="0c80a-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c80a-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="0c80a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c80a-102">SYNOPSIS</span></span>
<span data-ttu-id="0c80a-103">Pobiera klucze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="0c80a-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="0c80a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0c80a-104">SYNTAX</span></span>

### <span data-ttu-id="0c80a-105">ByVaultName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="0c80a-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c80a-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="0c80a-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c80a-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="0c80a-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c80a-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="0c80a-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c80a-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="0c80a-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c80a-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="0c80a-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c80a-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="0c80a-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c80a-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="0c80a-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c80a-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="0c80a-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c80a-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="0c80a-114">DESCRIPTION</span></span>
<span data-ttu-id="0c80a-115">Polecenie **cmdlet Get-AzKeyVaultKey** pobiera klucze magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0c80a-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="0c80a-116">To polecenie cmdlet pobiera określoną usługę **Microsoft.Azure.Commands.KeyVault.Models.KeySłudze lub** listę wszystkich obiektów **Key Jednakdle** w magazynie kluczy lub według wersji.</span><span class="sxs-lookup"><span data-stu-id="0c80a-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="0c80a-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0c80a-117">EXAMPLES</span></span>

### <span data-ttu-id="0c80a-118">Przykład 1. Uzyskiwanie wszystkich kluczy w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="0c80a-118">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="0c80a-119">To polecenie pobiera wszystkie klucze z magazynu kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="0c80a-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="0c80a-120">Przykład 2. Uzyskiwanie bieżącej wersji klucza</span><span class="sxs-lookup"><span data-stu-id="0c80a-120">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="0c80a-121">To polecenie pobiera bieżącą wersję klucza o nazwie test1 w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="0c80a-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="0c80a-122">Przykład 3. Uzyskiwanie wszystkich wersji klucza</span><span class="sxs-lookup"><span data-stu-id="0c80a-122">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="0c80a-123">To polecenie pobiera wszystkie wersje klucza o nazwie ITPfx w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="0c80a-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="0c80a-124">Przykład 4. Uzyskiwanie określonej wersji klucza</span><span class="sxs-lookup"><span data-stu-id="0c80a-124">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="0c80a-125">To polecenie pobiera określoną wersję klucza o nazwie test1 w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="0c80a-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="0c80a-126">Po uruchomieniu tego polecenia możesz sprawdzać różne właściwości klucza, przechodząc między $Key obiektami.</span><span class="sxs-lookup"><span data-stu-id="0c80a-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="0c80a-127">Przykład 5. Uzyskaj wszystkie klucze, które zostały usunięte, ale nie zostały wyczyszone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="0c80a-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="0c80a-128">To polecenie pobiera wszystkie klucze, które zostały wcześniej usunięte, ale nie przeczyszono, w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="0c80a-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="0c80a-129">Przykład 6. Pobiera klucz ITPfx, który został usunięty, ale nie został przeczyszony dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="0c80a-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="0c80a-130">To polecenie pobiera test3 klucza, który został wcześniej usunięty, ale nie przeczyszczony, w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="0c80a-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="0c80a-131">To polecenie zwróci metadane, takie jak data usunięcia i zaplanowana data usunięcia tego usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="0c80a-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="0c80a-132">Przykład 7. Uzyskiwanie wszystkich kluczy w magazynie kluczy przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="0c80a-132">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="0c80a-133">To polecenie pobiera wszystkie klucze w magazynie kluczy o nazwie Contoso, które zaczynają się od "testu".</span><span class="sxs-lookup"><span data-stu-id="0c80a-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

## <span data-ttu-id="0c80a-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c80a-134">PARAMETERS</span></span>

### <span data-ttu-id="0c80a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c80a-135">-DefaultProfile</span></span>
<span data-ttu-id="0c80a-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0c80a-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c80a-137">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="0c80a-137">-IncludeVersions</span></span>
<span data-ttu-id="0c80a-138">Wskazuje, że to polecenie cmdlet pobiera wszystkie wersje klucza.</span><span class="sxs-lookup"><span data-stu-id="0c80a-138">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="0c80a-139">Bieżąca wersja klucza jest pierwszą wersją na liście.</span><span class="sxs-lookup"><span data-stu-id="0c80a-139">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="0c80a-140">Jeśli określisz ten parametr, musisz również określić parametry *Name (Nazwa) i* *VaultName (Nazwa magazynu).*</span><span class="sxs-lookup"><span data-stu-id="0c80a-140">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="0c80a-141">Jeśli parametr *IncludeVersions* nie zostanie określony, to polecenie cmdlet pobiera bieżącą wersję klucza o określonej *nazwie.*</span><span class="sxs-lookup"><span data-stu-id="0c80a-141">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

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

### <span data-ttu-id="0c80a-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c80a-142">-InputObject</span></span>
<span data-ttu-id="0c80a-143">Obiekt KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0c80a-143">KeyVault object.</span></span>

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

### <span data-ttu-id="0c80a-144">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="0c80a-144">-InRemovedState</span></span>
<span data-ttu-id="0c80a-145">Określa, czy poprzednio usunięte klucze mają być wyświetlane w wynikach</span><span class="sxs-lookup"><span data-stu-id="0c80a-145">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="0c80a-146">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0c80a-146">-Name</span></span>
<span data-ttu-id="0c80a-147">Określa nazwę pakietu kluczy do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="0c80a-147">Specifies the name of the key bundle to get.</span></span>

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

### <span data-ttu-id="0c80a-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c80a-148">-ResourceId</span></span>
<span data-ttu-id="0c80a-149">Identyfikator zasobu KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0c80a-149">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="0c80a-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0c80a-150">-VaultName</span></span>
<span data-ttu-id="0c80a-151">Określa nazwę magazynu kluczy, z którego to polecenie cmdlet pobiera klucze.</span><span class="sxs-lookup"><span data-stu-id="0c80a-151">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="0c80a-152">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy, która jest określana przez ten parametr i wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="0c80a-152">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="0c80a-153">— Wersja</span><span class="sxs-lookup"><span data-stu-id="0c80a-153">-Version</span></span>
<span data-ttu-id="0c80a-154">Określa wersję klucza.</span><span class="sxs-lookup"><span data-stu-id="0c80a-154">Specifies the key version.</span></span>
<span data-ttu-id="0c80a-155">To polecenie cmdlet konstruuje nazwę FQDN klucza na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, nazwy klucza i wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="0c80a-155">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="0c80a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c80a-156">CommonParameters</span></span>
<span data-ttu-id="0c80a-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c80a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c80a-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c80a-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c80a-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c80a-159">INPUTS</span></span>

### <span data-ttu-id="0c80a-160">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0c80a-160">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0c80a-161">System.String</span><span class="sxs-lookup"><span data-stu-id="0c80a-161">System.String</span></span>

## <span data-ttu-id="0c80a-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c80a-162">OUTPUTS</span></span>

### <span data-ttu-id="0c80a-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0c80a-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="0c80a-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c80a-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="0c80a-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0c80a-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="0c80a-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c80a-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="0c80a-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0c80a-167">NOTES</span></span>

## <span data-ttu-id="0c80a-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c80a-168">RELATED LINKS</span></span>

[<span data-ttu-id="0c80a-169">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c80a-169">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="0c80a-170">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c80a-170">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="0c80a-171">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="0c80a-171">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)


