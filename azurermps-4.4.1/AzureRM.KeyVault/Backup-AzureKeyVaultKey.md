---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://go.microsoft.com/fwlink/?LinkId=690296
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
ms.openlocfilehash: f6d6b362a93897dc854170b8cbbbfd228b305abc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719641"
---
# <span data-ttu-id="e7d4f-101">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e7d4f-101">Backup-AzureKeyVaultKey</span></span>

## <span data-ttu-id="e7d4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d4f-103">Wykonywanie kopii zapasowej klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-103">Backs up a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7d4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7d4f-104">SYNTAX</span></span>

### <span data-ttu-id="e7d4f-105">ByKeyName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e7d4f-105">ByKeyName (Default)</span></span>
```
Backup-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7d4f-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="e7d4f-106">ByKey</span></span>
```
Backup-AzureKeyVaultKey [-Key] <KeyBundle> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7d4f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e7d4f-107">DESCRIPTION</span></span>
<span data-ttu-id="e7d4f-108">Polecenie cmdlet **Backup-AzureKeyVaultKey** wykonuje kopię zapasową określonego klucza w magazynie kluczy przez pobranie go i zapisanie go w pliku.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-108">The **Backup-AzureKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="e7d4f-109">Jeśli istnieje wiele wersji klucza, wszystkie wersje są uwzględniane w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="e7d4f-110">Ponieważ pobrana zawartość jest szyfrowana, nie można jej użyć poza magazynem kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="e7d4f-111">Klucz kopii zapasowej można przywrócić w dowolnym magazynie kluczy subskrypcji, z której wykonano kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="e7d4f-112">Typowe przyczyny korzystania z tego polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e7d4f-112">Typical reasons to use this cmdlet are:</span></span> 

- <span data-ttu-id="e7d4f-113">Chcesz zalogować się do kopii klucza, aby uzyskać kopię w trybie offline, na wypadek przypadkowego usunięcia klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="e7d4f-114">Utworzono klucz za pomocą magazynu kluczy, a teraz chcę sklonować klucz do innego obszaru platformy Azure, aby można go było używać we wszystkich wystąpieniach aplikacji rozproszonej.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="e7d4f-115">Użyj polecenia cmdlet **Backup-AzureKeyVaultKey** , aby pobrać klucz w zaszyfrowanej formie, a następnie użyj polecenia cmdlet Restore-AzureKeyVaultKey i określ Magazyn kluczy w drugim regionie.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-115">Use the **Backup-AzureKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzureKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="e7d4f-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7d4f-116">EXAMPLES</span></span>

### <span data-ttu-id="e7d4f-117">Przykład 1. Tworzenie kopii zapasowej klucza z automatycznie wygenerowaną nazwą pliku</span><span class="sxs-lookup"><span data-stu-id="e7d4f-117">Example 1: Back up a key with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="e7d4f-118">To polecenie pobiera klucz o nazwie MyKey z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego klucza w pliku, którego nazwa jest automatycznie nazywana, i wyświetla nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="e7d4f-119">Przykład 2: wykonywanie kopii zapasowej klucza na określonej nazwie pliku</span><span class="sxs-lookup"><span data-stu-id="e7d4f-119">Example 2: Back up a key to a specified file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="e7d4f-120">To polecenie pobiera klucz o nazwie MyKey z klucza vaultnamed MyKeyVault i zapisuje kopię zapasową tego klucza do pliku o nazwie Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="e7d4f-121">Przykład 3: wykonywanie kopii zapasowej uprzednio pobranego klucza do określonej nazwy pliku, zastępując plik docelowy bez monitowania.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```
PS C:\>$key = Get-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzureKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="e7d4f-122">To polecenie tworzy kopię zapasową klucza o nazwie $key. Nazwa w magazynie o nazwie $key. Element magazynname do pliku o nazwie Backup. blob, w cichym zastępowaniu pliku, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="e7d4f-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7d4f-123">PARAMETERS</span></span>

### <span data-ttu-id="e7d4f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e7d4f-124">-Force</span></span>
<span data-ttu-id="e7d4f-125">Zastąpienie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="e7d4f-125">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d4f-126">-Key</span><span class="sxs-lookup"><span data-stu-id="e7d4f-126">-Key</span></span>
<span data-ttu-id="e7d4f-127">Określa poprzednio pobrany klucz, którego kopię zapasową należy wykonać.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-127">Specifies a previously retrieved key which is to be backed up.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyBundle
Parameter Sets: ByKey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d4f-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7d4f-128">-Name</span></span>
<span data-ttu-id="e7d4f-129">Określa nazwę klucza, którego kopię zapasową należy wykonać.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-129">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d4f-130">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="e7d4f-130">-OutputFile</span></span>
<span data-ttu-id="e7d4f-131">Określa plik wyjściowy, w którym jest przechowywany obiekt BLOB kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-131">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="e7d4f-132">Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-132">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="e7d4f-133">Jeśli określisz nazwę istniejącego pliku wyjściowego, operacja nie zostanie ukończona i zwróci komunikat o błędzie informujący o tym, że plik kopii zapasowej już istnieje.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-133">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d4f-134">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="e7d4f-134">-VaultName</span></span>
<span data-ttu-id="e7d4f-135">Określa nazwę magazynu kluczy zawierającego klucz do utworzenia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-135">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d4f-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7d4f-136">-Confirm</span></span>
<span data-ttu-id="e7d4f-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7d4f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d4f-138">-WhatIf</span></span>
<span data-ttu-id="e7d4f-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7d4f-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7d4f-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d4f-141">-DefaultProfile</span></span>
<span data-ttu-id="e7d4f-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7d4f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d4f-143">CommonParameters</span></span>
<span data-ttu-id="e7d4f-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d4f-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7d4f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d4f-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7d4f-146">INPUTS</span></span>

## <span data-ttu-id="e7d4f-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7d4f-147">OUTPUTS</span></span>

### <span data-ttu-id="e7d4f-148">Ciąg</span><span class="sxs-lookup"><span data-stu-id="e7d4f-148">String</span></span>
<span data-ttu-id="e7d4f-149">Polecenie cmdlet zwraca ścieżkę pliku wyjściowego zawierającego kopię zapasową klucza.</span><span class="sxs-lookup"><span data-stu-id="e7d4f-149">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="e7d4f-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7d4f-150">NOTES</span></span>

## <span data-ttu-id="e7d4f-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7d4f-151">RELATED LINKS</span></span>

[<span data-ttu-id="e7d4f-152">Dodaj-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e7d4f-152">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="e7d4f-153">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e7d4f-153">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="e7d4f-154">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e7d4f-154">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="e7d4f-155">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e7d4f-155">Restore-AzureKeyVaultKey</span></span>](./Restore-AzureKeyVaultKey.md)

