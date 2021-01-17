---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: 18b87f6a83f335958e9c10e392d859ae307e9e87
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361697"
---
# <span data-ttu-id="14df5-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="14df5-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="14df5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14df5-102">SYNOPSIS</span></span>
<span data-ttu-id="14df5-103">Pobiera klucze tajne w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="14df5-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="14df5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14df5-104">SYNTAX</span></span>

### <span data-ttu-id="14df5-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="14df5-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14df5-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="14df5-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14df5-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="14df5-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14df5-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="14df5-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14df5-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="14df5-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14df5-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="14df5-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14df5-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="14df5-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14df5-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="14df5-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14df5-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="14df5-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14df5-114">Opis</span><span class="sxs-lookup"><span data-stu-id="14df5-114">DESCRIPTION</span></span>
<span data-ttu-id="14df5-115">Polecenie cmdlet **Get-AzKeyVaultSecret** pobiera klucze tajne w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="14df5-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="14df5-116">To polecenie cmdlet umożliwia pobieranie określonego hasła lub wszystkich kluczy tajnych w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="14df5-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="14df5-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14df5-117">EXAMPLES</span></span>

### <span data-ttu-id="14df5-118">Przykład 1. Pobierz wszystkie bieżące wersje wszystkich kluczy tajnych w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="14df5-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
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

<span data-ttu-id="14df5-119">To polecenie pobiera bieżące wersje wszystkich kluczy tajnych w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="14df5-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="14df5-120">Przykład 2: pobieranie wszystkich wersji określonego hasła</span><span class="sxs-lookup"><span data-stu-id="14df5-120">Example 2: Get all versions of a specific secret</span></span>
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

<span data-ttu-id="14df5-121">To polecenie pobiera wszystkie wersje sekretu o nazwie secret1 w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="14df5-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="14df5-122">Przykład 3: uzyskiwanie bieżącej wersji określonego hasła</span><span class="sxs-lookup"><span data-stu-id="14df5-122">Example 3: Get the current version of a specific secret</span></span>
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

<span data-ttu-id="14df5-123">To polecenie pobiera aktualną wersję sekretu o nazwie secret1 w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="14df5-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="14df5-124">Przykład 4: uzyskiwanie określonej wersji określonego hasła</span><span class="sxs-lookup"><span data-stu-id="14df5-124">Example 4: Get a specific version of a specific secret</span></span>
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

<span data-ttu-id="14df5-125">To polecenie pobiera określoną wersję sekretu o nazwie secret1 w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="14df5-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="14df5-126">Przykład 5: uzyskiwanie wartości zwykłego tekstu bieżącej wersji określonego klucza tajnego</span><span class="sxs-lookup"><span data-stu-id="14df5-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'

# Method 1: requires PowerShell >= 7.0
PS C:\> $secretInPlainText = $secret.SecretValue | ConvertFrom-SecureString -AsPlainText

# Method 2: works on older PowerShell versions
PS C:\> $secretValueText = '';
PS C:\> $ssPtr = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue)
PS C:\> try {
    $secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR($ssPtr)
} finally {
    [System.Runtime.InteropServices.Marshal]::ZeroFreeBSTR($ssPtr)
}

