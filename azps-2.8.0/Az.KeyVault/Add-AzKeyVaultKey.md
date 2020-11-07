---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: f7447725e63634642f285b6a796a2b59b4d1d301
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705189"
---
# <span data-ttu-id="678f0-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="678f0-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="678f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="678f0-102">SYNOPSIS</span></span>
<span data-ttu-id="678f0-103">Tworzy klucz w magazynie kluczy lub importuje klucz do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="678f0-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="678f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="678f0-104">SYNTAX</span></span>

### <span data-ttu-id="678f0-105">InteractiveCreate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="678f0-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="678f0-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="678f0-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="678f0-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="678f0-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="678f0-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="678f0-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="678f0-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="678f0-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="678f0-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="678f0-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="678f0-111">Opis</span><span class="sxs-lookup"><span data-stu-id="678f0-111">DESCRIPTION</span></span>
<span data-ttu-id="678f0-112">Polecenie cmdlet **Add-AzKeyVaultKey** tworzy klucz w magazynie kluczy w magazynie kluczy Azure lub importuje klucz do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="678f0-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="678f0-113">Za pomocą tego polecenia cmdlet można dodawać klucze przy użyciu dowolnej z poniższych metod:</span><span class="sxs-lookup"><span data-stu-id="678f0-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="678f0-114">Utwórz klucz w sprzęcie sprzętowym modułu zabezpieczeń (HSM) w usłudze Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="678f0-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="678f0-115">Utwórz klucz w oprogramowaniu w usłudze Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="678f0-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="678f0-116">Zaimportuj klucz z własnego sprzętu sprzętowego modułu zabezpieczeń (HSM), aby HSMs w usłudze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="678f0-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="678f0-117">Importowanie klucza z pliku PFX na komputerze.</span><span class="sxs-lookup"><span data-stu-id="678f0-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="678f0-118">Zaimportuj klucz z pliku PFX na komputerze do modułów zabezpieczeń sprzętowych (HSMs) w usłudze Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="678f0-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="678f0-119">W przypadku dowolnej z tych operacji możesz podać atrybuty klucza lub zaakceptować ustawienia domyślne.</span><span class="sxs-lookup"><span data-stu-id="678f0-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="678f0-120">W przypadku utworzenia lub zaimportowania klucza o takiej samej nazwie jak istniejący klucz w magazynie kluczy oryginalny klucz zostanie zaktualizowany o wartości określone dla nowego klucza.</span><span class="sxs-lookup"><span data-stu-id="678f0-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="678f0-121">Dostęp do poprzednich wartości można uzyskać przy użyciu identyfikatora URI specyficznego dla wersji dla tej wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="678f0-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="678f0-122">Aby uzyskać informacje na temat wersji kluczowych i struktury identyfikatora URI, zobacz [Informacje o kluczach i hasłach](https://go.microsoft.com/fwlink/?linkid=518560) w dokumentacji interfejsu API w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="678f0-122">To learn about key versions and the URI structure, see [About Keys and Secrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="678f0-123">Uwaga: Aby zaimportować klucz z własnego sprzętowego modułu zabezpieczeń, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku BYOK) przy użyciu narzędzia BYOK magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="678f0-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="678f0-124">Aby uzyskać więcej informacji, zobacz [sposób generowania i transferowania kluczy HSM-Protected dla magazynu kluczy platformy Azure](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="678f0-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="678f0-125">Najlepszym rozwiązaniem jest wykonanie kopii zapasowej klucza po jego utworzeniu lub zaktualizowaniu za pomocą polecenia cmdlet Backup-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="678f0-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="678f0-126">Nie ma żadnych funkcji usuwania zmian, więc jeśli przypadkowo usuniesz klucz lub usuniesz go, a następnie zmienisz zdanie, nie będzie można odzyskać klucza, chyba że masz kopię zapasową, którą możesz przywrócić.</span><span class="sxs-lookup"><span data-stu-id="678f0-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="678f0-127">Przykłady</span><span class="sxs-lookup"><span data-stu-id="678f0-127">EXAMPLES</span></span>

### <span data-ttu-id="678f0-128">Przykład 1. Tworzenie klucza</span><span class="sxs-lookup"><span data-stu-id="678f0-128">Example 1: Create a key</span></span>
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

<span data-ttu-id="678f0-129">To polecenie tworzy klucz chroniony oprogramowaniem o nazwie ITSoftware w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="678f0-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="678f0-130">Przykład 2: Tworzenie klucza chronionego przy użyciu modułu HSM</span><span class="sxs-lookup"><span data-stu-id="678f0-130">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="678f0-131">To polecenie tworzy klucz chroniony przez HSM w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="678f0-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="678f0-132">Przykład 3: Tworzenie klucza z wartościami niedomyślnymi</span><span class="sxs-lookup"><span data-stu-id="678f0-132">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="678f0-133">Pierwsze polecenie zapisuje wartości w postaci odszyfrowania i weryfikacji w zmiennej $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="678f0-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="678f0-134">Drugie polecenie tworzy obiekt **DateTime** , zdefiniowany w formacie UTC, przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="678f0-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="678f0-135">Ten obiekt Określa godzinę w przyszłości w dwóch latach.</span><span class="sxs-lookup"><span data-stu-id="678f0-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="678f0-136">Polecenie zapisuje tę datę w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="678f0-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="678f0-137">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="678f0-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="678f0-138">Trzecie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="678f0-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="678f0-139">Ten obiekt określa bieżący czas UTC.</span><span class="sxs-lookup"><span data-stu-id="678f0-139">That object specifies current UTC time.</span></span> <span data-ttu-id="678f0-140">Polecenie zapisuje tę datę w zmiennej $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="678f0-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="678f0-141">Ostatnie polecenie tworzy klucz o nazwie ITHsmNonDefault, który jest kluczem chronionym przy użyciu modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="678f0-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="678f0-142">W poleceniu są określone wartości dozwolonych kluczowych operacji przechowywanych $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="678f0-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="678f0-143">Polecenie określa czasy, w jakich parametry *Expires* i *NotBefore* zostały utworzone w poprzednich poleceniach, oraz znaczniki wysokiej wagi i.</span><span class="sxs-lookup"><span data-stu-id="678f0-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="678f0-144">Nowy klucz jest wyłączony.</span><span class="sxs-lookup"><span data-stu-id="678f0-144">The new key is disabled.</span></span> <span data-ttu-id="678f0-145">Możesz ją włączyć za pomocą polecenia cmdlet **Set-AzKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="678f0-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="678f0-146">Przykład 4: Importowanie klucza chronionego przez HSM</span><span class="sxs-lookup"><span data-stu-id="678f0-146">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="678f0-147">To polecenie importuje klucz o nazwie ITByok z lokalizacji, w której określono parametr Key *FilePath* .</span><span class="sxs-lookup"><span data-stu-id="678f0-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="678f0-148">Importowany klucz jest kluczem chronionym przy użyciu modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="678f0-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="678f0-149">Aby zaimportować klucz z własnego sprzętowego modułu zabezpieczeń, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku BYOK) przy użyciu przybornika kluczy usługi Azure BYOK.</span><span class="sxs-lookup"><span data-stu-id="678f0-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="678f0-150">Aby uzyskać więcej informacji, zobacz [sposób generowania i transferowania kluczy HSM-Protected dla magazynu kluczy platformy Azure](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="678f0-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="678f0-151">Przykład 5: Importowanie klucza chronionego oprogramowaniem</span><span class="sxs-lookup"><span data-stu-id="678f0-151">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="678f0-152">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="678f0-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="678f0-153">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="678f0-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="678f0-154">Drugie polecenie tworzy hasło oprogramowania w magazynie kluczy contoso.</span><span class="sxs-lookup"><span data-stu-id="678f0-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="678f0-155">Polecenie określa lokalizację klucza i hasło przechowywane w $Password.</span><span class="sxs-lookup"><span data-stu-id="678f0-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="678f0-156">Przykład 6: Importowanie klucza i przypisywanie atrybutów</span><span class="sxs-lookup"><span data-stu-id="678f0-156">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="678f0-157">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="678f0-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="678f0-158">Drugie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** , a następnie zapisuje ten obiekt w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="678f0-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="678f0-159">Trzecie polecenie tworzy zmienną $tags, aby ustawić znaczniki wysokiej wagi i je.</span><span class="sxs-lookup"><span data-stu-id="678f0-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="678f0-160">Polecenie ostatnie importuje klucz jako klucz HSM z określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="678f0-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="678f0-161">Polecenie określa czas wygaśnięcia przechowywany w $Expires i hasło przechowywane w $Password i stosuje Tagi przechowywane w $tags.</span><span class="sxs-lookup"><span data-stu-id="678f0-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="678f0-162">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="678f0-162">PARAMETERS</span></span>

### <span data-ttu-id="678f0-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678f0-163">-DefaultProfile</span></span>
<span data-ttu-id="678f0-164">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="678f0-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="678f0-165">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="678f0-165">-Destination</span></span>
<span data-ttu-id="678f0-166">Określa, czy chcesz dodać ten klucz jako klucz chroniony oprogramowaniem, czy klucz chroniony HSM w usłudze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="678f0-166">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="678f0-167">Prawidłowe wartości to: HSM i Software.</span><span class="sxs-lookup"><span data-stu-id="678f0-167">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="678f0-168">Uwaga: Aby używać modułu HSM jako miejsca docelowego, musisz mieć kluczowy magazyn obsługujący HSMs.</span><span class="sxs-lookup"><span data-stu-id="678f0-168">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="678f0-169">Aby uzyskać więcej informacji na temat warstw usług i funkcji magazynu kluczy platformy Azure, zobacz [witrynę sieci Web usługi Azure Key](https://go.microsoft.com/fwlink/?linkid=512521)about.</span><span class="sxs-lookup"><span data-stu-id="678f0-169">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="678f0-170">Ten parametr jest wymagany podczas tworzenia nowego klucza.</span><span class="sxs-lookup"><span data-stu-id="678f0-170">This parameter is required when you create a new key.</span></span> <span data-ttu-id="678f0-171">Jeśli importujesz klucz za pomocą parametru *FilePath* , ten parametr jest opcjonalny:</span><span class="sxs-lookup"><span data-stu-id="678f0-171">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="678f0-172">Jeśli ten parametr nie jest określony, a polecenie cmdlet powoduje zaimportowanie klucza z rozszerzeniem nazwy pliku BYOK, powoduje to zaimportowanie tego klucza jako klucza chronionego przy użyciu modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="678f0-172">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="678f0-173">Polecenie cmdlet nie może zaimportować tego klucza jako klucza chronionego oprogramowaniem.</span><span class="sxs-lookup"><span data-stu-id="678f0-173">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="678f0-174">Jeśli ten parametr nie jest określony, a polecenie cmdlet spowoduje zaimportowanie klucza o rozszerzeniu nazwy pliku PFX, program zaimportuje klucz jako klucz chroniony oprogramowaniem.</span><span class="sxs-lookup"><span data-stu-id="678f0-174">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="678f0-175">-Disable</span><span class="sxs-lookup"><span data-stu-id="678f0-175">-Disable</span></span>
<span data-ttu-id="678f0-176">Wskazuje, że dodawany klawisz jest ustawiony na początkowy stan wyłączony.</span><span class="sxs-lookup"><span data-stu-id="678f0-176">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="678f0-177">Każda próba użycia tego klawisza zakończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="678f0-177">Any attempt to use the key will fail.</span></span> <span data-ttu-id="678f0-178">Tego parametru należy użyć, jeśli wstępnie załadowano klucze, które mają być później włączone.</span><span class="sxs-lookup"><span data-stu-id="678f0-178">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="678f0-179">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="678f0-179">-Expires</span></span>
<span data-ttu-id="678f0-180">Określa czas wygaśnięcia jako obiekt **DateTime** dla klucza, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="678f0-180">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="678f0-181">W tym parametrze jest używany uniwersalny czas koordynowany (UTC).</span><span class="sxs-lookup"><span data-stu-id="678f0-181">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="678f0-182">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="678f0-182">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="678f0-183">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="678f0-183">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="678f0-184">Jeśli nie określisz tego parametru, klucz nie wygasa.</span><span class="sxs-lookup"><span data-stu-id="678f0-184">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="678f0-185">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="678f0-185">-InputObject</span></span>
<span data-ttu-id="678f0-186">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="678f0-186">Vault object.</span></span>

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

### <span data-ttu-id="678f0-187">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="678f0-187">-KeyFilePassword</span></span>
<span data-ttu-id="678f0-188">Określa hasło importowanego pliku jako obiekt **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="678f0-188">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="678f0-189">Aby uzyskać obiekt **SecureString** , użyj polecenia cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="678f0-189">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="678f0-190">Aby uzyskać więcej informacji, wpisz tekst `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="678f0-190">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="678f0-191">Musisz określić to hasło, aby zaimportować plik z rozszerzeniem nazwy pliku PFX.</span><span class="sxs-lookup"><span data-stu-id="678f0-191">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678f0-192">-FilePath</span><span class="sxs-lookup"><span data-stu-id="678f0-192">-KeyFilePath</span></span>
<span data-ttu-id="678f0-193">Określa ścieżkę pliku lokalnego zawierającego kluczowe materiały importowane przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="678f0-193">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="678f0-194">Prawidłowe rozszerzenia nazw plików to. BYOK i. pfx.</span><span class="sxs-lookup"><span data-stu-id="678f0-194">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="678f0-195">Jeśli plik jest plikiem BYOK, po zakończeniu importu klucz jest automatycznie chroniony przez HSMs i nie można zastąpić tego ustawienia domyślnego.</span><span class="sxs-lookup"><span data-stu-id="678f0-195">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="678f0-196">Jeśli plik jest plikiem pfx, po zakończeniu importowania klucz jest automatycznie chroniony przez oprogramowanie.</span><span class="sxs-lookup"><span data-stu-id="678f0-196">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="678f0-197">Aby zastąpić to ustawienie domyślne, ustaw parametr *lokalizacja_docelowa* na HSM, tak aby klucz był chroniony za pomocą modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="678f0-197">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="678f0-198">Po określeniu tego parametru parametr *docelowy* jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="678f0-198">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678f0-199">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="678f0-199">-KeyOps</span></span>
<span data-ttu-id="678f0-200">Określa tablicę operacji, które można wykonać przy użyciu klucza, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="678f0-200">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="678f0-201">Jeśli nie podano tego parametru, można wykonać wszystkie operacje.</span><span class="sxs-lookup"><span data-stu-id="678f0-201">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="678f0-202">Dopuszczalne wartości tego parametru to rozdzielana przecinkami lista podstawowych operacji, które zdefiniowano w [specyfikacji klucza internetowego JSON (JWK)](https://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="678f0-202">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="678f0-203">Szyfrowane</span><span class="sxs-lookup"><span data-stu-id="678f0-203">Encrypt</span></span>
- <span data-ttu-id="678f0-204">Szyfruj</span><span class="sxs-lookup"><span data-stu-id="678f0-204">Decrypt</span></span>
- <span data-ttu-id="678f0-205">Pakuj</span><span class="sxs-lookup"><span data-stu-id="678f0-205">Wrap</span></span>
- <span data-ttu-id="678f0-206">Odwinięcie</span><span class="sxs-lookup"><span data-stu-id="678f0-206">Unwrap</span></span>
- <span data-ttu-id="678f0-207">Zapisywania</span><span class="sxs-lookup"><span data-stu-id="678f0-207">Sign</span></span>
- <span data-ttu-id="678f0-208">Sprawdzić</span><span class="sxs-lookup"><span data-stu-id="678f0-208">Verify</span></span>

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

### <span data-ttu-id="678f0-209">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="678f0-209">-Name</span></span>
<span data-ttu-id="678f0-210">Określa nazwę klucza, który ma zostać dodany do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="678f0-210">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="678f0-211">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="678f0-211">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="678f0-212">Nazwa musi zawierać ciąg od 1 do 63 znaków, który zawiera tylko 0-9, a-z, a-Z i-(symbol kreski).</span><span class="sxs-lookup"><span data-stu-id="678f0-212">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="678f0-213">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="678f0-213">-NotBefore</span></span>
<span data-ttu-id="678f0-214">Określa czas (w postaci obiektu **DateTime** ), przed którym nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="678f0-214">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="678f0-215">Ten parametr używa czasu UTC.</span><span class="sxs-lookup"><span data-stu-id="678f0-215">This parameter uses UTC.</span></span> <span data-ttu-id="678f0-216">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="678f0-216">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="678f0-217">Jeśli ten parametr nie jest określony, klucz może być natychmiast wykorzystany.</span><span class="sxs-lookup"><span data-stu-id="678f0-217">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="678f0-218">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="678f0-218">-ResourceId</span></span>
<span data-ttu-id="678f0-219">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="678f0-219">Vault Resource Id.</span></span>

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

### <span data-ttu-id="678f0-220">-Size</span><span class="sxs-lookup"><span data-stu-id="678f0-220">-Size</span></span>
<span data-ttu-id="678f0-221">Rozmiar klucza RSA w bitach.</span><span class="sxs-lookup"><span data-stu-id="678f0-221">RSA key size, in bits.</span></span> <span data-ttu-id="678f0-222">Jeśli nie zostanie określona, usługa będzie dostarczać bezpieczne ustawienia domyślne.</span><span class="sxs-lookup"><span data-stu-id="678f0-222">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678f0-223">-Tag</span><span class="sxs-lookup"><span data-stu-id="678f0-223">-Tag</span></span>
<span data-ttu-id="678f0-224">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="678f0-224">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="678f0-225">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="678f0-225">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="678f0-226">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="678f0-226">-VaultName</span></span>
<span data-ttu-id="678f0-227">Określa nazwę magazynu kluczy, do którego jest dodawany klucz polecenia.</span><span class="sxs-lookup"><span data-stu-id="678f0-227">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="678f0-228">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="678f0-228">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="678f0-229">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="678f0-229">-Confirm</span></span>
<span data-ttu-id="678f0-230">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="678f0-230">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="678f0-231">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="678f0-231">-WhatIf</span></span>
<span data-ttu-id="678f0-232">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="678f0-232">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="678f0-233">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="678f0-233">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="678f0-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678f0-234">CommonParameters</span></span>
<span data-ttu-id="678f0-235">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="678f0-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678f0-236">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="678f0-236">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678f0-237">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="678f0-237">INPUTS</span></span>

### <span data-ttu-id="678f0-238">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="678f0-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="678f0-239">System. String</span><span class="sxs-lookup"><span data-stu-id="678f0-239">System.String</span></span>

## <span data-ttu-id="678f0-240">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="678f0-240">OUTPUTS</span></span>

### <span data-ttu-id="678f0-241">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="678f0-241">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="678f0-242">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="678f0-242">NOTES</span></span>

## <span data-ttu-id="678f0-243">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="678f0-243">RELATED LINKS</span></span>

[<span data-ttu-id="678f0-244">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="678f0-244">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="678f0-245">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="678f0-245">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="678f0-246">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="678f0-246">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="678f0-247">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="678f0-247">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
