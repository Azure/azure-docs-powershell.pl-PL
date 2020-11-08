---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064066"
---
# <span data-ttu-id="c2e6a-101">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c2e6a-101">Backup-AzKeyVaultSecret</span></span>

## <span data-ttu-id="c2e6a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e6a-103">Tworzy kopię zapasową klucza tajnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-103">Backs up a secret in a key vault.</span></span>

## <span data-ttu-id="c2e6a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2e6a-104">SYNTAX</span></span>

### <span data-ttu-id="c2e6a-105">BySecretName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c2e6a-105">BySecretName (Default)</span></span>
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2e6a-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="c2e6a-106">BySecret</span></span>
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2e6a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c2e6a-107">DESCRIPTION</span></span>
<span data-ttu-id="c2e6a-108">Polecenie cmdlet **Backup-AzKeyVaultSecret** wykonuje kopię zapasową określonego klucza tajnego w magazynie kluczy, pobierając go i zapisując w pliku.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-108">The **Backup-AzKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="c2e6a-109">Jeśli istnieje wiele wersji klucza tajnego, wszystkie wersje są uwzględniane w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="c2e6a-110">Ponieważ pobrana zawartość jest szyfrowana, nie można jej użyć poza magazynem kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="c2e6a-111">Kopię zapasową klucza tajnego można przywrócić w dowolnym magazynie kluczy subskrypcji, z której wykonano kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="c2e6a-112">Typowe przyczyny korzystania z tego polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c2e6a-112">Typical reasons to use this cmdlet are:</span></span>
- <span data-ttu-id="c2e6a-113">Chcesz zalogować się do kopii klucza tajnego, aby mieć kopię w trybie offline na wypadek przypadkowego usunięcia klucza tajnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="c2e6a-114">Dodałeś klucz tajny do magazynu kluczy i chcesz teraz sklonować ten klucz tajny do innego obszaru platformy Azure, aby można go było używać we wszystkich wystąpieniach aplikacji rozproszonej.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="c2e6a-115">Użyj polecenia cmdlet Backup-AzKeyVaultSecret, aby pobrać klucz tajny w szyfrowanym formacie, a następnie użyć polecenia cmdlet Restore-AzKeyVaultSecret i określić Magazyn kluczy w drugim regionie.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-115">Use the Backup-AzKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="c2e6a-116">(Należy pamiętać, że regiony muszą należeć do tej samej geograficznej lokalizacji).</span><span class="sxs-lookup"><span data-stu-id="c2e6a-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="c2e6a-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2e6a-117">EXAMPLES</span></span>

### <span data-ttu-id="c2e6a-118">Przykład 1: wykonywanie kopii zapasowej hasła za pomocą automatycznie generowanej nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="c2e6a-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

<span data-ttu-id="c2e6a-119">To polecenie pobiera tajne imię o nazwie dbsecret z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego wpisu do pliku, którego nazwa jest automatycznie nazywana, i wyświetla nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="c2e6a-120">Przykład 2: wykonywanie kopii zapasowej hasła do określonej nazwy pliku, zastąpienie istniejącego pliku bez monitowania</span><span class="sxs-lookup"><span data-stu-id="c2e6a-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="c2e6a-121">To polecenie pobiera tajne hasło o nazwie vaultnamed MyKeyVault i zapisuje kopię zapasową tego klucza tajnego w pliku o nazwie Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="c2e6a-122">Przykład 3: wykonywanie kopii zapasowej uprzednio pobranej do określonej nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="c2e6a-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="c2e6a-123">W tym poleceniu jest używana nazwa i nazwa magazynu obiektu $secret w celu pobrania klucza tajnego i zapisu jego kopii zapasowej w pliku o nazwie Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="c2e6a-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2e6a-124">PARAMETERS</span></span>

### <span data-ttu-id="c2e6a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e6a-125">-DefaultProfile</span></span>
<span data-ttu-id="c2e6a-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c2e6a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2e6a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c2e6a-127">-Force</span></span>
<span data-ttu-id="c2e6a-128">Monituje o potwierdzenie przed zastąpieniem pliku wyjściowego, jeśli ten plik istnieje.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

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

### <span data-ttu-id="c2e6a-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2e6a-129">-InputObject</span></span>
<span data-ttu-id="c2e6a-130">Nie można utworzyć kopii zapasowej, która została przetworzona na podstawie danych wyjściowych rozmowy.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-130">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="c2e6a-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2e6a-131">-Name</span></span>
<span data-ttu-id="c2e6a-132">Określa nazwę klucza tajnego do wykonania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-132">Specifies the name of the secret to back up.</span></span>

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

### <span data-ttu-id="c2e6a-133">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="c2e6a-133">-OutputFile</span></span>
<span data-ttu-id="c2e6a-134">Określa plik wyjściowy, w którym jest przechowywany obiekt BLOB kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-134">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="c2e6a-135">Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-135">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="c2e6a-136">Jeśli określisz nazwę istniejącego pliku wyjściowego, operacja nie zostanie ukończona i zwróci komunikat o błędzie informujący o tym, że plik kopii zapasowej już istnieje.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-136">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="c2e6a-137">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="c2e6a-137">-VaultName</span></span>
<span data-ttu-id="c2e6a-138">Określa nazwę magazynu kluczy zawierającego klucz tajny do wykonania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

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

### <span data-ttu-id="c2e6a-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2e6a-139">-Confirm</span></span>
<span data-ttu-id="c2e6a-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2e6a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2e6a-141">-WhatIf</span></span>
<span data-ttu-id="c2e6a-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2e6a-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2e6a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e6a-144">CommonParameters</span></span>
<span data-ttu-id="c2e6a-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e6a-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2e6a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e6a-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2e6a-147">INPUTS</span></span>

### <span data-ttu-id="c2e6a-148">Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c2e6a-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="c2e6a-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2e6a-149">OUTPUTS</span></span>

### <span data-ttu-id="c2e6a-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c2e6a-150">System.String</span></span>

## <span data-ttu-id="c2e6a-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2e6a-151">NOTES</span></span>

## <span data-ttu-id="c2e6a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2e6a-152">RELATED LINKS</span></span>

[<span data-ttu-id="c2e6a-153">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c2e6a-153">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="c2e6a-154">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c2e6a-154">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="c2e6a-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c2e6a-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="c2e6a-156">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c2e6a-156">Restore-AzKeyVaultSecret</span></span>](./Restore-AzKeyVaultSecret.md)

