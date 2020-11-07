---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
ms.openlocfilehash: 6021e9c4c3be3ac4eb2721684b9f94463e1b69af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719420"
---
# <span data-ttu-id="2a327-101">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2a327-101">Backup-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="2a327-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a327-102">SYNOPSIS</span></span>
<span data-ttu-id="2a327-103">Tworzy kopię zapasową klucza tajnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="2a327-103">Backs up a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a327-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a327-104">SYNTAX</span></span>

### <span data-ttu-id="2a327-105">BySecretName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2a327-105">BySecretName (Default)</span></span>
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a327-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="2a327-106">BySecret</span></span>
```
Backup-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a327-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2a327-107">DESCRIPTION</span></span>
<span data-ttu-id="2a327-108">Polecenie cmdlet **Backup-AzureKeyVaultSecret** wykonuje kopię zapasową określonego klucza tajnego w magazynie kluczy, pobierając go i zapisując w pliku.</span><span class="sxs-lookup"><span data-stu-id="2a327-108">The **Backup-AzureKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="2a327-109">Jeśli istnieje wiele wersji klucza tajnego, wszystkie wersje są uwzględniane w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2a327-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="2a327-110">Ponieważ pobrana zawartość jest szyfrowana, nie można jej użyć poza magazynem kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2a327-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="2a327-111">Kopię zapasową klucza tajnego można przywrócić w dowolnym magazynie kluczy subskrypcji, z której wykonano kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="2a327-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="2a327-112">Typowe przyczyny korzystania z tego polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2a327-112">Typical reasons to use this cmdlet are:</span></span>
- <span data-ttu-id="2a327-113">Chcesz zalogować się do kopii klucza tajnego, aby mieć kopię w trybie offline na wypadek przypadkowego usunięcia klucza tajnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="2a327-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="2a327-114">Dodałeś klucz tajny do magazynu kluczy i chcesz teraz sklonować ten klucz tajny do innego obszaru platformy Azure, aby można go było używać we wszystkich wystąpieniach aplikacji rozproszonej.</span><span class="sxs-lookup"><span data-stu-id="2a327-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="2a327-115">Użyj polecenia cmdlet Backup-AzureKeyVaultSecret, aby pobrać klucz tajny w szyfrowanym formacie, a następnie użyć polecenia cmdlet Restore-AzureKeyVaultSecret i określić Magazyn kluczy w drugim regionie.</span><span class="sxs-lookup"><span data-stu-id="2a327-115">Use the Backup-AzureKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzureKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="2a327-116">(Należy pamiętać, że regiony muszą należeć do tej samej geograficznej lokalizacji).</span><span class="sxs-lookup"><span data-stu-id="2a327-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="2a327-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a327-117">EXAMPLES</span></span>

### <span data-ttu-id="2a327-118">Przykład 1: wykonywanie kopii zapasowej hasła za pomocą automatycznie generowanej nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="2a327-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

<span data-ttu-id="2a327-119">To polecenie pobiera tajne imię o nazwie dbsecret z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego wpisu do pliku, którego nazwa jest automatycznie nazywana, i wyświetla nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="2a327-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="2a327-120">Przykład 2: wykonywanie kopii zapasowej hasła do określonej nazwy pliku, zastąpienie istniejącego pliku bez monitowania</span><span class="sxs-lookup"><span data-stu-id="2a327-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="2a327-121">To polecenie pobiera tajne hasło o nazwie vaultnamed MyKeyVault i zapisuje kopię zapasową tego klucza tajnego w pliku o nazwie Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="2a327-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="2a327-122">Przykład 3: wykonywanie kopii zapasowej uprzednio pobranej do określonej nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="2a327-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```powershell
PS C:\> $secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="2a327-123">W tym poleceniu jest używana nazwa i nazwa magazynu obiektu $secret w celu pobrania klucza tajnego i zapisu jego kopii zapasowej w pliku o nazwie Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="2a327-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="2a327-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a327-124">PARAMETERS</span></span>

### <span data-ttu-id="2a327-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a327-125">-DefaultProfile</span></span>
<span data-ttu-id="2a327-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2a327-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a327-127">-Force</span><span class="sxs-lookup"><span data-stu-id="2a327-127">-Force</span></span>
<span data-ttu-id="2a327-128">Monituje o potwierdzenie przed zastąpieniem pliku wyjściowego, jeśli ten plik istnieje.</span><span class="sxs-lookup"><span data-stu-id="2a327-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a327-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2a327-129">-InputObject</span></span>
<span data-ttu-id="2a327-130">Nie można utworzyć kopii zapasowej, która została przetworzona na podstawie danych wyjściowych rozmowy.</span><span class="sxs-lookup"><span data-stu-id="2a327-130">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a327-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a327-131">-Name</span></span>
<span data-ttu-id="2a327-132">Określa nazwę klucza tajnego do wykonania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2a327-132">Specifies the name of the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a327-133">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="2a327-133">-OutputFile</span></span>
<span data-ttu-id="2a327-134">Określa plik wyjściowy, w którym jest przechowywany obiekt BLOB kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2a327-134">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="2a327-135">Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="2a327-135">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="2a327-136">Jeśli określisz nazwę istniejącego pliku wyjściowego, operacja nie zostanie ukończona i zwróci komunikat o błędzie informujący o tym, że plik kopii zapasowej już istnieje.</span><span class="sxs-lookup"><span data-stu-id="2a327-136">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="2a327-137">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="2a327-137">-VaultName</span></span>
<span data-ttu-id="2a327-138">Określa nazwę magazynu kluczy zawierającego klucz tajny do wykonania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2a327-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a327-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a327-139">-Confirm</span></span>
<span data-ttu-id="2a327-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a327-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a327-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a327-141">-WhatIf</span></span>
<span data-ttu-id="2a327-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a327-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a327-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a327-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a327-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a327-144">CommonParameters</span></span>
<span data-ttu-id="2a327-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a327-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a327-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a327-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a327-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a327-147">INPUTS</span></span>

### <span data-ttu-id="2a327-148">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="2a327-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="2a327-149">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2a327-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2a327-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a327-150">OUTPUTS</span></span>

### <span data-ttu-id="2a327-151">System. String</span><span class="sxs-lookup"><span data-stu-id="2a327-151">System.String</span></span>

## <span data-ttu-id="2a327-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a327-152">NOTES</span></span>

## <span data-ttu-id="2a327-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a327-153">RELATED LINKS</span></span>

[<span data-ttu-id="2a327-154">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2a327-154">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="2a327-155">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2a327-155">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="2a327-156">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2a327-156">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="2a327-157">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2a327-157">Restore-AzureKeyVaultSecret</span></span>](./Restore-AzureKeyVaultSecret.md)
