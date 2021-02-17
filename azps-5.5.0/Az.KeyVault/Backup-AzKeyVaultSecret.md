---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192395"
---
# <span data-ttu-id="151de-101">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="151de-101">Backup-AzKeyVaultSecret</span></span>

## <span data-ttu-id="151de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="151de-102">SYNOPSIS</span></span>
<span data-ttu-id="151de-103">Kopię zapasową klucza tajnego w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="151de-103">Backs up a secret in a key vault.</span></span>

## <span data-ttu-id="151de-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="151de-104">SYNTAX</span></span>

### <span data-ttu-id="151de-105">BySecretName (Default)</span><span class="sxs-lookup"><span data-stu-id="151de-105">BySecretName (Default)</span></span>
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="151de-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="151de-106">BySecret</span></span>
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="151de-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="151de-107">DESCRIPTION</span></span>
<span data-ttu-id="151de-108">Polecenie **cmdlet Backup-AzKeyVaultSecret** kopii zapasowej określonego klucza tajnego jest kopii zapasowej w magazynie kluczy, pobierając je i przechowując w pliku.</span><span class="sxs-lookup"><span data-stu-id="151de-108">The **Backup-AzKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="151de-109">Jeśli istnieje wiele wersji tajnych, wszystkie wersje są uwzględniane w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="151de-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="151de-110">Pobrana zawartość jest zaszyfrowana, więc nie można jej używać poza magazynem kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="151de-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="151de-111">Kopię zapasową klucza tajnego możesz przywrócić do dowolnego magazynu kluczy w subskrypcji, z których została wyzowana jego kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="151de-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="151de-112">Typowe powody, dla których należy używać tego polecenia cmdlet, to:</span><span class="sxs-lookup"><span data-stu-id="151de-112">Typical reasons to use this cmdlet are:</span></span>
- <span data-ttu-id="151de-113">Chcesz usunąć kopię klucza tajnego, aby mieć kopię w trybie offline na wypadek przypadkowego usunięcia klucza tajnego w twoim magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="151de-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="151de-114">Dodano klucz tajny do magazynu kluczy i teraz chcesz sklonować klucz tajny do innego regionu platformy Azure, aby można było go używać ze wszystkich wystąpień aplikacji rozproszonej.</span><span class="sxs-lookup"><span data-stu-id="151de-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="151de-115">Użyj Backup-AzKeyVaultSecret cmdlet, aby pobrać klucz tajny w zaszyfrowanym formacie, a następnie użyj polecenia cmdlet Restore-AzKeyVaultSecret i określ magazyn kluczy w drugim regionie.</span><span class="sxs-lookup"><span data-stu-id="151de-115">Use the Backup-AzKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="151de-116">(Regiony muszą należeć do tej samej lokalizacji geograficznej).</span><span class="sxs-lookup"><span data-stu-id="151de-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="151de-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="151de-117">EXAMPLES</span></span>

### <span data-ttu-id="151de-118">Przykład 1. Tworzy kopię zapasową sekretu przy użyciu automatycznie wygenerowanej nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="151de-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

<span data-ttu-id="151de-119">To polecenie pobiera klucz tajny o nazwie MySecret z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego klucza tajnego w automatycznie nazwanym pliku i wyświetla nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="151de-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="151de-120">Przykład 2. Kopię zapasową tajnego pliku o określonej nazwie pliku i nadpisanie istniejącego pliku bez monitu</span><span class="sxs-lookup"><span data-stu-id="151de-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="151de-121">To polecenie pobiera klucz tajny o nazwie MySecret z magazynu klucza o nazwie MyKeyVault i zapisuje kopię zapasową tego klucza tajnego w pliku o nazwie Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="151de-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="151de-122">Przykład 3. Kopii zapasowej poprzednio pobranej informacji tajnej do określonej nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="151de-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="151de-123">To polecenie używa nazwy i $secret magazynu obiektu w celu pobrania informacji tajnych i zapisania jego kopii zapasowej w pliku o nazwie Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="151de-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="151de-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="151de-124">PARAMETERS</span></span>

### <span data-ttu-id="151de-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="151de-125">-DefaultProfile</span></span>
<span data-ttu-id="151de-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="151de-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="151de-127">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="151de-127">-Force</span></span>
<span data-ttu-id="151de-128">Wyświetla monit o potwierdzenie przed nadpisaniem pliku wyjściowego, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="151de-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

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

### <span data-ttu-id="151de-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="151de-129">-InputObject</span></span>
<span data-ttu-id="151de-130">Tajna, aby można było wrócić do kopii zapasowej, potokowana z danych wyjściowych połączenia pobierania.</span><span class="sxs-lookup"><span data-stu-id="151de-130">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="151de-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="151de-131">-Name</span></span>
<span data-ttu-id="151de-132">Określa nazwę tajnych kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="151de-132">Specifies the name of the secret to back up.</span></span>

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

### <span data-ttu-id="151de-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="151de-133">-OutputFile</span></span>
<span data-ttu-id="151de-134">Określa plik wyjściowy, w którym jest przechowywany obiekt blob kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="151de-134">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="151de-135">Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="151de-135">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="151de-136">Jeśli określisz nazwę istniejącego pliku wyjściowego, operacja nie zostanie ukończona i zostanie wyświetlony komunikat o błędzie informujący, że plik kopii zapasowej już istnieje.</span><span class="sxs-lookup"><span data-stu-id="151de-136">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="151de-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="151de-137">-VaultName</span></span>
<span data-ttu-id="151de-138">Określa nazwę magazynu kluczy zawierającego klucz tajny, który ma być kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="151de-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

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

### <span data-ttu-id="151de-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="151de-139">-Confirm</span></span>
<span data-ttu-id="151de-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="151de-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="151de-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="151de-141">-WhatIf</span></span>
<span data-ttu-id="151de-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="151de-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="151de-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="151de-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="151de-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="151de-144">CommonParameters</span></span>
<span data-ttu-id="151de-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="151de-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="151de-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="151de-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="151de-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="151de-147">INPUTS</span></span>

### <span data-ttu-id="151de-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="151de-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="151de-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="151de-149">OUTPUTS</span></span>

### <span data-ttu-id="151de-150">System.String</span><span class="sxs-lookup"><span data-stu-id="151de-150">System.String</span></span>

## <span data-ttu-id="151de-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="151de-151">NOTES</span></span>

## <span data-ttu-id="151de-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="151de-152">RELATED LINKS</span></span>

[<span data-ttu-id="151de-153">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="151de-153">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="151de-154">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="151de-154">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="151de-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="151de-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="151de-156">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="151de-156">Restore-AzKeyVaultSecret</span></span>](./Restore-AzKeyVaultSecret.md)

