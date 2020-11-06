---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://go.microsoft.com/fwlink/?LinkId=690298
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: f6fca9ec6b5f5696cbaa1fb82942e5aa6dfadf80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527554"
---
# <span data-ttu-id="d6cb6-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d6cb6-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="d6cb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="d6cb6-103">Pobiera klucze tajne w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6cb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6cb6-104">SYNTAX</span></span>

### <span data-ttu-id="d6cb6-105">ByVaultName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d6cb6-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6cb6-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="d6cb6-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6cb6-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="d6cb6-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6cb6-108">ByDeletedSecrets</span><span class="sxs-lookup"><span data-stu-id="d6cb6-108">ByDeletedSecrets</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6cb6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d6cb6-109">DESCRIPTION</span></span>
<span data-ttu-id="d6cb6-110">Polecenie cmdlet **Get-AzureKeyVaultSecret** pobiera klucze tajne w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-110">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="d6cb6-111">To polecenie cmdlet umożliwia pobieranie określonego hasła lub wszystkich kluczy tajnych w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-111">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="d6cb6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6cb6-112">EXAMPLES</span></span>

### <span data-ttu-id="d6cb6-113">Przykład 1. Pobierz wszystkie bieżące wersje wszystkich kluczy tajnych w magazynie kluczy</span><span class="sxs-lookup"><span data-stu-id="d6cb6-113">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="d6cb6-114">To polecenie pobiera bieżące wersje wszystkich kluczy tajnych w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-114">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="d6cb6-115">Przykład 2: pobieranie wszystkich wersji określonego hasła</span><span class="sxs-lookup"><span data-stu-id="d6cb6-115">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="d6cb6-116">To polecenie pobiera wszystkie wersje sekretu o nazwie ITSecret w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-116">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="d6cb6-117">Przykład 3: uzyskiwanie bieżącej wersji określonego hasła</span><span class="sxs-lookup"><span data-stu-id="d6cb6-117">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="d6cb6-118">To polecenie pobiera aktualną wersję sekretu o nazwie ITSecret w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-118">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="d6cb6-119">Przykład 4: uzyskiwanie określonej wersji określonego hasła</span><span class="sxs-lookup"><span data-stu-id="d6cb6-119">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="d6cb6-120">To polecenie pobiera określoną wersję sekretu o nazwie ITSecret w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-120">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="d6cb6-121">Przykład 5: uzyskiwanie wartości zwykłego tekstu bieżącej wersji określonego klucza tajnego</span><span class="sxs-lookup"><span data-stu-id="d6cb6-121">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="d6cb6-122">Te polecenia uzyskują aktualną wersję sekretu o nazwie ITSecret, a następnie wyświetlają wartość zwykłego tekstu tego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-122">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="d6cb6-123">Przykład 6: pobieranie wszystkich kluczy tajnych, które zostały usunięte, ale nie zostały oczyszczone dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-123">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="d6cb6-124">To polecenie pobiera wszystkie klucze tajne, które zostały wcześniej usunięte, ale nie zostały oczyszczone w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-124">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="d6cb6-125">Przykład 7: Pobiera tajne ITSecret, który został usunięty, ale nie został odczyszczony dla tego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-125">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="d6cb6-126">To polecenie uzyskuje tajne ITSecret, który został wcześniej usunięty, ale nie został przeczyszczony w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-126">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="d6cb6-127">To polecenie zwróci metadane, takie jak Data usunięcia, oraz zaplanowaną datę przeczyszczania tego usuniętego klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-127">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="d6cb6-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6cb6-128">PARAMETERS</span></span>

### <span data-ttu-id="d6cb6-129">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="d6cb6-129">-IncludeVersions</span></span>
<span data-ttu-id="d6cb6-130">Wskazuje, że to polecenie cmdlet pobiera wszystkie wersje klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-130">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="d6cb6-131">Bieżąca wersja sekretu to pierwsza z nich na liście.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-131">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="d6cb6-132">W przypadku określenia tego parametru należy również określić *nazwę* i parametry *magazynu* .</span><span class="sxs-lookup"><span data-stu-id="d6cb6-132">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="d6cb6-133">Jeśli nie określisz parametru *IncludeVersions* , to polecenie cmdlet pobiera aktualną wersję klucza tajnego o określonej *nazwie*.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-133">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cb6-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d6cb6-134">-InRemovedState</span></span>
<span data-ttu-id="d6cb6-135">Określa, czy mają być pokazywane uprzednio usunięte klucze tajne w danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-135">Specifies whether to show the previously deleted secrets in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cb6-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d6cb6-136">-Name</span></span>
<span data-ttu-id="d6cb6-137">Określa nazwę klucza tajnego do pobrania.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-137">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cb6-138">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="d6cb6-138">-VaultName</span></span>
<span data-ttu-id="d6cb6-139">Określa nazwę magazynu kluczy, do którego należy odpowiedni klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-139">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="d6cb6-140">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-140">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cb6-141">-Version</span><span class="sxs-lookup"><span data-stu-id="d6cb6-141">-Version</span></span>
<span data-ttu-id="d6cb6-142">Określa wersję tajną.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-142">Specifies the secret version.</span></span>
<span data-ttu-id="d6cb6-143">To polecenie cmdlet konstruuje nazwę FQDN wpisu tajnego na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, tajnej nazwy i tajnej wersji.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-143">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cb6-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6cb6-144">-DefaultProfile</span></span>
<span data-ttu-id="d6cb6-145">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6cb6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6cb6-146">CommonParameters</span></span>
<span data-ttu-id="d6cb6-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6cb6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6cb6-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6cb6-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6cb6-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6cb6-149">INPUTS</span></span>

### <span data-ttu-id="d6cb6-150">Ciąg</span><span class="sxs-lookup"><span data-stu-id="d6cb6-150">String</span></span>

## <span data-ttu-id="d6cb6-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6cb6-151">OUTPUTS</span></span>

### <span data-ttu-id="d6cb6-152">Lista<Microsoft. Azure. Commands. Data. models. SecretIdentityItem>, Microsoft. Azure. Commands. platforming. model. Secret, list<Microsoft. Azure. Commands. platform. modele. DeletedSecretIdentityItem>, Microsoft. Azure. Commands. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="d6cb6-152">List<Microsoft.Azure.Commands.KeyVault.Models.SecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.Secret, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>

## <span data-ttu-id="d6cb6-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6cb6-153">NOTES</span></span>

## <span data-ttu-id="d6cb6-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6cb6-154">RELATED LINKS</span></span>

[<span data-ttu-id="d6cb6-155">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d6cb6-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="d6cb6-156">Cofanie — AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="d6cb6-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="d6cb6-157">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d6cb6-157">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