# Method 3: works in ConstrainedLanguage mode
$secretInPlainText = [pscredential]::new("DoesntMatter", $secret.SecretValue).GetNetworkCredential().Password
```

<span data-ttu-id="14df5-127">Te polecenia uzyskują aktualną wersję sekretu o nazwie ITSecret, a następnie wyświetlają wartość zwykłego tekstu tego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="14df5-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

<span data-ttu-id="14df5-128">(Uwaga: Użyj metody 3, jeśli pracujesz w [trybie ConstrainedLanguage](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_language_modes?view=powershell-7.1#constrained-language-constrained-language)programu PowerShell, na przykład na bezpiecznych i uprzywilejowanych stacjach roboczych dostępu).</span><span class="sxs-lookup"><span data-stu-id="14df5-128">(Note: use method 3 if you are working in PowerShell [ConstrainedLanguage mode](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_language_modes?view=powershell-7.1#constrained-language-constrained-language), for example, on secure/privileged access workstations.)</span></span>

### <span data-ttu-id="14df5-129">Przykład 6: pobieranie wszystkich kluczy tajnych, które zostały usunięte, ale nie zostały oczyszczone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="14df5-129">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="14df5-130">To polecenie pobiera wszystkie klucze tajne, które zostały wcześniej usunięte, ale nie zostały oczyszczone w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="14df5-130">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="14df5-131">Przykład 7: Pobiera tajne ITSecret, który został usunięty, ale nie został odczyszczony dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="14df5-131">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="14df5-132">To polecenie pobiera klucz tajny "secret1", który został wcześniej usunięty, ale nie przeczyszczony, w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="14df5-132">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="14df5-133">To polecenie zwróci metadane, takie jak Data usunięcia, oraz zaplanowaną datę przeczyszczania tego usuniętego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="14df5-133">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="14df5-134">Przykład 8: pobieranie wszystkich bieżących wersji wszystkich kluczy tajnych w magazynie kluczy przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="14df5-134">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
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

<span data-ttu-id="14df5-135">To polecenie pobiera bieżące wersje wszystkich kluczy tajnych w magazynie kluczy o nazwie contoso, które zaczynają się od "tajemnicy".</span><span class="sxs-lookup"><span data-stu-id="14df5-135">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="14df5-136">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14df5-136">PARAMETERS</span></span>

### <span data-ttu-id="14df5-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14df5-137">-DefaultProfile</span></span>
<span data-ttu-id="14df5-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="14df5-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14df5-139">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="14df5-139">-IncludeVersions</span></span>
<span data-ttu-id="14df5-140">Wskazuje, że to polecenie cmdlet pobiera wszystkie wersje klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="14df5-140">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="14df5-141">Bieżąca wersja sekretu to pierwsza z nich na liście.</span><span class="sxs-lookup"><span data-stu-id="14df5-141">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="14df5-142">W przypadku określenia tego parametru należy również określić *nazwę* i parametry *magazynu* .</span><span class="sxs-lookup"><span data-stu-id="14df5-142">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="14df5-143">Jeśli nie określisz parametru *IncludeVersions* , to polecenie cmdlet pobiera aktualną wersję klucza tajnego o określonej *nazwie*.</span><span class="sxs-lookup"><span data-stu-id="14df5-143">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

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

### <span data-ttu-id="14df5-144">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="14df5-144">-InputObject</span></span>
<span data-ttu-id="14df5-145">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="14df5-145">KeyVault Object.</span></span>

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

### <span data-ttu-id="14df5-146">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="14df5-146">-InRemovedState</span></span>
<span data-ttu-id="14df5-147">Określa, czy mają być pokazywane uprzednio usunięte klucze tajne w danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="14df5-147">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="14df5-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="14df5-148">-Name</span></span>
<span data-ttu-id="14df5-149">Określa nazwę klucza tajnego do pobrania.</span><span class="sxs-lookup"><span data-stu-id="14df5-149">Specifies the name of the secret to get.</span></span>

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

### <span data-ttu-id="14df5-150">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14df5-150">-ResourceId</span></span>
<span data-ttu-id="14df5-151">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="14df5-151">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="14df5-152">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="14df5-152">-VaultName</span></span>
<span data-ttu-id="14df5-153">Określa nazwę magazynu kluczy, do którego należy odpowiedni klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="14df5-153">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="14df5-154">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="14df5-154">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="14df5-155">-Version</span><span class="sxs-lookup"><span data-stu-id="14df5-155">-Version</span></span>
<span data-ttu-id="14df5-156">Określa wersję tajną.</span><span class="sxs-lookup"><span data-stu-id="14df5-156">Specifies the secret version.</span></span>
<span data-ttu-id="14df5-157">To polecenie cmdlet konstruuje nazwę FQDN wpisu tajnego na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, tajnej nazwy i tajnej wersji.</span><span class="sxs-lookup"><span data-stu-id="14df5-157">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="14df5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14df5-158">CommonParameters</span></span>
<span data-ttu-id="14df5-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14df5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14df5-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14df5-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14df5-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14df5-161">INPUTS</span></span>

### <span data-ttu-id="14df5-162">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="14df5-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="14df5-163">System. String</span><span class="sxs-lookup"><span data-stu-id="14df5-163">System.String</span></span>

## <span data-ttu-id="14df5-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14df5-164">OUTPUTS</span></span>

### <span data-ttu-id="14df5-165">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="14df5-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="14df5-166">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="14df5-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="14df5-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="14df5-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="14df5-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="14df5-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="14df5-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14df5-169">NOTES</span></span>

## <span data-ttu-id="14df5-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14df5-170">RELATED LINKS</span></span>

[<span data-ttu-id="14df5-171">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="14df5-171">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="14df5-172">Cofanie — AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="14df5-172">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="14df5-173">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="14df5-173">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

