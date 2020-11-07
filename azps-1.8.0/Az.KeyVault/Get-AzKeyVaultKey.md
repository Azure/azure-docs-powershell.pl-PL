---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 21d2f6efa039dbd9b229562fcefd53c715f400fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867976"
---
# <span data-ttu-id="633b6-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="633b6-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="633b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="633b6-102">SYNOPSIS</span></span>
<span data-ttu-id="633b6-103">Pobiera klucze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="633b6-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="633b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="633b6-104">SYNTAX</span></span>

### <span data-ttu-id="633b6-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="633b6-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="633b6-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="633b6-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="633b6-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="633b6-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="633b6-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="633b6-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="633b6-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="633b6-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="633b6-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="633b6-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="633b6-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="633b6-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="633b6-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="633b6-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="633b6-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="633b6-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="633b6-114">Opis</span><span class="sxs-lookup"><span data-stu-id="633b6-114">DESCRIPTION</span></span>
<span data-ttu-id="633b6-115">Polecenie cmdlet **Get-AzKeyVaultKey** pobiera klucze magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="633b6-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="633b6-116">To polecenie cmdlet umożliwia pobieranie określonego pakietu **Microsoft. Azure. Commands. Key. MODELES** lub lista wszystkich obiektów **pakietu** kluczy w magazynie kluczy lub według wersji.</span><span class="sxs-lookup"><span data-stu-id="633b6-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="633b6-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="633b6-117">EXAMPLES</span></span>

### <span data-ttu-id="633b6-118">Przykład 1. pobieranie wszystkich kluczy w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="633b6-118">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="633b6-119">To polecenie pobiera wszystkie klucze w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="633b6-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="633b6-120">Przykład 2: uzyskiwanie bieżącej wersji klucza</span><span class="sxs-lookup"><span data-stu-id="633b6-120">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="633b6-121">To polecenie pobiera aktualną wersję klucza o nazwie TEST1 w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="633b6-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="633b6-122">Przykład 3: pobieranie wszystkich wersji klucza</span><span class="sxs-lookup"><span data-stu-id="633b6-122">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="633b6-123">To polecenie pobiera wszystkie wersje klucza o nazwie ITPfx w kluczu vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="633b6-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="633b6-124">Przykład 4: uzyskiwanie określonej wersji klucza</span><span class="sxs-lookup"><span data-stu-id="633b6-124">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="633b6-125">To polecenie pobiera określoną wersję klucza o nazwie TEST1 w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="633b6-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="633b6-126">Po uruchomieniu tego polecenia możesz sprawdzić różne właściwości klucza, przechodząc do obiektu $Key.</span><span class="sxs-lookup"><span data-stu-id="633b6-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="633b6-127">Przykład 5: Uzyskaj wszystkie klucze, które zostały usunięte, ale nie zostały oczyszczone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="633b6-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="633b6-128">To polecenie pobiera wszystkie klucze, które zostały wcześniej usunięte, ale nie zostały oczyszczone w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="633b6-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="633b6-129">Przykład 6: Pobiera klucze ITPfx, które zostały usunięte, ale nie zostały oczyszczone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="633b6-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="633b6-130">To polecenie pobiera klucze test3, które zostały wcześniej usunięte, ale nie zostały oczyszczone w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="633b6-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="633b6-131">To polecenie zwróci metadane, takie jak Data usunięcia, oraz zaplanowaną datę przeczyszczania tego usuniętego klucza.</span><span class="sxs-lookup"><span data-stu-id="633b6-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="633b6-132">Przykład 7: uzyskiwanie wszystkich kluczy w magazynie kluczy przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="633b6-132">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="633b6-133">To polecenie pobiera wszystkie klucze w magazynie kluczy o nazwie contoso, które zaczynają się od tekstu "test".</span><span class="sxs-lookup"><span data-stu-id="633b6-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

## <span data-ttu-id="633b6-134">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="633b6-134">PARAMETERS</span></span>

### <span data-ttu-id="633b6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="633b6-135">-DefaultProfile</span></span>
<span data-ttu-id="633b6-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="633b6-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="633b6-137">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="633b6-137">-IncludeVersions</span></span>
<span data-ttu-id="633b6-138">Wskazuje, że to polecenie cmdlet pobiera wszystkie wersje klucza.</span><span class="sxs-lookup"><span data-stu-id="633b6-138">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="633b6-139">Bieżąca wersja klucza to pierwsza z nich na liście.</span><span class="sxs-lookup"><span data-stu-id="633b6-139">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="633b6-140">W przypadku określenia tego parametru należy również określić *nazwę* i parametry *magazynu* .</span><span class="sxs-lookup"><span data-stu-id="633b6-140">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="633b6-141">Jeśli nie określisz parametru *IncludeVersions* , to polecenie cmdlet pobiera bieżącą wersję klucza o określonej *nazwie*.</span><span class="sxs-lookup"><span data-stu-id="633b6-141">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

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

### <span data-ttu-id="633b6-142">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="633b6-142">-InputObject</span></span>
<span data-ttu-id="633b6-143">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="633b6-143">KeyVault object.</span></span>

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

### <span data-ttu-id="633b6-144">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="633b6-144">-InRemovedState</span></span>
<span data-ttu-id="633b6-145">Określa, czy w wyniku mają być pokazywane uprzednio usunięte klucze.</span><span class="sxs-lookup"><span data-stu-id="633b6-145">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="633b6-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="633b6-146">-Name</span></span>
<span data-ttu-id="633b6-147">Określa nazwę pakietu kluczy, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="633b6-147">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="633b6-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="633b6-148">-ResourceId</span></span>
<span data-ttu-id="633b6-149">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="633b6-149">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="633b6-150">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="633b6-150">-VaultName</span></span>
<span data-ttu-id="633b6-151">Określa nazwę magazynu kluczy, z którego to polecenie cmdlet pobiera klucze.</span><span class="sxs-lookup"><span data-stu-id="633b6-151">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="633b6-152">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy, jaką ten parametr określa i wybrane środowisko.</span><span class="sxs-lookup"><span data-stu-id="633b6-152">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="633b6-153">-Version</span><span class="sxs-lookup"><span data-stu-id="633b6-153">-Version</span></span>
<span data-ttu-id="633b6-154">Określa wersję klucza.</span><span class="sxs-lookup"><span data-stu-id="633b6-154">Specifies the key version.</span></span>
<span data-ttu-id="633b6-155">To polecenie cmdlet konstruuje nazwę FQDN klucza na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, nazwy klucza i wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="633b6-155">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="633b6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="633b6-156">CommonParameters</span></span>
<span data-ttu-id="633b6-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="633b6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="633b6-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="633b6-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="633b6-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="633b6-159">INPUTS</span></span>

### <span data-ttu-id="633b6-160">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="633b6-160">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="633b6-161">System. String</span><span class="sxs-lookup"><span data-stu-id="633b6-161">System.String</span></span>

## <span data-ttu-id="633b6-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="633b6-162">OUTPUTS</span></span>

### <span data-ttu-id="633b6-163">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="633b6-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="633b6-164">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="633b6-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="633b6-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="633b6-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="633b6-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="633b6-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="633b6-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="633b6-167">NOTES</span></span>

## <span data-ttu-id="633b6-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="633b6-168">RELATED LINKS</span></span>

[<span data-ttu-id="633b6-169">Dodaj-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="633b6-169">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="633b6-170">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="633b6-170">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="633b6-171">Cofanie — AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="633b6-171">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="633b6-172">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="633b6-172">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

