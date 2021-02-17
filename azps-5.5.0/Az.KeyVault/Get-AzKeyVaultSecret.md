---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: 6824777d5df0f06705f4c10c4af248f1f8e8714a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243403"
---
# <span data-ttu-id="a7dfa-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a7dfa-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="a7dfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="a7dfa-103">Staje się tajemnicą w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="a7dfa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a7dfa-104">SYNTAX</span></span>

### <span data-ttu-id="a7dfa-105">ByVaultName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="a7dfa-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7dfa-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="a7dfa-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7dfa-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="a7dfa-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7dfa-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="a7dfa-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7dfa-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="a7dfa-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7dfa-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="a7dfa-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7dfa-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="a7dfa-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7dfa-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="a7dfa-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7dfa-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="a7dfa-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7dfa-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="a7dfa-114">DESCRIPTION</span></span>
<span data-ttu-id="a7dfa-115">Polecenie **cmdlet Get-AzKeyVaultSecret** staje się tajemnicą w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="a7dfa-116">To polecenie cmdlet uzyskuje określoną tajemnicę lub wszystkie tajemnice w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="a7dfa-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a7dfa-117">EXAMPLES</span></span>

### <span data-ttu-id="a7dfa-118">Przykład 1. Uzyskiwanie wszystkich bieżących wersji wszystkich sekretów w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="a7dfa-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
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

<span data-ttu-id="a7dfa-119">To polecenie pobiera bieżące wersje wszystkich sekretów magazynu kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="a7dfa-120">Przykład 2. Uzyskiwanie wszystkich wersji o określonym kluczu tajnym</span><span class="sxs-lookup"><span data-stu-id="a7dfa-120">Example 2: Get all versions of a specific secret</span></span>
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

<span data-ttu-id="a7dfa-121">To polecenie pobiera wszystkie wersje klucza tajnego o nazwie secret1 w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="a7dfa-122">Przykład 3. Uzyskiwanie bieżącej wersji określonego tajnych</span><span class="sxs-lookup"><span data-stu-id="a7dfa-122">Example 3: Get the current version of a specific secret</span></span>
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

<span data-ttu-id="a7dfa-123">To polecenie pobiera bieżącą wersję klucza tajnego o nazwie secret1 w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="a7dfa-124">Przykład 4. Uzyskiwanie konkretnej wersji określonego tajnych</span><span class="sxs-lookup"><span data-stu-id="a7dfa-124">Example 4: Get a specific version of a specific secret</span></span>
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

