---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
ms.openlocfilehash: 2cf7c569a8c8d25f89c5006be4295a980186cbe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718848"
---
# <span data-ttu-id="bb2a2-101">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb2a2-101">Backup-AzureKeyVaultKey</span></span>

## <span data-ttu-id="bb2a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="bb2a2-103">Wykonywanie kopii zapasowej klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-103">Backs up a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb2a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb2a2-104">SYNTAX</span></span>

### <span data-ttu-id="bb2a2-105">ByKeyName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bb2a2-105">ByKeyName (Default)</span></span>
```
Backup-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb2a2-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="bb2a2-106">ByKey</span></span>
```
Backup-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb2a2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bb2a2-107">DESCRIPTION</span></span>
<span data-ttu-id="bb2a2-108">Polecenie cmdlet **Backup-AzureKeyVaultKey** wykonuje kopię zapasową określonego klucza w magazynie kluczy przez pobranie go i zapisanie go w pliku.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-108">The **Backup-AzureKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="bb2a2-109">Jeśli istnieje wiele wersji klucza, wszystkie wersje są uwzględniane w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="bb2a2-110">Ponieważ pobrana zawartość jest szyfrowana, nie można jej użyć poza magazynem kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="bb2a2-111">Klucz kopii zapasowej można przywrócić w dowolnym magazynie kluczy subskrypcji, z której wykonano kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="bb2a2-112">Typowe przyczyny korzystania z tego polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="bb2a2-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="bb2a2-113">Chcesz zalogować się do kopii klucza, aby uzyskać kopię w trybie offline, na wypadek przypadkowego usunięcia klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="bb2a2-114">Utworzono klucz za pomocą magazynu kluczy, a teraz chcę sklonować klucz do innego obszaru platformy Azure, aby można go było używać we wszystkich wystąpieniach aplikacji rozproszonej.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="bb2a2-115">Użyj polecenia cmdlet **Backup-AzureKeyVaultKey** , aby pobrać klucz w zaszyfrowanej formie, a następnie użyj polecenia cmdlet Restore-AzureKeyVaultKey i określ Magazyn kluczy w drugim regionie.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-115">Use the **Backup-AzureKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzureKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="bb2a2-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb2a2-116">EXAMPLES</span></span>

### <span data-ttu-id="bb2a2-117">Przykład 1. Tworzenie kopii zapasowej klucza z automatycznie wygenerowaną nazwą pliku</span><span class="sxs-lookup"><span data-stu-id="bb2a2-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="bb2a2-118">To polecenie pobiera klucz o nazwie MyKey z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego klucza w pliku, którego nazwa jest automatycznie nazywana, i wyświetla nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="bb2a2-119">Przykład 2: wykonywanie kopii zapasowej klucza na określonej nazwie pliku</span><span class="sxs-lookup"><span data-stu-id="bb2a2-119">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="bb2a2-120">To polecenie pobiera klucz o nazwie MyKey z klucza vaultnamed MyKeyVault i zapisuje kopię zapasową tego klucza do pliku o nazwie Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="bb2a2-121">Przykład 3: wykonywanie kopii zapasowej uprzednio pobranego klucza do określonej nazwy pliku, zastępując plik docelowy bez monitowania.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzureKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="bb2a2-122">To polecenie tworzy kopię zapasową klucza o nazwie $key. Nazwa w magazynie o nazwie $key. Element magazynname do pliku o nazwie Backup. blob, w cichym zastępowaniu pliku, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="bb2a2-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb2a2-123">PARAMETERS</span></span>

### <span data-ttu-id="bb2a2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb2a2-124">-DefaultProfile</span></span>
<span data-ttu-id="bb2a2-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bb2a2-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb2a2-126">-Force</span><span class="sxs-lookup"><span data-stu-id="bb2a2-126">-Force</span></span>
<span data-ttu-id="bb2a2-127">Zastąpienie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="bb2a2-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="bb2a2-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bb2a2-128">-InputObject</span></span>
<span data-ttu-id="bb2a2-129">Kluczowy pakiet do utworzenia kopii zapasowej, który połączył się z wyników rozmowy o pobraniu.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2a2-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bb2a2-130">-Name</span></span>
<span data-ttu-id="bb2a2-131">Określa nazwę klucza, którego kopię zapasową należy wykonać.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2a2-132">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="bb2a2-132">-OutputFile</span></span>
<span data-ttu-id="bb2a2-133">Określa plik wyjściowy, w którym jest przechowywany obiekt BLOB kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="bb2a2-134">Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="bb2a2-135">Jeśli określisz nazwę istniejącego pliku wyjściowego, operacja nie zostanie ukończona i zwróci komunikat o błędzie informujący o tym, że plik kopii zapasowej już istnieje.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2a2-136">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="bb2a2-136">-VaultName</span></span>
<span data-ttu-id="bb2a2-137">Określa nazwę magazynu kluczy zawierającego klucz do utworzenia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-137">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2a2-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb2a2-138">-Confirm</span></span>
<span data-ttu-id="bb2a2-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb2a2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb2a2-140">-WhatIf</span></span>
<span data-ttu-id="bb2a2-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb2a2-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb2a2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb2a2-143">CommonParameters</span></span>
<span data-ttu-id="bb2a2-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb2a2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb2a2-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb2a2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb2a2-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb2a2-146">INPUTS</span></span>

### <span data-ttu-id="bb2a2-147">Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bb2a2-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="bb2a2-148">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bb2a2-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bb2a2-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb2a2-149">OUTPUTS</span></span>

### <span data-ttu-id="bb2a2-150">System. String</span><span class="sxs-lookup"><span data-stu-id="bb2a2-150">System.String</span></span>

## <span data-ttu-id="bb2a2-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb2a2-151">NOTES</span></span>

## <span data-ttu-id="bb2a2-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb2a2-152">RELATED LINKS</span></span>

[<span data-ttu-id="bb2a2-153">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb2a2-153">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="bb2a2-154">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb2a2-154">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="bb2a2-155">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb2a2-155">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="bb2a2-156">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb2a2-156">Restore-AzureKeyVaultKey</span></span>](./Restore-AzureKeyVaultKey.md)

