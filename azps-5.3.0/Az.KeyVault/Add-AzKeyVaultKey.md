---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 6cea7f2584de3a27be2cee36c3f32fd792564160
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503383"
---
# <span data-ttu-id="75665-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75665-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="75665-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75665-102">SYNOPSIS</span></span>
<span data-ttu-id="75665-103">Tworzy klucz w magazynie kluczy lub importuje klucz do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="75665-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="75665-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75665-104">SYNTAX</span></span>

### <span data-ttu-id="75665-105">InteractiveCreate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="75665-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75665-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="75665-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75665-107">HsmInteractiveCreate</span><span class="sxs-lookup"><span data-stu-id="75665-107">HsmInteractiveCreate</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75665-108">HsmInteractiveImport</span><span class="sxs-lookup"><span data-stu-id="75665-108">HsmInteractiveImport</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75665-109">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="75665-109">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75665-110">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="75665-110">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75665-111">HsmInputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="75665-111">HsmInputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75665-112">HsmInputObjectImport</span><span class="sxs-lookup"><span data-stu-id="75665-112">HsmInputObjectImport</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75665-113">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="75665-113">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75665-114">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="75665-114">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75665-115">HsmResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="75665-115">HsmResourceIdCreate</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75665-116">HsmResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="75665-116">HsmResourceIdImport</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75665-117">Opis</span><span class="sxs-lookup"><span data-stu-id="75665-117">DESCRIPTION</span></span>
<span data-ttu-id="75665-118">Polecenie cmdlet **Add-AzKeyVaultKey** tworzy klucz w magazynie kluczy w magazynie kluczy Azure lub importuje klucz do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="75665-118">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="75665-119">Za pomocą tego polecenia cmdlet można dodawać klucze przy użyciu dowolnej z poniższych metod:</span><span class="sxs-lookup"><span data-stu-id="75665-119">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="75665-120">Utwórz klucz w sprzęcie sprzętowym modułu zabezpieczeń (HSM) w usłudze Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="75665-120">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="75665-121">Utwórz klucz w oprogramowaniu w usłudze Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="75665-121">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="75665-122">Zaimportuj klucz z własnego sprzętu sprzętowego modułu zabezpieczeń (HSM), aby HSMs w usłudze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="75665-122">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="75665-123">Importowanie klucza z pliku PFX na komputerze.</span><span class="sxs-lookup"><span data-stu-id="75665-123">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="75665-124">Zaimportuj klucz z pliku PFX na komputerze do modułów zabezpieczeń sprzętowych (HSMs) w usłudze Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="75665-124">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="75665-125">W przypadku dowolnej z tych operacji możesz podać atrybuty klucza lub zaakceptować ustawienia domyślne.</span><span class="sxs-lookup"><span data-stu-id="75665-125">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="75665-126">W przypadku utworzenia lub zaimportowania klucza o takiej samej nazwie jak istniejący klucz w magazynie kluczy oryginalny klucz zostanie zaktualizowany o wartości określone dla nowego klucza.</span><span class="sxs-lookup"><span data-stu-id="75665-126">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="75665-127">Dostęp do poprzednich wartości można uzyskać przy użyciu identyfikatora URI specyficznego dla wersji dla tej wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="75665-127">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="75665-128">Aby uzyskać informacje na temat wersji kluczowych i struktury identyfikatora URI, zobacz [Informacje o kluczach i hasłach](http://go.microsoft.com/fwlink/?linkid=518560) w dokumentacji interfejsu API w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="75665-128">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="75665-129">Uwaga: Aby zaimportować klucz z własnego sprzętowego modułu zabezpieczeń, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku BYOK) przy użyciu narzędzia BYOK magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="75665-129">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="75665-130">Aby uzyskać więcej informacji, zobacz [sposób generowania i transferowania kluczy HSM-Protected dla magazynu kluczy platformy Azure](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="75665-130">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="75665-131">Najlepszym rozwiązaniem jest wykonanie kopii zapasowej klucza po jego utworzeniu lub zaktualizowaniu za pomocą polecenia cmdlet Backup-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="75665-131">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="75665-132">Nie ma żadnych funkcji usuwania zmian, więc jeśli przypadkowo usuniesz klucz lub usuniesz go, a następnie zmienisz zdanie, nie będzie można odzyskać klucza, chyba że masz kopię zapasową, którą możesz przywrócić.</span><span class="sxs-lookup"><span data-stu-id="75665-132">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="75665-133">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75665-133">EXAMPLES</span></span>

### <span data-ttu-id="75665-134">Przykład 1. Tworzenie klucza</span><span class="sxs-lookup"><span data-stu-id="75665-134">Example 1: Create a key</span></span>
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

<span data-ttu-id="75665-135">To polecenie tworzy klucz chroniony oprogramowaniem o nazwie ITSoftware w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="75665-135">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="75665-136">Przykład 2: Tworzenie klucza chronionego przy użyciu modułu HSM</span><span class="sxs-lookup"><span data-stu-id="75665-136">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="75665-137">To polecenie tworzy klucz chroniony przez HSM w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="75665-137">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="75665-138">Przykład 3: Tworzenie klucza z wartościami niedomyślnymi</span><span class="sxs-lookup"><span data-stu-id="75665-138">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="75665-139">Pierwsze polecenie zapisuje wartości w postaci odszyfrowania i weryfikacji w zmiennej $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="75665-139">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="75665-140">Drugie polecenie tworzy obiekt **DateTime** , zdefiniowany w formacie UTC, przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="75665-140">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="75665-141">Ten obiekt Określa godzinę w przyszłości w dwóch latach.</span><span class="sxs-lookup"><span data-stu-id="75665-141">That object specifies a time two years in the future.</span></span> <span data-ttu-id="75665-142">Polecenie zapisuje tę datę w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="75665-142">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="75665-143">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="75665-143">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="75665-144">Trzecie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="75665-144">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="75665-145">Ten obiekt określa bieżący czas UTC.</span><span class="sxs-lookup"><span data-stu-id="75665-145">That object specifies current UTC time.</span></span> <span data-ttu-id="75665-146">Polecenie zapisuje tę datę w zmiennej $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="75665-146">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="75665-147">Ostatnie polecenie tworzy klucz o nazwie ITHsmNonDefault, który jest kluczem chronionym przy użyciu modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="75665-147">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="75665-148">W poleceniu są określone wartości dozwolonych kluczowych operacji przechowywanych $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="75665-148">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="75665-149">Polecenie określa czasy, w jakich parametry *Expires* i *NotBefore* zostały utworzone w poprzednich poleceniach, oraz znaczniki wysokiej wagi i.</span><span class="sxs-lookup"><span data-stu-id="75665-149">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="75665-150">Nowy klucz jest wyłączony.</span><span class="sxs-lookup"><span data-stu-id="75665-150">The new key is disabled.</span></span> <span data-ttu-id="75665-151">Możesz ją włączyć za pomocą polecenia cmdlet **Set-AzKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="75665-151">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="75665-152">Przykład 4: Importowanie klucza chronionego przez HSM</span><span class="sxs-lookup"><span data-stu-id="75665-152">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="75665-153">To polecenie importuje klucz o nazwie ITByok z lokalizacji, w której określono parametr Key *FilePath* .</span><span class="sxs-lookup"><span data-stu-id="75665-153">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="75665-154">Importowany klucz jest kluczem chronionym przy użyciu modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="75665-154">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="75665-155">Aby zaimportować klucz z własnego sprzętowego modułu zabezpieczeń, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku BYOK) przy użyciu przybornika kluczy usługi Azure BYOK.</span><span class="sxs-lookup"><span data-stu-id="75665-155">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="75665-156">Aby uzyskać więcej informacji, zobacz [sposób generowania i transferowania kluczy HSM-Protected dla magazynu kluczy platformy Azure](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="75665-156">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="75665-157">Przykład 5: Importowanie klucza chronionego oprogramowaniem</span><span class="sxs-lookup"><span data-stu-id="75665-157">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="75665-158">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="75665-158">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="75665-159">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="75665-159">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="75665-160">Drugie polecenie tworzy hasło oprogramowania w magazynie kluczy contoso.</span><span class="sxs-lookup"><span data-stu-id="75665-160">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="75665-161">Polecenie określa lokalizację klucza i hasło przechowywane w $Password.</span><span class="sxs-lookup"><span data-stu-id="75665-161">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="75665-162">Przykład 6: Importowanie klucza i przypisywanie atrybutów</span><span class="sxs-lookup"><span data-stu-id="75665-162">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="75665-163">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="75665-163">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="75665-164">Drugie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** , a następnie zapisuje ten obiekt w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="75665-164">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="75665-165">Trzecie polecenie tworzy zmienną $tags, aby ustawić znaczniki wysokiej wagi i je.</span><span class="sxs-lookup"><span data-stu-id="75665-165">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="75665-166">Polecenie ostatnie importuje klucz jako klucz HSM z określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="75665-166">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="75665-167">Polecenie określa czas wygaśnięcia przechowywany w $Expires i hasło przechowywane w $Password i stosuje Tagi przechowywane w $tags.</span><span class="sxs-lookup"><span data-stu-id="75665-167">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="75665-168">Przykład 7: generowanie klucza wymiany kluczy (KEK) dla funkcji "Dobierz własny klucz" (BYOK)</span><span class="sxs-lookup"><span data-stu-id="75665-168">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="75665-169">Generuje klucz (nazywany kluczem wymiany kluczy (KEK)).</span><span class="sxs-lookup"><span data-stu-id="75665-169">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="75665-170">KEK musi być kluczem modułu RSA-HSM, który ma tylko operację importowania klucza.</span><span class="sxs-lookup"><span data-stu-id="75665-170">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="75665-171">Tylko klucze modułu HSM RSA obsługują tylko Magazyn kluczy Premium.</span><span class="sxs-lookup"><span data-stu-id="75665-171">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="75665-172">Więcej informacji znajdziesz w sekcji https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="75665-172">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="75665-173">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75665-173">PARAMETERS</span></span>

### <span data-ttu-id="75665-174">-Zakrętname</span><span class="sxs-lookup"><span data-stu-id="75665-174">-CurveName</span></span>
<span data-ttu-id="75665-175">Określa nazwę krzywej kryptografii krzywej eliptycznej, która jest prawidłowa, gdy właściwość KeyType ma wartość EC.</span><span class="sxs-lookup"><span data-stu-id="75665-175">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75665-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75665-176">-DefaultProfile</span></span>
<span data-ttu-id="75665-177">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="75665-177">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75665-178">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="75665-178">-Destination</span></span>
<span data-ttu-id="75665-179">Określa, czy chcesz dodać ten klucz jako klucz chroniony oprogramowaniem, czy klucz chroniony HSM w usłudze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="75665-179">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="75665-180">Prawidłowe wartości to: HSM i Software.</span><span class="sxs-lookup"><span data-stu-id="75665-180">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="75665-181">Uwaga: Aby używać modułu HSM jako miejsca docelowego, musisz mieć kluczowy magazyn obsługujący HSMs.</span><span class="sxs-lookup"><span data-stu-id="75665-181">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="75665-182">Aby uzyskać więcej informacji na temat warstw usług i funkcji magazynu kluczy platformy Azure, zobacz [witrynę sieci Web usługi Azure Key](http://go.microsoft.com/fwlink/?linkid=512521)about.</span><span class="sxs-lookup"><span data-stu-id="75665-182">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="75665-183">Ten parametr jest wymagany podczas tworzenia nowego klucza.</span><span class="sxs-lookup"><span data-stu-id="75665-183">This parameter is required when you create a new key.</span></span> <span data-ttu-id="75665-184">Jeśli importujesz klucz za pomocą parametru *FilePath* , ten parametr jest opcjonalny:</span><span class="sxs-lookup"><span data-stu-id="75665-184">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="75665-185">Jeśli ten parametr nie jest określony, a polecenie cmdlet powoduje zaimportowanie klucza z rozszerzeniem nazwy pliku BYOK, powoduje to zaimportowanie tego klucza jako klucza chronionego przy użyciu modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="75665-185">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="75665-186">Polecenie cmdlet nie może zaimportować tego klucza jako klucza chronionego oprogramowaniem.</span><span class="sxs-lookup"><span data-stu-id="75665-186">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="75665-187">Jeśli ten parametr nie jest określony, a polecenie cmdlet spowoduje zaimportowanie klucza o rozszerzeniu nazwy pliku PFX, program zaimportuje klucz jako klucz chroniony oprogramowaniem.</span><span class="sxs-lookup"><span data-stu-id="75665-187">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="75665-188">-Disable</span><span class="sxs-lookup"><span data-stu-id="75665-188">-Disable</span></span>
<span data-ttu-id="75665-189">Wskazuje, że dodawany klawisz jest ustawiony na początkowy stan wyłączony.</span><span class="sxs-lookup"><span data-stu-id="75665-189">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="75665-190">Każda próba użycia tego klawisza zakończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="75665-190">Any attempt to use the key will fail.</span></span> <span data-ttu-id="75665-191">Tego parametru należy użyć, jeśli wstępnie załadowano klucze, które mają być później włączone.</span><span class="sxs-lookup"><span data-stu-id="75665-191">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="75665-192">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="75665-192">-Expires</span></span>
<span data-ttu-id="75665-193">Określa czas wygaśnięcia jako obiekt **DateTime** dla klucza, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75665-193">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="75665-194">W tym parametrze jest używany uniwersalny czas koordynowany (UTC).</span><span class="sxs-lookup"><span data-stu-id="75665-194">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="75665-195">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="75665-195">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="75665-196">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="75665-196">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="75665-197">Jeśli nie określisz tego parametru, klucz nie wygasa.</span><span class="sxs-lookup"><span data-stu-id="75665-197">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="75665-198">-HsmName</span><span class="sxs-lookup"><span data-stu-id="75665-198">-HsmName</span></span>
<span data-ttu-id="75665-199">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="75665-199">HSM name.</span></span> <span data-ttu-id="75665-200">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="75665-200">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="75665-201">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="75665-201">-HsmObject</span></span>
<span data-ttu-id="75665-202">Obiekt HSM.</span><span class="sxs-lookup"><span data-stu-id="75665-202">HSM object.</span></span>

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

### <span data-ttu-id="75665-203">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="75665-203">-HsmResourceId</span></span>
<span data-ttu-id="75665-204">Identyfikator zasobu modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="75665-204">Resource ID of the HSM.</span></span>

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

### <span data-ttu-id="75665-205">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="75665-205">-InputObject</span></span>
<span data-ttu-id="75665-206">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="75665-206">Vault object.</span></span>

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

### <span data-ttu-id="75665-207">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="75665-207">-KeyFilePassword</span></span>
<span data-ttu-id="75665-208">Określa hasło importowanego pliku jako obiekt **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="75665-208">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="75665-209">Aby uzyskać obiekt **SecureString** , użyj polecenia cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="75665-209">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="75665-210">Aby uzyskać więcej informacji, wpisz tekst `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="75665-210">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="75665-211">Musisz określić to hasło, aby zaimportować plik z rozszerzeniem nazwy pliku PFX.</span><span class="sxs-lookup"><span data-stu-id="75665-211">You must specify this password to import a file with a .pfx file name extension.</span></span>

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

### <span data-ttu-id="75665-212">-FilePath</span><span class="sxs-lookup"><span data-stu-id="75665-212">-KeyFilePath</span></span>
<span data-ttu-id="75665-213">Określa ścieżkę pliku lokalnego zawierającego kluczowe materiały importowane przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="75665-213">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="75665-214">Prawidłowe rozszerzenia nazw plików to. BYOK i. pfx.</span><span class="sxs-lookup"><span data-stu-id="75665-214">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="75665-215">Jeśli plik jest plikiem BYOK, po zakończeniu importu klucz jest automatycznie chroniony przez HSMs i nie można zastąpić tego ustawienia domyślnego.</span><span class="sxs-lookup"><span data-stu-id="75665-215">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="75665-216">Jeśli plik jest plikiem pfx, po zakończeniu importowania klucz jest automatycznie chroniony przez oprogramowanie.</span><span class="sxs-lookup"><span data-stu-id="75665-216">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="75665-217">Aby zastąpić to ustawienie domyślne, ustaw parametr *lokalizacja_docelowa* na HSM, tak aby klucz był chroniony za pomocą modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="75665-217">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="75665-218">Po określeniu tego parametru parametr *docelowy* jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="75665-218">When you specify this parameter, the *Destination* parameter is optional.</span></span>

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

### <span data-ttu-id="75665-219">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="75665-219">-KeyOps</span></span>
<span data-ttu-id="75665-220">Określa tablicę operacji, które można wykonać przy użyciu klucza, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75665-220">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="75665-221">Jeśli nie podano tego parametru, można wykonać wszystkie operacje.</span><span class="sxs-lookup"><span data-stu-id="75665-221">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="75665-222">Dopuszczalne wartości tego parametru to rozdzielana przecinkami lista podstawowych operacji, które zdefiniowano w [specyfikacji klucza internetowego JSON (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="75665-222">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="75665-223">szyfrowane</span><span class="sxs-lookup"><span data-stu-id="75665-223">encrypt</span></span>
- <span data-ttu-id="75665-224">Szyfruj</span><span class="sxs-lookup"><span data-stu-id="75665-224">decrypt</span></span>
- <span data-ttu-id="75665-225">wrapKey</span><span class="sxs-lookup"><span data-stu-id="75665-225">wrapKey</span></span>
- <span data-ttu-id="75665-226">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="75665-226">unwrapKey</span></span>
- <span data-ttu-id="75665-227">zapisywania</span><span class="sxs-lookup"><span data-stu-id="75665-227">sign</span></span>
- <span data-ttu-id="75665-228">sprawdzić</span><span class="sxs-lookup"><span data-stu-id="75665-228">verify</span></span>
- <span data-ttu-id="75665-229">Importowanie (tylko w przypadku KEK, zobacz przykład 7)</span><span class="sxs-lookup"><span data-stu-id="75665-229">import (for KEK only, see example 7)</span></span>

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

### <span data-ttu-id="75665-230">-KeyType</span><span class="sxs-lookup"><span data-stu-id="75665-230">-KeyType</span></span>
<span data-ttu-id="75665-231">Określa typ klucza dla tego klucza.</span><span class="sxs-lookup"><span data-stu-id="75665-231">Specifies the key type of this key.</span></span>

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

### <span data-ttu-id="75665-232">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="75665-232">-Name</span></span>
<span data-ttu-id="75665-233">Określa nazwę klucza, który ma zostać dodany do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="75665-233">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="75665-234">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="75665-234">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="75665-235">Nazwa musi zawierać ciąg od 1 do 63 znaków, który zawiera tylko 0-9, a-z, a-Z i-(symbol kreski).</span><span class="sxs-lookup"><span data-stu-id="75665-235">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="75665-236">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="75665-236">-NotBefore</span></span>
<span data-ttu-id="75665-237">Określa czas (w postaci obiektu **DateTime** ), przed którym nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="75665-237">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="75665-238">Ten parametr używa czasu UTC.</span><span class="sxs-lookup"><span data-stu-id="75665-238">This parameter uses UTC.</span></span> <span data-ttu-id="75665-239">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="75665-239">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="75665-240">Jeśli ten parametr nie jest określony, klucz może być natychmiast wykorzystany.</span><span class="sxs-lookup"><span data-stu-id="75665-240">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="75665-241">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75665-241">-ResourceId</span></span>
<span data-ttu-id="75665-242">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="75665-242">Vault Resource Id.</span></span>

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

### <span data-ttu-id="75665-243">-Size</span><span class="sxs-lookup"><span data-stu-id="75665-243">-Size</span></span>
<span data-ttu-id="75665-244">Rozmiar klucza RSA w bitach.</span><span class="sxs-lookup"><span data-stu-id="75665-244">RSA key size, in bits.</span></span> <span data-ttu-id="75665-245">Jeśli nie zostanie określona, usługa będzie dostarczać bezpieczne ustawienia domyślne.</span><span class="sxs-lookup"><span data-stu-id="75665-245">If not specified, the service will provide a safe default.</span></span>

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

### <span data-ttu-id="75665-246">-Tag</span><span class="sxs-lookup"><span data-stu-id="75665-246">-Tag</span></span>
<span data-ttu-id="75665-247">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="75665-247">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="75665-248">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="75665-248">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="75665-249">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="75665-249">-VaultName</span></span>
<span data-ttu-id="75665-250">Określa nazwę magazynu kluczy, do którego jest dodawany klucz polecenia.</span><span class="sxs-lookup"><span data-stu-id="75665-250">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="75665-251">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="75665-251">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="75665-252">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="75665-252">-Confirm</span></span>
<span data-ttu-id="75665-253">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75665-253">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75665-254">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75665-254">-WhatIf</span></span>
<span data-ttu-id="75665-255">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75665-255">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75665-256">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="75665-256">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75665-257">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75665-257">CommonParameters</span></span>
<span data-ttu-id="75665-258">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75665-258">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75665-259">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75665-259">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75665-260">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75665-260">INPUTS</span></span>

### <span data-ttu-id="75665-261">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="75665-261">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="75665-262">System. String</span><span class="sxs-lookup"><span data-stu-id="75665-262">System.String</span></span>

## <span data-ttu-id="75665-263">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75665-263">OUTPUTS</span></span>

### <span data-ttu-id="75665-264">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75665-264">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="75665-265">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75665-265">NOTES</span></span>

## <span data-ttu-id="75665-266">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75665-266">RELATED LINKS</span></span>

[<span data-ttu-id="75665-267">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75665-267">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="75665-268">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75665-268">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="75665-269">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="75665-269">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="75665-270">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="75665-270">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
