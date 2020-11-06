---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
ms.openlocfilehash: 153cd3099b750732e281992e98cdafb173a71276
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548996"
---
# <span data-ttu-id="59970-101">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="59970-101">Add-AzureKeyVaultKey</span></span>

## <span data-ttu-id="59970-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59970-102">SYNOPSIS</span></span>
<span data-ttu-id="59970-103">Tworzy klucz w magazynie kluczy lub importuje klucz do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="59970-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59970-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59970-104">SYNTAX</span></span>

### <span data-ttu-id="59970-105">InteractiveCreate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="59970-105">InteractiveCreate (Default)</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59970-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="59970-106">InteractiveImport</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59970-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="59970-107">InputObjectCreate</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59970-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="59970-108">InputObjectImport</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59970-109">Opis</span><span class="sxs-lookup"><span data-stu-id="59970-109">DESCRIPTION</span></span>
<span data-ttu-id="59970-110">Polecenie cmdlet **Add-AzureKeyVaultKey** tworzy klucz w magazynie kluczy w magazynie kluczy Azure lub importuje klucz do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="59970-110">The **Add-AzureKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="59970-111">Za pomocą tego polecenia cmdlet można dodawać klucze przy użyciu dowolnej z poniższych metod:</span><span class="sxs-lookup"><span data-stu-id="59970-111">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="59970-112">Utwórz klucz w sprzęcie sprzętowym modułu zabezpieczeń (HSM) w usłudze Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="59970-112">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="59970-113">Utwórz klucz w oprogramowaniu w usłudze Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="59970-113">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="59970-114">Zaimportuj klucz z własnego sprzętu sprzętowego modułu zabezpieczeń (HSM), aby HSMs w usłudze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="59970-114">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="59970-115">Importowanie klucza z pliku PFX na komputerze.</span><span class="sxs-lookup"><span data-stu-id="59970-115">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="59970-116">Zaimportuj klucz z pliku PFX na komputerze do modułów zabezpieczeń sprzętowych (HSMs) w usłudze Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="59970-116">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="59970-117">W przypadku dowolnej z tych operacji możesz podać atrybuty klucza lub zaakceptować ustawienia domyślne.</span><span class="sxs-lookup"><span data-stu-id="59970-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="59970-118">W przypadku utworzenia lub zaimportowania klucza o takiej samej nazwie jak istniejący klucz w magazynie kluczy oryginalny klucz zostanie zaktualizowany o wartości określone dla nowego klucza.</span><span class="sxs-lookup"><span data-stu-id="59970-118">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="59970-119">Dostęp do poprzednich wartości można uzyskać przy użyciu identyfikatora URI specyficznego dla wersji dla tej wersji klucza.</span><span class="sxs-lookup"><span data-stu-id="59970-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="59970-120">Aby uzyskać informacje na temat wersji kluczowych i struktury identyfikatora URI, zobacz [Informacje o kluczach andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) w dokumentacji interfejsu API w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="59970-120">To learn about key versions and the URI structure, see [About Keys andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="59970-121">Uwaga: Aby zaimportować klucz z własnego sprzętowego modułu zabezpieczeń, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku BYOK) przy użyciu narzędzia BYOK magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="59970-121">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="59970-122">Aby uzyskać więcej informacji, zobacz [sposób generowania i transferowania kluczy HSM-Protected dla magazynu kluczy platformy Azure](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="59970-122">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="59970-123">Najlepszym rozwiązaniem jest wykonanie kopii zapasowej klucza po jego utworzeniu lub zaktualizowaniu za pomocą polecenia cmdlet Backup-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="59970-123">As a best practice, back up your key after it is created or updated, by using the Backup-AzureKeyVaultKey cmdlet.</span></span> <span data-ttu-id="59970-124">Nie ma żadnych funkcji usuwania zmian, więc jeśli przypadkowo usuniesz klucz lub usuniesz go, a następnie zmienisz zdanie, nie będzie można odzyskać klucza, chyba że masz kopię zapasową, którą możesz przywrócić.</span><span class="sxs-lookup"><span data-stu-id="59970-124">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="59970-125">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59970-125">EXAMPLES</span></span>

### <span data-ttu-id="59970-126">Przykład 1. Tworzenie klucza</span><span class="sxs-lookup"><span data-stu-id="59970-126">Example 1: Create a key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="59970-127">To polecenie tworzy klucz chroniony oprogramowaniem o nazwie ITSoftware w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="59970-127">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="59970-128">Przykład 2: Tworzenie klucza chronionego przy użyciu modułu HSM</span><span class="sxs-lookup"><span data-stu-id="59970-128">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="59970-129">To polecenie tworzy klucz chroniony przez HSM w magazynie kluczy o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="59970-129">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="59970-130">Przykład 3: Tworzenie klucza z wartościami niedomyślnymi</span><span class="sxs-lookup"><span data-stu-id="59970-130">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="59970-131">Pierwsze polecenie zapisuje wartości w postaci odszyfrowania i weryfikacji w zmiennej $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="59970-131">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="59970-132">Drugie polecenie tworzy obiekt **DateTime** , zdefiniowany w formacie UTC, przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="59970-132">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="59970-133">Ten obiekt Określa godzinę w przyszłości w dwóch latach.</span><span class="sxs-lookup"><span data-stu-id="59970-133">That object specifies a time two years in the future.</span></span> <span data-ttu-id="59970-134">Polecenie zapisuje tę datę w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="59970-134">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="59970-135">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="59970-135">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="59970-136">Trzecie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="59970-136">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="59970-137">Ten obiekt określa bieżący czas UTC.</span><span class="sxs-lookup"><span data-stu-id="59970-137">That object specifies current UTC time.</span></span> <span data-ttu-id="59970-138">Polecenie zapisuje tę datę w zmiennej $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="59970-138">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="59970-139">Ostatnie polecenie tworzy klucz o nazwie ITHsmNonDefault, który jest kluczem chronionym przy użyciu modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="59970-139">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="59970-140">W poleceniu są określone wartości dozwolonych kluczowych operacji przechowywanych $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="59970-140">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="59970-141">Polecenie określa czasy, w jakich parametry *Expires* i *NotBefore* zostały utworzone w poprzednich poleceniach, oraz znaczniki wysokiej wagi i.</span><span class="sxs-lookup"><span data-stu-id="59970-141">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="59970-142">Nowy klucz jest wyłączony.</span><span class="sxs-lookup"><span data-stu-id="59970-142">The new key is disabled.</span></span> <span data-ttu-id="59970-143">Możesz ją włączyć za pomocą polecenia cmdlet **Set-AzureKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="59970-143">You can enable it by using the **Set-AzureKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="59970-144">Przykład 4: Importowanie klucza chronionego przez HSM</span><span class="sxs-lookup"><span data-stu-id="59970-144">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="59970-145">To polecenie importuje klucz o nazwie ITByok z lokalizacji, w której określono parametr Key *FilePath* .</span><span class="sxs-lookup"><span data-stu-id="59970-145">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="59970-146">Importowany klucz jest kluczem chronionym przy użyciu modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="59970-146">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="59970-147">Aby zaimportować klucz z własnego sprzętowego modułu zabezpieczeń, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku BYOK) przy użyciu przybornika kluczy usługi Azure BYOK.</span><span class="sxs-lookup"><span data-stu-id="59970-147">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="59970-148">Aby uzyskać więcej informacji, zobacz [sposób generowania i transferowania kluczy HSM-Protected dla magazynu kluczy platformy Azure](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="59970-148">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="59970-149">Przykład 5: Importowanie klucza chronionego oprogramowaniem</span><span class="sxs-lookup"><span data-stu-id="59970-149">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="59970-150">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="59970-150">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="59970-151">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="59970-151">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="59970-152">Drugie polecenie tworzy hasło oprogramowania w magazynie kluczy contoso.</span><span class="sxs-lookup"><span data-stu-id="59970-152">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="59970-153">Polecenie określa lokalizację klucza i hasło przechowywane w $Password.</span><span class="sxs-lookup"><span data-stu-id="59970-153">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="59970-154">Przykład 6: Importowanie klucza i przypisywanie atrybutów</span><span class="sxs-lookup"><span data-stu-id="59970-154">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="59970-155">Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="59970-155">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="59970-156">Drugie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** , a następnie zapisuje ten obiekt w zmiennej $Expires.</span><span class="sxs-lookup"><span data-stu-id="59970-156">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="59970-157">Trzecie polecenie tworzy zmienną $tags, aby ustawić znaczniki wysokiej wagi i je.</span><span class="sxs-lookup"><span data-stu-id="59970-157">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="59970-158">Polecenie ostatnie importuje klucz jako klucz HSM z określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="59970-158">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="59970-159">Polecenie określa czas wygaśnięcia przechowywany w $Expires i hasło przechowywane w $Password i stosuje Tagi przechowywane w $tags.</span><span class="sxs-lookup"><span data-stu-id="59970-159">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="59970-160">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59970-160">PARAMETERS</span></span>

### <span data-ttu-id="59970-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59970-161">-DefaultProfile</span></span>
<span data-ttu-id="59970-162">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="59970-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59970-163">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="59970-163">-Destination</span></span>
<span data-ttu-id="59970-164">Określa, czy chcesz dodać ten klucz jako klucz chroniony oprogramowaniem, czy klucz chroniony HSM w usłudze magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="59970-164">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="59970-165">Prawidłowe wartości to: HSM i Software.</span><span class="sxs-lookup"><span data-stu-id="59970-165">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="59970-166">Uwaga: Aby używać modułu HSM jako miejsca docelowego, musisz mieć kluczowy magazyn obsługujący HSMs.</span><span class="sxs-lookup"><span data-stu-id="59970-166">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="59970-167">Aby uzyskać więcej informacji na temat warstw usług i funkcji magazynu kluczy platformy Azure, zobacz [witrynę sieci Web usługi Azure Key](https://go.microsoft.com/fwlink/?linkid=512521)about.</span><span class="sxs-lookup"><span data-stu-id="59970-167">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="59970-168">Ten parametr jest wymagany podczas tworzenia nowego klucza.</span><span class="sxs-lookup"><span data-stu-id="59970-168">This parameter is required when you create a new key.</span></span> <span data-ttu-id="59970-169">Jeśli importujesz klucz za pomocą parametru *FilePath* , ten parametr jest opcjonalny:</span><span class="sxs-lookup"><span data-stu-id="59970-169">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="59970-170">Jeśli ten parametr nie jest określony, a polecenie cmdlet powoduje zaimportowanie klucza z rozszerzeniem nazwy pliku BYOK, powoduje to zaimportowanie tego klucza jako klucza chronionego przy użyciu modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="59970-170">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="59970-171">Polecenie cmdlet nie może zaimportować tego klucza jako klucza chronionego oprogramowaniem.</span><span class="sxs-lookup"><span data-stu-id="59970-171">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="59970-172">Jeśli ten parametr nie jest określony, a polecenie cmdlet spowoduje zaimportowanie klucza o rozszerzeniu nazwy pliku PFX, program zaimportuje klucz jako klucz chroniony oprogramowaniem.</span><span class="sxs-lookup"><span data-stu-id="59970-172">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveCreate, InputObjectCreate
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
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59970-173">-Disable</span><span class="sxs-lookup"><span data-stu-id="59970-173">-Disable</span></span>
<span data-ttu-id="59970-174">Wskazuje, że dodawany klawisz jest ustawiony na początkowy stan wyłączony.</span><span class="sxs-lookup"><span data-stu-id="59970-174">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="59970-175">Każda próba użycia tego klawisza zakończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="59970-175">Any attempt to use the key will fail.</span></span> <span data-ttu-id="59970-176">Tego parametru należy użyć, jeśli wstępnie załadowano klucze, które mają być później włączone.</span><span class="sxs-lookup"><span data-stu-id="59970-176">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="59970-177">-Wygasa</span><span class="sxs-lookup"><span data-stu-id="59970-177">-Expires</span></span>
<span data-ttu-id="59970-178">Określa czas wygaśnięcia jako obiekt **DateTime** dla klucza, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59970-178">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="59970-179">W tym parametrze jest używany uniwersalny czas koordynowany (UTC).</span><span class="sxs-lookup"><span data-stu-id="59970-179">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="59970-180">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="59970-180">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="59970-181">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="59970-181">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="59970-182">Jeśli nie określisz tego parametru, klucz nie wygasa.</span><span class="sxs-lookup"><span data-stu-id="59970-182">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="59970-183">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="59970-183">-InputObject</span></span>
<span data-ttu-id="59970-184">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="59970-184">Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59970-185">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="59970-185">-KeyFilePassword</span></span>
<span data-ttu-id="59970-186">Określa hasło importowanego pliku jako obiekt **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="59970-186">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="59970-187">Aby uzyskać obiekt **SecureString** , użyj polecenia cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="59970-187">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="59970-188">Aby uzyskać więcej informacji, wpisz tekst `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="59970-188">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="59970-189">Musisz określić to hasło, aby zaimportować plik z rozszerzeniem nazwy pliku PFX.</span><span class="sxs-lookup"><span data-stu-id="59970-189">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: SecureString
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59970-190">-FilePath</span><span class="sxs-lookup"><span data-stu-id="59970-190">-KeyFilePath</span></span>
<span data-ttu-id="59970-191">Określa ścieżkę pliku lokalnego zawierającego kluczowe materiały importowane przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="59970-191">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="59970-192">Prawidłowe rozszerzenia nazw plików to. BYOK i. pfx.</span><span class="sxs-lookup"><span data-stu-id="59970-192">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="59970-193">Jeśli plik jest plikiem BYOK, po zakończeniu importu klucz jest automatycznie chroniony przez HSMs i nie można zastąpić tego ustawienia domyślnego.</span><span class="sxs-lookup"><span data-stu-id="59970-193">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="59970-194">Jeśli plik jest plikiem pfx, po zakończeniu importowania klucz jest automatycznie chroniony przez oprogramowanie.</span><span class="sxs-lookup"><span data-stu-id="59970-194">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="59970-195">Aby zastąpić to ustawienie domyślne, ustaw parametr *lokalizacja_docelowa* na HSM, tak aby klucz był chroniony za pomocą modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="59970-195">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="59970-196">Po określeniu tego parametru parametr *docelowy* jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="59970-196">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59970-197">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="59970-197">-KeyOps</span></span>
<span data-ttu-id="59970-198">Określa tablicę operacji, które można wykonać przy użyciu klucza, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59970-198">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="59970-199">Jeśli nie podano tego parametru, można wykonać wszystkie operacje.</span><span class="sxs-lookup"><span data-stu-id="59970-199">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="59970-200">Dopuszczalne wartości tego parametru to rozdzielana przecinkami lista podstawowych operacji, które zdefiniowano w [specyfikacji klucza internetowego JSON (JWK)](https://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="59970-200">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="59970-201">Szyfrowane</span><span class="sxs-lookup"><span data-stu-id="59970-201">Encrypt</span></span>
- <span data-ttu-id="59970-202">Szyfruj</span><span class="sxs-lookup"><span data-stu-id="59970-202">Decrypt</span></span>
- <span data-ttu-id="59970-203">Pakuj</span><span class="sxs-lookup"><span data-stu-id="59970-203">Wrap</span></span>
- <span data-ttu-id="59970-204">Odwinięcie</span><span class="sxs-lookup"><span data-stu-id="59970-204">Unwrap</span></span>
- <span data-ttu-id="59970-205">Zapisywania</span><span class="sxs-lookup"><span data-stu-id="59970-205">Sign</span></span>
- <span data-ttu-id="59970-206">Sprawdzić</span><span class="sxs-lookup"><span data-stu-id="59970-206">Verify</span></span>

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

### <span data-ttu-id="59970-207">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="59970-207">-Name</span></span>
<span data-ttu-id="59970-208">Określa nazwę klucza, który ma zostać dodany do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="59970-208">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="59970-209">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="59970-209">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="59970-210">Nazwa musi zawierać ciąg od 1 do 63 znaków, który zawiera tylko 0-9, a-z, a-Z i-(symbol kreski).</span><span class="sxs-lookup"><span data-stu-id="59970-210">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="59970-211">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="59970-211">-NotBefore</span></span>
<span data-ttu-id="59970-212">Określa czas (w postaci obiektu **DateTime** ), przed którym nie można użyć klucza.</span><span class="sxs-lookup"><span data-stu-id="59970-212">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="59970-213">Ten parametr używa czasu UTC.</span><span class="sxs-lookup"><span data-stu-id="59970-213">This parameter uses UTC.</span></span> <span data-ttu-id="59970-214">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="59970-214">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="59970-215">Jeśli ten parametr nie jest określony, klucz może być natychmiast wykorzystany.</span><span class="sxs-lookup"><span data-stu-id="59970-215">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="59970-216">-Tag</span><span class="sxs-lookup"><span data-stu-id="59970-216">-Tag</span></span>
<span data-ttu-id="59970-217">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="59970-217">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="59970-218">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="59970-218">For example:</span></span>

<span data-ttu-id="59970-219">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="59970-219">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="59970-220">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="59970-220">-VaultName</span></span>
<span data-ttu-id="59970-221">Określa nazwę magazynu kluczy, do którego jest dodawany klucz polecenia.</span><span class="sxs-lookup"><span data-stu-id="59970-221">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="59970-222">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="59970-222">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59970-223">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59970-223">-Confirm</span></span>
<span data-ttu-id="59970-224">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59970-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59970-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59970-225">-WhatIf</span></span>
<span data-ttu-id="59970-226">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59970-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59970-227">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="59970-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59970-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59970-228">CommonParameters</span></span>
<span data-ttu-id="59970-229">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59970-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59970-230">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59970-230">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59970-231">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59970-231">INPUTS</span></span>

### <span data-ttu-id="59970-232">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="59970-232">None</span></span>
<span data-ttu-id="59970-233">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="59970-233">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59970-234">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59970-234">OUTPUTS</span></span>

### <span data-ttu-id="59970-235">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="59970-235">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="59970-236">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59970-236">NOTES</span></span>

## <span data-ttu-id="59970-237">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59970-237">RELATED LINKS</span></span>

[<span data-ttu-id="59970-238">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="59970-238">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="59970-239">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="59970-239">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="59970-240">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="59970-240">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="59970-241">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="59970-241">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)