<span data-ttu-id="a7dfa-125">To polecenie pobiera określoną wersję klucza tajnego o nazwie secret1 w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="a7dfa-126">Przykład 5. Uzyskiwanie wartości zwykłego tekstu bieżącej wersji określonej tajemnicy</span><span class="sxs-lookup"><span data-stu-id="a7dfa-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secretText = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -AsPlainText
```

<span data-ttu-id="a7dfa-127">Polecenie cmdlet zwraca klucz tajny jako ciąg po `-AsPlainText` zastosowaniu.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-127">The cmdlet returns the secret as a string when `-AsPlainText` is applied.</span></span>

### <span data-ttu-id="a7dfa-128">Przykład 6. Poznaj wszystkie tajemnice, które zostały usunięte, ale nie zostały usunięte dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="a7dfa-129">To polecenie pobiera wszystkie tajemnice, które zostały wcześniej usunięte, ale nie usunięte, w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="a7dfa-130">Przykład 7. Pobiera tajny klucz ITSecret, który został usunięty, ale nie przeczyszczony dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="a7dfa-131">To polecenie pobiera "tajny1", który został wcześniej usunięty, ale nie przeczyszczony, w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="a7dfa-132">To polecenie zwróci metadane, takie jak data usunięcia i zaplanowana data usunięcia tej usuniętej tajemnicy.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="a7dfa-133">Przykład 8. Uzyskiwanie wszystkich bieżących wersji wszystkich sekretów magazynu kluczy przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="a7dfa-133">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
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

<span data-ttu-id="a7dfa-134">To polecenie pobiera bieżące wersje wszystkich sekretów magazynu kluczy o nazwie Contoso, które zaczynają się od "tajnych".</span><span class="sxs-lookup"><span data-stu-id="a7dfa-134">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="a7dfa-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7dfa-135">PARAMETERS</span></span>

### <span data-ttu-id="a7dfa-136">-AsPlainText</span><span class="sxs-lookup"><span data-stu-id="a7dfa-136">-AsPlainText</span></span>
<span data-ttu-id="a7dfa-137">Po jej skonfigurowaniu polecenie cmdlet przekonwertuje ciąg tajny w postaci bezpiecznego ciągu na odszyfrowany ciąg zwykłego tekstu jako wynik.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-137">When set, the cmdlet will convert secret in secure string to the decrypted plaintext string as output.</span></span>

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

### <span data-ttu-id="a7dfa-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7dfa-138">-DefaultProfile</span></span>
<span data-ttu-id="a7dfa-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a7dfa-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7dfa-140">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="a7dfa-140">-IncludeVersions</span></span>
<span data-ttu-id="a7dfa-141">Wskazuje, że to polecenie cmdlet uzyskuje wszystkie wersje w kluczu tajnym.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-141">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="a7dfa-142">Bieżąca wersja informacji tajnych jest pierwszą na liście.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-142">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="a7dfa-143">Jeśli określisz ten parametr, musisz również określić parametry *Name (Nazwa) i* *VaultName (Nazwa magazynu).*</span><span class="sxs-lookup"><span data-stu-id="a7dfa-143">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="a7dfa-144">Jeśli nie określisz *parametru IncludeVersions,* to polecenie cmdlet pobiera bieżącą wersję tajnych z określoną *nazwą.*</span><span class="sxs-lookup"><span data-stu-id="a7dfa-144">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

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

### <span data-ttu-id="a7dfa-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7dfa-145">-InputObject</span></span>
<span data-ttu-id="a7dfa-146">Obiekt KeyVault.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-146">KeyVault Object.</span></span>

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

### <span data-ttu-id="a7dfa-147">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a7dfa-147">-InRemovedState</span></span>
<span data-ttu-id="a7dfa-148">Określa, czy dane wyjściowe mają być pokazywane usuniętym wcześniej tajemnicom</span><span class="sxs-lookup"><span data-stu-id="a7dfa-148">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="a7dfa-149">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a7dfa-149">-Name</span></span>
<span data-ttu-id="a7dfa-150">Określa nazwę sekretu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-150">Specifies the name of the secret to get.</span></span>

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

### <span data-ttu-id="a7dfa-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7dfa-151">-ResourceId</span></span>
<span data-ttu-id="a7dfa-152">Identyfikator zasobu KeyVault.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-152">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="a7dfa-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a7dfa-153">-VaultName</span></span>
<span data-ttu-id="a7dfa-154">Określa nazwę magazynu kluczy, do którego należy klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-154">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="a7dfa-155">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy, która jest określana przez ten parametr i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-155">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="a7dfa-156">— Wersja</span><span class="sxs-lookup"><span data-stu-id="a7dfa-156">-Version</span></span>
<span data-ttu-id="a7dfa-157">Określa wersję tajną.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-157">Specifies the secret version.</span></span>
<span data-ttu-id="a7dfa-158">To polecenie cmdlet konstruuje nazwę FQDN klucza tajnego na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, nazwy tajnej i wersji tajnej.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-158">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="a7dfa-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7dfa-159">CommonParameters</span></span>
<span data-ttu-id="a7dfa-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7dfa-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7dfa-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7dfa-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7dfa-162">INPUTS</span></span>

### <span data-ttu-id="a7dfa-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a7dfa-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a7dfa-164">System.String</span><span class="sxs-lookup"><span data-stu-id="a7dfa-164">System.String</span></span>

## <span data-ttu-id="a7dfa-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7dfa-165">OUTPUTS</span></span>

### <span data-ttu-id="a7dfa-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a7dfa-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="a7dfa-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a7dfa-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="a7dfa-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a7dfa-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="a7dfa-169">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a7dfa-169">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="a7dfa-170">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a7dfa-170">NOTES</span></span>

## <span data-ttu-id="a7dfa-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7dfa-171">RELATED LINKS</span></span>

[<span data-ttu-id="a7dfa-172">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a7dfa-172">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="a7dfa-173">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="a7dfa-173">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="a7dfa-174">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a7dfa-174">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

