---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: b01ed80385726660198d3f6fbb20ab1e5ec57dfe
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893065"
---
# <span data-ttu-id="5bdf6-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5bdf6-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="5bdf6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5bdf6-102">SYNOPSIS</span></span>
<span data-ttu-id="5bdf6-103">Tworzy klucz w magazynie kluczy lub importuje klucz do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="5bdf6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5bdf6-104">SYNTAX</span></span>

### <span data-ttu-id="5bdf6-105">Utwórz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5bdf6-105">Create (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bdf6-106">Przywoz</span><span class="sxs-lookup"><span data-stu-id="5bdf6-106">Import</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bdf6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5bdf6-107">DESCRIPTION</span></span>
<span data-ttu-id="5bdf6-108">Polecenie cmdlet **Add-AzKeyVaultKey** tworzy klucz w magazynie kluczy w magazynie kluczy Azure lub importuje klucz do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-108">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="5bdf6-109">Za pomocą tego polecenia cmdlet można dodawać klucze przy użyciu dowolnej z poniższych metod:</span><span class="sxs-lookup"><span data-stu-id="5bdf6-109">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="5bdf6-110">Utwórz klucz w sprzęcie sprzętowym modułu zabezpieczeń (HSM) w usłudze Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-110">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="5bdf6-111">Utwórz klucz w oprogramowaniu w usłudze Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-111">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="5bdf6-112">Zaimportuj klucz z własnego sprzętu sprzętowego modułu zabezpieczeń (HSM), aby HSMs w usłudze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-112">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="5bdf6-113">Importowanie klucza z pliku PFX na komputerze.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-113">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="5bdf6-114">Zaimportuj klucz z pliku PFX na komputerze do modułów zabezpieczeń sprzętowych (HSMs) w usłudze Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-114">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="5bdf6-115">W przypadku dowolnej z tych operacji możesz podać atrybuty klucza lub zaakceptować ustawienia domyślne.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-115">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="5bdf6-116">W przypadku utworzenia lub zaimportowania klucza o takiej samej nazwie jak istniejący klucz w magazynie kluczy oryginalny klucz zostanie zaktualizowany o wartości określone dla nowego klucza.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-116">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="5bdf6-117">Dostęp do poprzednich wartości można uzyskać przy użyciu identyfikatora URI specyficznego dla wersji dla tej wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-117">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="5bdf6-118">Aby uzyskać informacje na temat wersji kluczowych i struktury identyfikatora URI, zobacz [Informacje o kluczach andSecrets](http://go.microsoft.com/fwlink/?linkid=518560) w dokumentacji interfejsu API w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-118">To learn about key versions and the URI structure, see [About Keys andSecrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="5bdf6-119">Uwaga: Aby zaimportować klucz z własnego sprzętowego modułu zabezpieczeń, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku BYOK) przy użyciu narzędzia BYOK magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-119">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="5bdf6-120">Aby uzyskać więcej informacji, zobacz [sposób generowania i transferowania kluczy HSM-Protected dla magazynu kluczy platformy Azure](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="5bdf6-120">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="5bdf6-121">Najlepszym rozwiązaniem jest wykonanie kopii zapasowej klucza po jego utworzeniu lub zaktualizowaniu za pomocą polecenia cmdlet Backup-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-121">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="5bdf6-122">Nie ma żadnych funkcji usuwania zmian, więc jeśli przypadkowo usuniesz klucz lub usuniesz go, a następnie zmienisz zdanie, nie będzie można odzyskać klucza, chyba że masz kopię zapasową, którą możesz przywrócić.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-122">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="5bdf6-123">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5bdf6-123">EXAMPLES</span></span>

