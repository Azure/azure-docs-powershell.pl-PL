---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: da6460bf0a1126a11345336e4d55c300728bbd66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203842"
---
# <span data-ttu-id="94155-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94155-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="94155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94155-102">SYNOPSIS</span></span>
<span data-ttu-id="94155-103">Tworzy klucz w magazynie kluczy lub importuje klucz do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="94155-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="94155-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94155-104">SYNTAX</span></span>

### <span data-ttu-id="94155-105">InteractiveCreate (Default)</span><span class="sxs-lookup"><span data-stu-id="94155-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94155-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="94155-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94155-107">HsmInteractiveCreate</span><span class="sxs-lookup"><span data-stu-id="94155-107">HsmInteractiveCreate</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94155-108">HsmInteractiveImport</span><span class="sxs-lookup"><span data-stu-id="94155-108">HsmInteractiveImport</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94155-109">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="94155-109">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94155-110">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="94155-110">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94155-111">HsmInputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="94155-111">HsmInputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94155-112">HsmInputObjectImport</span><span class="sxs-lookup"><span data-stu-id="94155-112">HsmInputObjectImport</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94155-113">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="94155-113">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94155-114">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="94155-114">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94155-115">HsmResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="94155-115">HsmResourceIdCreate</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94155-116">HsmResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="94155-116">HsmResourceIdImport</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94155-117">OPIS</span><span class="sxs-lookup"><span data-stu-id="94155-117">DESCRIPTION</span></span>
<span data-ttu-id="94155-118">Polecenie **cmdlet Add-AzKeyVaultKey** tworzy klucz w magazynie kluczy w magazynie kluczy platformy Azure lub importuje klucz do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="94155-118">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="94155-119">Użyj tego polecenia cmdlet, aby dodać klucze przy użyciu dowolnej z następujących metod:</span><span class="sxs-lookup"><span data-stu-id="94155-119">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="94155-120">Tworzenie klucza w module zabezpieczeń sprzętu (HSM) w usłudze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="94155-120">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="94155-121">Utwórz klucz w oprogramowaniu w usłudze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="94155-121">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="94155-122">Importowanie klucza z własnego modułu zabezpieczeń sprzętu do hsm w usłudze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="94155-122">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="94155-123">Zaimportuj klucz z pliku pfx na komputerze.</span><span class="sxs-lookup"><span data-stu-id="94155-123">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="94155-124">Importowanie klucza z pliku pfx na komputerze do modułów zabezpieczeń sprzętu (HSM) w usłudze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="94155-124">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="94155-125">W przypadku dowolnej z tych operacji można podać atrybuty klucza lub zaakceptować ustawienia domyślne.</span><span class="sxs-lookup"><span data-stu-id="94155-125">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="94155-126">Jeśli utworzysz lub zaimportujesz klucz o takiej samej nazwie jak istniejący klucz w magazynie kluczy, klucz oryginalny zostanie zaktualizowany o wartości określone dla nowego klucza.</span><span class="sxs-lookup"><span data-stu-id="94155-126">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="94155-127">Aby uzyskać dostęp do poprzednich wartości, można użyć specyficznego dla wersji URI dla tej wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="94155-127">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="94155-128">Aby uzyskać informacje na temat kluczowych wersji i struktury URI, zobacz [Informacje](http://go.microsoft.com/fwlink/?linkid=518560) o kluczach i tajemnicach w dokumentacji interfejsu API REST magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="94155-128">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="94155-129">Uwaga: Aby zaimportować klucz z własnego modułu zabezpieczeń sprzętowych, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku byok) przy użyciu zestawu narzędzi BYOK magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="94155-129">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="94155-130">Aby uzyskać więcej informacji, zobacz [generuj i przesyłaj klucze HSM-Protected dla magazynu](http://go.microsoft.com/fwlink/?LinkId=522252)kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="94155-130">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="94155-131">Najlepszym rozwiązaniem jest, aby po utworzeniu lub zaktualizowaniu klucza utworzyć jego kopię zapasową, używając polecenia cmdlet Backup-AzKeyVaultKey cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94155-131">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="94155-132">Nie ma funkcji przywracania, więc jeśli przypadkowo usuniesz klucz lub usuniesz go, a następnie zmienisz zdanie, nie będzie można go odzyskać, chyba że masz jego kopię zapasową, która będzie można przywrócić.</span><span class="sxs-lookup"><span data-stu-id="94155-132">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="94155-133">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94155-133">EXAMPLES</span></span>

### <span data-ttu-id="94155-134">Przykład 1. Tworzenie klucza</span><span class="sxs-lookup"><span data-stu-id="94155-134">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="94155-135">To polecenie tworzy klucz chroniony oprogramowaniem o nazwie ITSoftware w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="94155-135">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="94155-136">Przykład 2. Tworzenie klucza chronionego przez hsm</span><span class="sxs-lookup"><span data-stu-id="94155-136">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="94155-137">To polecenie tworzy klucz chroniony modułem HSM w magazynie kluczy o nazwie Contoso.</span><span class="sxs-lookup"><span data-stu-id="94155-137">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="94155-138">Przykład 3. Tworzenie klucza z wartościami innymi niż domyślne</span><span class="sxs-lookup"><span data-stu-id="94155-138">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="94155-139">Pierwsze polecenie przechowuje wartości do odszyfrowywania i weryfikowania w $KeyOperations danych.</span><span class="sxs-lookup"><span data-stu-id="94155-139">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="94155-140">Drugie polecenie tworzy obiekt **DateTime** zdefiniowany w czasie UTC przy użyciu polecenia cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="94155-140">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="94155-141">Ten obiekt określa czas za dwa lata.</span><span class="sxs-lookup"><span data-stu-id="94155-141">That object specifies a time two years in the future.</span></span> <span data-ttu-id="94155-142">Polecenie przechowuje datę w $Expires zmienną.</span><span class="sxs-lookup"><span data-stu-id="94155-142">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="94155-143">Aby uzyskać więcej informacji, wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="94155-143">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="94155-144">Trzecie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="94155-144">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="94155-145">Ten obiekt określa bieżący czas UTC.</span><span class="sxs-lookup"><span data-stu-id="94155-145">That object specifies current UTC time.</span></span> <span data-ttu-id="94155-146">Polecenie przechowuje datę w $NotBefore zmienną.</span><span class="sxs-lookup"><span data-stu-id="94155-146">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="94155-147">Ostatnie polecenie tworzy klucz o nazwie ITHsmNonDefault, który jest kluczem chronionym przez HSM.</span><span class="sxs-lookup"><span data-stu-id="94155-147">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="94155-148">To polecenie określa wartości dozwolonych operacji na kluczach przechowywanych $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="94155-148">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="94155-149">Polecenie określa czasy dla parametrów *Wygasa i* *NieBefore* utworzonych w poprzednich poleceniach oraz tagów o wysokim poziomie ważności i dla parametrów IT.</span><span class="sxs-lookup"><span data-stu-id="94155-149">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="94155-150">Nowy klucz zostanie wyłączony.</span><span class="sxs-lookup"><span data-stu-id="94155-150">The new key is disabled.</span></span> <span data-ttu-id="94155-151">Możesz ją włączyć przy użyciu polecenia cmdlet **Set-AzKeyVaultKey.**</span><span class="sxs-lookup"><span data-stu-id="94155-151">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="94155-152">Przykład 4. Importowanie klucza chronionego przez HSM</span><span class="sxs-lookup"><span data-stu-id="94155-152">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="94155-153">To polecenie importuje klucz o nazwie ITByok z lokalizacji, która jest określana przez parametr *KeyFilePath.*</span><span class="sxs-lookup"><span data-stu-id="94155-153">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="94155-154">Importowany klucz jest kluczem chronionym przez hsm.</span><span class="sxs-lookup"><span data-stu-id="94155-154">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="94155-155">Aby zaimportować klucz z własnego modułu zabezpieczeń sprzętowych, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku byok) przy użyciu zestawu narzędzi BYOK magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="94155-155">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="94155-156">Aby uzyskać więcej informacji, zobacz [generuj i przesyłaj klucze HSM-Protected dla magazynu](http://go.microsoft.com/fwlink/?LinkId=522252)kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="94155-156">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="94155-157">Przykład 5. Importowanie klucza chronionego oprogramowaniem</span><span class="sxs-lookup"><span data-stu-id="94155-157">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="94155-158">Pierwsze polecenie konwertuje ciąg na bezpieczny ciąg za pomocą polecenia cmdlet **ConvertTo-SecureString,** a następnie zapisuje ten ciąg w $Password danych.</span><span class="sxs-lookup"><span data-stu-id="94155-158">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="94155-159">Aby uzyskać więcej informacji, wpisz `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="94155-159">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="94155-160">Drugie polecenie tworzy hasło oprogramowania w magazynie kluczy Contoso.</span><span class="sxs-lookup"><span data-stu-id="94155-160">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="94155-161">To polecenie określa lokalizację klucza i hasło przechowywane w programie $Password.</span><span class="sxs-lookup"><span data-stu-id="94155-161">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="94155-162">Przykład 6. Importowanie klucza i przypisywanie atrybutów</span><span class="sxs-lookup"><span data-stu-id="94155-162">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="94155-163">Pierwsze polecenie konwertuje ciąg na bezpieczny ciąg za pomocą polecenia cmdlet **ConvertTo-SecureString,** a następnie zapisuje ten ciąg w $Password danych.</span><span class="sxs-lookup"><span data-stu-id="94155-163">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="94155-164">Drugie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date,** a następnie zapisuje ten obiekt w $Expires danych.</span><span class="sxs-lookup"><span data-stu-id="94155-164">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="94155-165">Trzecie polecenie tworzy zmienną $tags, aby ustawiać tagi o wysokim poziomie ważności i it.</span><span class="sxs-lookup"><span data-stu-id="94155-165">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="94155-166">Ostatnie polecenie importuje klucz jako klucz HSM z określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="94155-166">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="94155-167">To polecenie określa czas wygaśnięcia przechowywany w programie $Expires hasło przechowywane w programie $Password i stosuje tagi przechowywane w $tags.</span><span class="sxs-lookup"><span data-stu-id="94155-167">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="94155-168">Przykład 7. Generowanie klucza programu Exchange (KEK) dla funkcji "bring your own key" (BYOK)</span><span class="sxs-lookup"><span data-stu-id="94155-168">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="94155-169">Generuje klucz (nazywany kluczem programu Exchange ).</span><span class="sxs-lookup"><span data-stu-id="94155-169">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="94155-170">KEK musi być kluczem RSA-HSM, który ma tylko operację klucza importu.</span><span class="sxs-lookup"><span data-stu-id="94155-170">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="94155-171">Tylko wersja SKU magazynu kluczy Premium obsługuje klucze RSA-HSM.</span><span class="sxs-lookup"><span data-stu-id="94155-171">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="94155-172">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="94155-172">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="94155-173">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94155-173">PARAMETERS</span></span>

### <span data-ttu-id="94155-174">-CurveName</span><span class="sxs-lookup"><span data-stu-id="94155-174">-CurveName</span></span>
<span data-ttu-id="94155-175">Określa nazwę krzywej kryptografii krzywej wielokropka. Ta wartość jest prawidłowa, gdy typ_klucza to EC.</span><span class="sxs-lookup"><span data-stu-id="94155-175">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveCreate, InputObjectImport, HsmInputObjectCreate, ResourceIdImport, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94155-176">-DefaultProfile</span></span>
<span data-ttu-id="94155-177">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="94155-177">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94155-178">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="94155-178">-Destination</span></span>
<span data-ttu-id="94155-179">Określa, czy należy dodać klucz jako klucz chroniony oprogramowaniem, czy jako klucz chroniony przez HSM w usłudze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="94155-179">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="94155-180">Prawidłowe wartości to: HSM i Software.</span><span class="sxs-lookup"><span data-stu-id="94155-180">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="94155-181">Uwaga: Aby użyć funkcji HSM jako miejsca docelowego, należy mieć magazyn kluczy obsługujący hsm.</span><span class="sxs-lookup"><span data-stu-id="94155-181">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="94155-182">Aby uzyskać więcej informacji o warstwach usług i możliwościach dla magazynu kluczy platformy Azure, zobacz witrynę internetową Ceny magazynu kluczy [platformy Azure.](http://go.microsoft.com/fwlink/?linkid=512521)</span><span class="sxs-lookup"><span data-stu-id="94155-182">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="94155-183">Ten parametr jest wymagany podczas tworzenia nowego klucza.</span><span class="sxs-lookup"><span data-stu-id="94155-183">This parameter is required when you create a new key.</span></span> <span data-ttu-id="94155-184">W przypadku importowania klucza za pomocą parametru *KeyFilePath* ten parametr jest opcjonalny:</span><span class="sxs-lookup"><span data-stu-id="94155-184">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="94155-185">Jeśli ten parametr nie zostanie określony, a to polecenie cmdlet importuje klucz z rozszerzeniem nazwy pliku byok, importuje ten klucz jako klucz chroniony przez moduł HSM.</span><span class="sxs-lookup"><span data-stu-id="94155-185">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="94155-186">Polecenie cmdlet nie może zaimportować tego klucza jako klucza chronionego oprogramowaniem.</span><span class="sxs-lookup"><span data-stu-id="94155-186">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="94155-187">Jeśli nie określisz tego parametru, a to polecenie cmdlet zaimresuje klucz z rozszerzeniem nazwy pliku pfx, zaimresuje ten klucz jako klucz chroniony oprogramowaniem.</span><span class="sxs-lookup"><span data-stu-id="94155-187">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-188">- Wyłącz</span><span class="sxs-lookup"><span data-stu-id="94155-188">-Disable</span></span>
<span data-ttu-id="94155-189">Wskazuje, że dodajeny klucz jest ustawiony na początkowy stan wyłączenia.</span><span class="sxs-lookup"><span data-stu-id="94155-189">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="94155-190">Próba użycia klucza nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="94155-190">Any attempt to use the key will fail.</span></span> <span data-ttu-id="94155-191">Użyj tego parametru, jeśli zamierzasz włączyć wstępnie klucze później.</span><span class="sxs-lookup"><span data-stu-id="94155-191">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-192">— Wygasa</span><span class="sxs-lookup"><span data-stu-id="94155-192">-Expires</span></span>
<span data-ttu-id="94155-193">Określa czas wygaśnięcia , jako obiekt **DateTime,** klucza, który dodaje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94155-193">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="94155-194">Ten parametr używa uniwersalnego czasu koordynowanej (UTC).</span><span class="sxs-lookup"><span data-stu-id="94155-194">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="94155-195">Aby uzyskać obiekt **DateTime,** użyj polecenia cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="94155-195">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="94155-196">Aby uzyskać więcej informacji, wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="94155-196">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="94155-197">Jeśli nie określisz tego parametru, klucz nie wygaśnie.</span><span class="sxs-lookup"><span data-stu-id="94155-197">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-198">- HsmName</span><span class="sxs-lookup"><span data-stu-id="94155-198">-HsmName</span></span>
<span data-ttu-id="94155-199">Nazwa HSM.</span><span class="sxs-lookup"><span data-stu-id="94155-199">HSM name.</span></span> <span data-ttu-id="94155-200">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="94155-200">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-201">- HsmObject</span><span class="sxs-lookup"><span data-stu-id="94155-201">-HsmObject</span></span>
<span data-ttu-id="94155-202">Obiekt HSM.</span><span class="sxs-lookup"><span data-stu-id="94155-202">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94155-203">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="94155-203">-HsmResourceId</span></span>
<span data-ttu-id="94155-204">Identyfikator zasobu hsm.</span><span class="sxs-lookup"><span data-stu-id="94155-204">Resource ID of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94155-205">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94155-205">-InputObject</span></span>
<span data-ttu-id="94155-206">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="94155-206">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94155-207">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="94155-207">-KeyFilePassword</span></span>
<span data-ttu-id="94155-208">Określa hasło dla zaimportowanego pliku jako obiektu **SecureString.**</span><span class="sxs-lookup"><span data-stu-id="94155-208">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="94155-209">Aby uzyskać obiekt **SecureString,** użyj polecenia cmdlet **ConvertTo-SecureString.**</span><span class="sxs-lookup"><span data-stu-id="94155-209">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="94155-210">Aby uzyskać więcej informacji, wpisz `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="94155-210">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="94155-211">To hasło należy określić, aby zaimportować plik z rozszerzeniem nazwy pliku pfx.</span><span class="sxs-lookup"><span data-stu-id="94155-211">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-212">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="94155-212">-KeyFilePath</span></span>
<span data-ttu-id="94155-213">Określa ścieżkę pliku lokalnego zawierającego klucz materiałów importowanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94155-213">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="94155-214">Prawidłowe rozszerzenia nazw plików to byok i pfx.</span><span class="sxs-lookup"><span data-stu-id="94155-214">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="94155-215">Jeśli plik jest plikiem byok, klucz jest automatycznie chroniony przez moduły HSM po zakończeniu importowania i nie można zastąpić tego ustawienia domyślnego.</span><span class="sxs-lookup"><span data-stu-id="94155-215">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="94155-216">Jeśli plik jest plikiem pfx, klucz jest automatycznie chroniony przez oprogramowanie po zaimportowaniu.</span><span class="sxs-lookup"><span data-stu-id="94155-216">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="94155-217">Aby zastąpić to ustawienie domyślne, należy ustawić dla parametru *Destination* wartość HSM tak, aby klucz był chroniony przez hsm.</span><span class="sxs-lookup"><span data-stu-id="94155-217">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="94155-218">Określenie tego parametru jest *parametrem docelowym* opcjonalnym.</span><span class="sxs-lookup"><span data-stu-id="94155-218">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-219">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="94155-219">-KeyOps</span></span>
<span data-ttu-id="94155-220">Określa tablicę operacji, które można wykonać przy użyciu klucza, który dodaje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94155-220">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="94155-221">Jeśli nie określisz tego parametru, będzie można wykonywać wszystkie operacje.</span><span class="sxs-lookup"><span data-stu-id="94155-221">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="94155-222">Dopuszczalne wartości dla tego parametru to rozdzielona przecinkami lista operacji klucza zgodnie ze specyfikacją klucza sieci [Web JSON (JWK):](http://go.microsoft.com/fwlink/?LinkID=613300)</span><span class="sxs-lookup"><span data-stu-id="94155-222">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="94155-223">szyfrowanie</span><span class="sxs-lookup"><span data-stu-id="94155-223">encrypt</span></span>
- <span data-ttu-id="94155-224">odszyfrowywanie</span><span class="sxs-lookup"><span data-stu-id="94155-224">decrypt</span></span>
- <span data-ttu-id="94155-225">wrapKey</span><span class="sxs-lookup"><span data-stu-id="94155-225">wrapKey</span></span>
- <span data-ttu-id="94155-226">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="94155-226">unwrapKey</span></span>
- <span data-ttu-id="94155-227">znak</span><span class="sxs-lookup"><span data-stu-id="94155-227">sign</span></span>
- <span data-ttu-id="94155-228">weryfikuj</span><span class="sxs-lookup"><span data-stu-id="94155-228">verify</span></span>
- <span data-ttu-id="94155-229">importowanie (dotyczy tylko KEK, zobacz przykład 7)</span><span class="sxs-lookup"><span data-stu-id="94155-229">import (for KEK only, see example 7)</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-230">-KeyType</span><span class="sxs-lookup"><span data-stu-id="94155-230">-KeyType</span></span>
<span data-ttu-id="94155-231">Określa typ klucza tego klucza.</span><span class="sxs-lookup"><span data-stu-id="94155-231">Specifies the key type of this key.</span></span> <span data-ttu-id="94155-232">Podczas importowania kluczy BYOK wartość domyślna to "RSA".</span><span class="sxs-lookup"><span data-stu-id="94155-232">When importing BYOK keys, it defaults to 'RSA'.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-233">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="94155-233">-Name</span></span>
<span data-ttu-id="94155-234">Określa nazwę klucza do dodania do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="94155-234">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="94155-235">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, która jest określana przez ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="94155-235">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="94155-236">Nazwa musi być ciągiem o długości od 1 do 63 znaków, który zawiera tylko wartości 0-9, a-z, A-Z i - (symbol kreski).</span><span class="sxs-lookup"><span data-stu-id="94155-236">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-237">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="94155-237">-NotBefore</span></span>
<span data-ttu-id="94155-238">Określa czas jako obiekt **DateTime,** przed którym nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="94155-238">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="94155-239">Ten parametr używa czasu UTC.</span><span class="sxs-lookup"><span data-stu-id="94155-239">This parameter uses UTC.</span></span> <span data-ttu-id="94155-240">Aby uzyskać obiekt **DateTime,** użyj polecenia cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="94155-240">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="94155-241">Jeśli nie określisz tego parametru, klucz może zostać użyty natychmiast.</span><span class="sxs-lookup"><span data-stu-id="94155-241">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-242">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94155-242">-ResourceId</span></span>
<span data-ttu-id="94155-243">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="94155-243">Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94155-244">— Rozmiar</span><span class="sxs-lookup"><span data-stu-id="94155-244">-Size</span></span>
<span data-ttu-id="94155-245">Rozmiar klucza RSA w bitach.</span><span class="sxs-lookup"><span data-stu-id="94155-245">RSA key size, in bits.</span></span> <span data-ttu-id="94155-246">Jeśli nie zostanie określona, usługa udostępni bezpieczny domyślny standard.</span><span class="sxs-lookup"><span data-stu-id="94155-246">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-247">— Tag</span><span class="sxs-lookup"><span data-stu-id="94155-247">-Tag</span></span>
<span data-ttu-id="94155-248">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="94155-248">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="94155-249">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="94155-249">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-250">-VaultName</span><span class="sxs-lookup"><span data-stu-id="94155-250">-VaultName</span></span>
<span data-ttu-id="94155-251">Określa nazwę magazynu kluczy, do którego to polecenie cmdlet dodaje klucz.</span><span class="sxs-lookup"><span data-stu-id="94155-251">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="94155-252">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, która jest określana przez ten parametr i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="94155-252">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-253">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94155-253">-Confirm</span></span>
<span data-ttu-id="94155-254">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94155-254">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-255">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94155-255">-WhatIf</span></span>
<span data-ttu-id="94155-256">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94155-256">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94155-257">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94155-257">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94155-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94155-258">CommonParameters</span></span>
<span data-ttu-id="94155-259">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94155-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94155-260">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94155-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94155-261">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94155-261">INPUTS</span></span>

### <span data-ttu-id="94155-262">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="94155-262">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="94155-263">System.String</span><span class="sxs-lookup"><span data-stu-id="94155-263">System.String</span></span>

## <span data-ttu-id="94155-264">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94155-264">OUTPUTS</span></span>

### <span data-ttu-id="94155-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94155-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="94155-266">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94155-266">NOTES</span></span>

## <span data-ttu-id="94155-267">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94155-267">RELATED LINKS</span></span>

[<span data-ttu-id="94155-268">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94155-268">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="94155-269">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94155-269">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="94155-270">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94155-270">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="94155-271">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="94155-271">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
