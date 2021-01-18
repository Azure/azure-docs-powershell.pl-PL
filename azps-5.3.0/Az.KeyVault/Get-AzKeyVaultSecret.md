---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: 6824777d5df0f06705f4c10c4af248f1f8e8714a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500922"
---
# <span data-ttu-id="1eb17-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1eb17-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="1eb17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1eb17-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb17-103">Pobiera klucze tajne w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="1eb17-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="1eb17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1eb17-104">SYNTAX</span></span>

### <span data-ttu-id="1eb17-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1eb17-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eb17-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="1eb17-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eb17-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="1eb17-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eb17-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="1eb17-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eb17-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="1eb17-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eb17-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="1eb17-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eb17-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="1eb17-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eb17-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="1eb17-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eb17-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="1eb17-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1eb17-114">Opis</span><span class="sxs-lookup"><span data-stu-id="1eb17-114">DESCRIPTION</span></span>
<span data-ttu-id="1eb17-115">Polecenie cmdlet **Get-AzKeyVaultSecret** pobiera klucze tajne w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="1eb17-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="1eb17-116">To polecenie cmdlet umożliwia pobieranie określonego hasła lub wszystkich kluczy tajnych w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="1eb17-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="1eb17-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1eb17-117">EXAMPLES</span></span>

### <span data-ttu-id="1eb17-118">Przykład 1. Pobierz wszystkie bieżące wersje wszystkich kluczy tajnych w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="1eb17-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso'

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="1eb17-119">To polecenie pobiera bieżące wersje wszystkich kluczy tajnych w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="1eb17-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="1eb17-120">Przykład 2: pobieranie wszystkich wersji określonego hasła</span><span class="sxs-lookup"><span data-stu-id="1eb17-120">Example 2: Get all versions of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -IncludeVersions

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="1eb17-121">To polecenie pobiera wszystkie wersje sekretu o nazwie secret1 w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="1eb17-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="1eb17-122">Przykład 3: uzyskiwanie bieżącej wersji określonego hasła</span><span class="sxs-lookup"><span data-stu-id="1eb17-122">Example 3: Get the current version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1'

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="1eb17-123">To polecenie pobiera aktualną wersję sekretu o nazwie secret1 w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="1eb17-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="1eb17-124">Przykład 4: uzyskiwanie określonej wersji określonego hasła</span><span class="sxs-lookup"><span data-stu-id="1eb17-124">Example 4: Get a specific version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -Version '5d1a74ba2c454439886fb8509b6cab3c'

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="1eb17-125">To polecenie pobiera określoną wersję sekretu o nazwie secret1 w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="1eb17-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="1eb17-126">Przykład 5: uzyskiwanie wartości zwykłego tekstu bieżącej wersji określonego klucza tajnego</span><span class="sxs-lookup"><span data-stu-id="1eb17-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secretText = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -AsPlainText
```

<span data-ttu-id="1eb17-127">Polecenie cmdlet zwraca wartość klucza tajnego w przypadku `-AsPlainText` zastosowania ciągu.</span><span class="sxs-lookup"><span data-stu-id="1eb17-127">The cmdlet returns the secret as a string when `-AsPlainText` is applied.</span></span>

### <span data-ttu-id="1eb17-128">Przykład 6: pobieranie wszystkich kluczy tajnych, które zostały usunięte, ale nie zostały oczyszczone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1eb17-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Id                   : https://contoso.vault.azure.net:443/secrets/secret1
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :

Vault Name           : contoso
Name                 : secret2
Id                   : https://contoso.vault.azure.net:443/secrets/secret2
Deleted Date         : 5/7/2018 7:56:34 PM
Scheduled Purge Date : 8/5/2018 7:56:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/6/2018 8:39:15 PM
Updated              : 4/6/2018 10:11:24 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="1eb17-129">To polecenie pobiera wszystkie klucze tajne, które zostały wcześniej usunięte, ale nie zostały oczyszczone w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="1eb17-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="1eb17-130">Przykład 7: Pobiera tajne ITSecret, który został usunięty, ale nie został odczyszczony dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1eb17-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Version              : 689d23346e9c42a2a64f4e3d75094dcc
Id                   : https://contoso.vault.azure.net:443/secrets/secret1/689d23346e9c42a2a64f4e3d75094dcc
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="1eb17-131">To polecenie pobiera klucz tajny "secret1", który został wcześniej usunięty, ale nie przeczyszczony, w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="1eb17-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="1eb17-132">To polecenie zwróci metadane, takie jak Data usunięcia, oraz zaplanowaną datę przeczyszczania tego usuniętego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="1eb17-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="1eb17-133">Przykład 8: pobieranie wszystkich bieżących wersji wszystkich kluczy tajnych w magazynie kluczy przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="1eb17-133">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name "secret*"

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="1eb17-134">To polecenie pobiera bieżące wersje wszystkich kluczy tajnych w magazynie kluczy o nazwie contoso, które zaczynają się od "tajemnicy".</span><span class="sxs-lookup"><span data-stu-id="1eb17-134">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="1eb17-135">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1eb17-135">PARAMETERS</span></span>

### <span data-ttu-id="1eb17-136">-AsPlainText</span><span class="sxs-lookup"><span data-stu-id="1eb17-136">-AsPlainText</span></span>
<span data-ttu-id="1eb17-137">Po ustawieniu polecenie cmdlet konwertuje klucz tajny w bezpiecznym ciągu na ciąg w postaci ciągu tekstowego.</span><span class="sxs-lookup"><span data-stu-id="1eb17-137">When set, the cmdlet will convert secret in secure string to the decrypted plaintext string as output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, BySecretName, ByInputObjectVaultName, ByInputObjectSecretName, ByResourceIdVaultName, ByResourceIdSecretName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb17-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb17-138">-DefaultProfile</span></span>
<span data-ttu-id="1eb17-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1eb17-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1eb17-140">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="1eb17-140">-IncludeVersions</span></span>
<span data-ttu-id="1eb17-141">Wskazuje, że to polecenie cmdlet pobiera wszystkie wersje klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="1eb17-141">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="1eb17-142">Bieżąca wersja sekretu to pierwsza z nich na liście.</span><span class="sxs-lookup"><span data-stu-id="1eb17-142">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="1eb17-143">W przypadku określenia tego parametru należy również określić *nazwę* i parametry *magazynu* .</span><span class="sxs-lookup"><span data-stu-id="1eb17-143">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="1eb17-144">Jeśli nie określisz parametru *IncludeVersions* , to polecenie cmdlet pobiera aktualną wersję klucza tajnego o określonej *nazwie*.</span><span class="sxs-lookup"><span data-stu-id="1eb17-144">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions, ByResourceIdSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb17-145">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1eb17-145">-InputObject</span></span>
<span data-ttu-id="1eb17-146">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="1eb17-146">KeyVault Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1eb17-147">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="1eb17-147">-InRemovedState</span></span>
<span data-ttu-id="1eb17-148">Określa, czy mają być pokazywane uprzednio usunięte klucze tajne w danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1eb17-148">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="1eb17-149">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1eb17-149">-Name</span></span>
<span data-ttu-id="1eb17-150">Określa nazwę klucza tajnego do pobrania.</span><span class="sxs-lookup"><span data-stu-id="1eb17-150">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="1eb17-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1eb17-151">-ResourceId</span></span>
<span data-ttu-id="1eb17-152">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="1eb17-152">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eb17-153">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="1eb17-153">-VaultName</span></span>
<span data-ttu-id="1eb17-154">Określa nazwę magazynu kluczy, do którego należy odpowiedni klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="1eb17-154">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="1eb17-155">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="1eb17-155">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb17-156">-Version</span><span class="sxs-lookup"><span data-stu-id="1eb17-156">-Version</span></span>
<span data-ttu-id="1eb17-157">Określa wersję tajną.</span><span class="sxs-lookup"><span data-stu-id="1eb17-157">Specifies the secret version.</span></span>
<span data-ttu-id="1eb17-158">To polecenie cmdlet konstruuje nazwę FQDN wpisu tajnego na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, tajnej nazwy i tajnej wersji.</span><span class="sxs-lookup"><span data-stu-id="1eb17-158">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName, ByInputObjectSecretName, ByResourceIdSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb17-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb17-159">CommonParameters</span></span>
<span data-ttu-id="1eb17-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb17-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb17-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1eb17-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb17-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1eb17-162">INPUTS</span></span>

### <span data-ttu-id="1eb17-163">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1eb17-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1eb17-164">System. String</span><span class="sxs-lookup"><span data-stu-id="1eb17-164">System.String</span></span>

## <span data-ttu-id="1eb17-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1eb17-165">OUTPUTS</span></span>

### <span data-ttu-id="1eb17-166">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1eb17-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="1eb17-167">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1eb17-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="1eb17-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1eb17-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="1eb17-169">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1eb17-169">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="1eb17-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1eb17-170">NOTES</span></span>

## <span data-ttu-id="1eb17-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1eb17-171">RELATED LINKS</span></span>

[<span data-ttu-id="1eb17-172">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1eb17-172">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="1eb17-173">Cofanie — AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="1eb17-173">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="1eb17-174">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1eb17-174">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