### <span data-ttu-id="5bdf6-124">Przykład 1. Tworzenie klucza</span><span class="sxs-lookup"><span data-stu-id="5bdf6-124">Example 1: Create a key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="5bdf6-125">To polecenie tworzy klucz chroniony oprogramowaniem o nazwie ITSoftware w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-125">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="5bdf6-126">Przykład 2: Tworzenie klucza chronionego przy użyciu modułu HSM</span><span class="sxs-lookup"><span data-stu-id="5bdf6-126">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="5bdf6-127">To polecenie tworzy klucz chroniony przez HSM w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-127">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="5bdf6-128">Przykład 3: Tworzenie klucza z wartościami niedomyślnymi</span><span class="sxs-lookup"><span data-stu-id="5bdf6-128">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="5bdf6-129">Pierwsze polecenie zapisuje wartości w postaci odszyfrowania i weryfikacji w zmiennej $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-129">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="5bdf6-130">Drugie polecenie tworzy obiekt **DateTime** , zdefiniowany w formacie UTC, przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="5bdf6-130">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="5bdf6-131">Ten obiekt Określa godzinę w przyszłości w dwóch latach.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-131">That object specifies a time two years in the future.</span></span> <span data-ttu-id="5bdf6-132">Polecenie zapisuje tę datę w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-132">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="5bdf6-133">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="5bdf6-133">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="5bdf6-134">Trzecie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="5bdf6-134">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="5bdf6-135">Ten obiekt określa bieżący czas UTC.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-135">That object specifies current UTC time.</span></span> <span data-ttu-id="5bdf6-136">Polecenie zapisuje tę datę w zmiennej $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-136">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="5bdf6-137">Ostatnie polecenie tworzy klucz o nazwie ITHsmNonDefault, który jest kluczem chronionym przy użyciu modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-137">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="5bdf6-138">W poleceniu są określone wartości dozwolonych kluczowych operacji przechowywanych $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-138">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="5bdf6-139">Polecenie określa czasy, w jakich parametry *Expires* i *NotBefore* zostały utworzone w poprzednich poleceniach, oraz znaczniki wysokiej wagi i.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-139">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="5bdf6-140">Nowy klucz jest wyłączony.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-140">The new key is disabled.</span></span> <span data-ttu-id="5bdf6-141">Możesz ją włączyć za pomocą polecenia cmdlet **Set-AzKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="5bdf6-141">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="5bdf6-142">Przykład 4: Importowanie klucza chronionego przez HSM</span><span class="sxs-lookup"><span data-stu-id="5bdf6-142">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="5bdf6-143">To polecenie importuje klucz o nazwie ITByok z lokalizacji, w której określono parametr Key *FilePath* .</span><span class="sxs-lookup"><span data-stu-id="5bdf6-143">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="5bdf6-144">Importowany klucz jest kluczem chronionym przy użyciu modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-144">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="5bdf6-145">Aby zaimportować klucz z własnego sprzętowego modułu zabezpieczeń, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku BYOK) przy użyciu przybornika kluczy usługi Azure BYOK.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-145">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="5bdf6-146">Aby uzyskać więcej informacji, zobacz [sposób generowania i transferowania kluczy HSM-Protected dla magazynu kluczy platformy Azure](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="5bdf6-146">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="5bdf6-147">Przykład 5: Importowanie klucza chronionego oprogramowaniem</span><span class="sxs-lookup"><span data-stu-id="5bdf6-147">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="5bdf6-148">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-148">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="5bdf6-149">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="5bdf6-149">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="5bdf6-150">Drugie polecenie tworzy hasło oprogramowania w magazynie kluczy contoso.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-150">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="5bdf6-151">Polecenie określa lokalizację klucza i hasło przechowywane w $Password.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-151">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="5bdf6-152">Przykład 6: Importowanie klucza i przypisywanie atrybutów</span><span class="sxs-lookup"><span data-stu-id="5bdf6-152">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="5bdf6-153">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-153">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="5bdf6-154">Drugie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** , a następnie zapisuje ten obiekt w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-154">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="5bdf6-155">Trzecie polecenie tworzy zmienną $tags, aby ustawić znaczniki wysokiej wagi i je.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-155">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="5bdf6-156">Polecenie ostatnie importuje klucz jako klucz HSM z określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-156">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="5bdf6-157">Polecenie określa czas wygaśnięcia przechowywany w $Expires i hasło przechowywane w $Password i stosuje Tagi przechowywane w $tags.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-157">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="5bdf6-158">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5bdf6-158">PARAMETERS</span></span>

### <span data-ttu-id="5bdf6-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bdf6-159">-DefaultProfile</span></span>
<span data-ttu-id="5bdf6-160">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5bdf6-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf6-161">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="5bdf6-161">-Destination</span></span>
<span data-ttu-id="5bdf6-162">Określa, czy chcesz dodać ten klucz jako klucz chroniony oprogramowaniem, czy klucz chroniony HSM w usłudze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-162">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="5bdf6-163">Prawidłowe wartości to: HSM i Software.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-163">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="5bdf6-164">Uwaga: Aby używać modułu HSM jako miejsca docelowego, musisz mieć kluczowy magazyn obsługujący HSMs.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-164">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="5bdf6-165">Aby uzyskać więcej informacji na temat warstw usług i funkcji magazynu kluczy platformy Azure, zobacz [witrynę sieci Web usługi Azure Key](http://go.microsoft.com/fwlink/?linkid=512521)about.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-165">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="5bdf6-166">Ten parametr jest wymagany podczas tworzenia nowego klucza.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-166">This parameter is required when you create a new key.</span></span> <span data-ttu-id="5bdf6-167">Jeśli importujesz klucz za pomocą parametru *FilePath* , ten parametr jest opcjonalny:</span><span class="sxs-lookup"><span data-stu-id="5bdf6-167">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="5bdf6-168">Jeśli ten parametr nie jest określony, a polecenie cmdlet powoduje zaimportowanie klucza z rozszerzeniem nazwy pliku BYOK, powoduje to zaimportowanie tego klucza jako klucza chronionego przy użyciu modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-168">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="5bdf6-169">Polecenie cmdlet nie może zaimportować tego klucza jako klucza chronionego oprogramowaniem.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-169">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="5bdf6-170">Jeśli ten parametr nie jest określony, a polecenie cmdlet spowoduje zaimportowanie klucza o rozszerzeniu nazwy pliku PFX, program zaimportuje klucz jako klucz chroniony oprogramowaniem.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-170">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf6-171">-Disable</span><span class="sxs-lookup"><span data-stu-id="5bdf6-171">-Disable</span></span>
<span data-ttu-id="5bdf6-172">Wskazuje, że dodawany klawisz jest ustawiony na początkowy stan wyłączony.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-172">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="5bdf6-173">Każda próba użycia tego klawisza zakończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-173">Any attempt to use the key will fail.</span></span> <span data-ttu-id="5bdf6-174">Tego parametru należy użyć, jeśli wstępnie załadowano klucze, które mają być później włączone.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-174">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf6-175">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="5bdf6-175">-Expires</span></span>
<span data-ttu-id="5bdf6-176">Określa czas wygaśnięcia jako obiekt **DateTime** dla klucza, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-176">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="5bdf6-177">W tym parametrze jest używany uniwersalny czas koordynowany (UTC).</span><span class="sxs-lookup"><span data-stu-id="5bdf6-177">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="5bdf6-178">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="5bdf6-178">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="5bdf6-179">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="5bdf6-179">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="5bdf6-180">Jeśli nie określisz tego parametru, klucz nie wygasa.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-180">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf6-181">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="5bdf6-181">-KeyFilePassword</span></span>
<span data-ttu-id="5bdf6-182">Określa hasło importowanego pliku jako obiekt **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="5bdf6-182">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="5bdf6-183">Aby uzyskać obiekt **SecureString** , użyj polecenia cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="5bdf6-183">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="5bdf6-184">Aby uzyskać więcej informacji, wpisz tekst `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="5bdf6-184">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="5bdf6-185">Musisz określić to hasło, aby zaimportować plik z rozszerzeniem nazwy pliku PFX.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-185">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf6-186">-FilePath</span><span class="sxs-lookup"><span data-stu-id="5bdf6-186">-KeyFilePath</span></span>
<span data-ttu-id="5bdf6-187">Określa ścieżkę pliku lokalnego zawierającego kluczowe materiały importowane przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-187">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="5bdf6-188">Prawidłowe rozszerzenia nazw plików to. BYOK i. pfx.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-188">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="5bdf6-189">Jeśli plik jest plikiem BYOK, po zakończeniu importu klucz jest automatycznie chroniony przez HSMs i nie można zastąpić tego ustawienia domyślnego.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-189">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="5bdf6-190">Jeśli plik jest plikiem pfx, po zakończeniu importowania klucz jest automatycznie chroniony przez oprogramowanie.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-190">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="5bdf6-191">Aby zastąpić to ustawienie domyślne, ustaw parametr *lokalizacja_docelowa* na HSM, tak aby klucz był chroniony za pomocą modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-191">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="5bdf6-192">Po określeniu tego parametru parametr *docelowy* jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-192">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf6-193">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="5bdf6-193">-KeyOps</span></span>
<span data-ttu-id="5bdf6-194">Określa tablicę operacji, które można wykonać przy użyciu klucza, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-194">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="5bdf6-195">Jeśli nie podano tego parametru, można wykonać wszystkie operacje.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-195">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="5bdf6-196">Dopuszczalne wartości tego parametru to rozdzielana przecinkami lista podstawowych operacji, które zdefiniowano w [specyfikacji klucza internetowego JSON (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="5bdf6-196">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="5bdf6-197">Szyfrowane</span><span class="sxs-lookup"><span data-stu-id="5bdf6-197">Encrypt</span></span>
- <span data-ttu-id="5bdf6-198">Szyfruj</span><span class="sxs-lookup"><span data-stu-id="5bdf6-198">Decrypt</span></span>
- <span data-ttu-id="5bdf6-199">Pakuj</span><span class="sxs-lookup"><span data-stu-id="5bdf6-199">Wrap</span></span>
- <span data-ttu-id="5bdf6-200">Odwinięcie</span><span class="sxs-lookup"><span data-stu-id="5bdf6-200">Unwrap</span></span>
- <span data-ttu-id="5bdf6-201">Zapisywania</span><span class="sxs-lookup"><span data-stu-id="5bdf6-201">Sign</span></span>
- <span data-ttu-id="5bdf6-202">Sprawdzić</span><span class="sxs-lookup"><span data-stu-id="5bdf6-202">Verify</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf6-203">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5bdf6-203">-Name</span></span>
<span data-ttu-id="5bdf6-204">Określa nazwę klucza, który ma zostać dodany do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-204">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="5bdf6-205">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-205">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="5bdf6-206">Nazwa musi zawierać ciąg od 1 do 63 znaków, który zawiera tylko 0-9, a-z, a-Z i-(symbol kreski).</span><span class="sxs-lookup"><span data-stu-id="5bdf6-206">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf6-207">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="5bdf6-207">-NotBefore</span></span>
<span data-ttu-id="5bdf6-208">Określa czas (w postaci obiektu **DateTime** ), przed którym nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-208">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="5bdf6-209">Ten parametr używa czasu UTC.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-209">This parameter uses UTC.</span></span> <span data-ttu-id="5bdf6-210">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="5bdf6-210">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="5bdf6-211">Jeśli ten parametr nie jest określony, klucz może być natychmiast wykorzystany.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-211">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf6-212">-Tag</span><span class="sxs-lookup"><span data-stu-id="5bdf6-212">-Tag</span></span>
<span data-ttu-id="5bdf6-213">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-213">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5bdf6-214">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="5bdf6-214">For example:</span></span>

<span data-ttu-id="5bdf6-215">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5bdf6-215">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf6-216">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="5bdf6-216">-VaultName</span></span>
<span data-ttu-id="5bdf6-217">Określa nazwę magazynu kluczy, do którego jest dodawany klucz polecenia.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-217">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="5bdf6-218">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-218">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf6-219">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5bdf6-219">-Confirm</span></span>
<span data-ttu-id="5bdf6-220">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-220">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf6-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bdf6-221">-WhatIf</span></span>
<span data-ttu-id="5bdf6-222">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bdf6-223">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-223">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdf6-224">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bdf6-224">CommonParameters</span></span>
<span data-ttu-id="5bdf6-225">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-225">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bdf6-226">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bdf6-226">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bdf6-227">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bdf6-227">INPUTS</span></span>

### <span data-ttu-id="5bdf6-228">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5bdf6-228">None</span></span>
<span data-ttu-id="5bdf6-229">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-229">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5bdf6-230">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5bdf6-230">OUTPUTS</span></span>

### <span data-ttu-id="5bdf6-231">Microsoft. Azure. Commands. platforming. MODELES.</span><span class="sxs-lookup"><span data-stu-id="5bdf6-231">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="5bdf6-232">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5bdf6-232">NOTES</span></span>

## <span data-ttu-id="5bdf6-233">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bdf6-233">RELATED LINKS</span></span>

[<span data-ttu-id="5bdf6-234">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5bdf6-234">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="5bdf6-235">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5bdf6-235">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="5bdf6-236">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5bdf6-236">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="5bdf6-237">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="5bdf6-237">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
