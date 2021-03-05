---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 3123d0fa188e0e9a4c419ceaa567969fc3a2f8b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977018"
---
# <span data-ttu-id="0f23e-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0f23e-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="0f23e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f23e-102">SYNOPSIS</span></span>
<span data-ttu-id="0f23e-103">Kopię zapasową klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="0f23e-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="0f23e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0f23e-104">SYNTAX</span></span>

### <span data-ttu-id="0f23e-105">ByKeyName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="0f23e-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f23e-106">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="0f23e-106">HsmByKeyName</span></span>
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f23e-107">ByKey</span><span class="sxs-lookup"><span data-stu-id="0f23e-107">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f23e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0f23e-108">DESCRIPTION</span></span>
<span data-ttu-id="0f23e-109">Polecenie **cmdlet Backup-AzKeyVaultKey** kopii zapasowej określonego klucza w magazynie kluczy, pobierając go i przechowując w pliku.</span><span class="sxs-lookup"><span data-stu-id="0f23e-109">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="0f23e-110">Jeśli istnieje wiele wersji klucza, wszystkie wersje są uwzględniane w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0f23e-110">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="0f23e-111">Pobrana zawartość jest zaszyfrowana, więc nie można jej używać poza magazynem kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0f23e-111">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="0f23e-112">Możesz przywrócić klucz kopii zapasowej do dowolnego magazynu kluczy w subskrypcji, z których została utworzyć kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="0f23e-112">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="0f23e-113">Typowe powody, dla których należy używać tego polecenia cmdlet, to:</span><span class="sxs-lookup"><span data-stu-id="0f23e-113">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="0f23e-114">Chcesz usunąć kopię klucza, aby mieć kopię w trybie offline na wypadek przypadkowego usunięcia klucza w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="0f23e-114">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="0f23e-115">Klucz został utworzony przy użyciu magazynu kluczy, a teraz chcesz go sklonować w innym regionie platformy Azure, aby można było go używać ze wszystkich wystąpień aplikacji rozproszonej.</span><span class="sxs-lookup"><span data-stu-id="0f23e-115">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="0f23e-116">Użyj polecenia cmdlet **Backup-AzKeyVaultKey,** aby pobrać klucz w postaci zaszyfrowanej, a następnie użyj polecenia cmdlet Restore-AzKeyVaultKey i określ magazyn kluczy w drugim regionie.</span><span class="sxs-lookup"><span data-stu-id="0f23e-116">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="0f23e-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0f23e-117">EXAMPLES</span></span>

### <span data-ttu-id="0f23e-118">Przykład 1. Tworzy kopię zapasową klucza z automatycznie wygenerowaną nazwą pliku</span><span class="sxs-lookup"><span data-stu-id="0f23e-118">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="0f23e-119">To polecenie pobiera klucz o nazwie MyKey z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego klucza w pliku, który jest automatycznie nazwany dla Ciebie, i wyświetla nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="0f23e-119">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="0f23e-120">Przykład 2. Kopii zapasowej klucza pod określoną nazwą pliku</span><span class="sxs-lookup"><span data-stu-id="0f23e-120">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="0f23e-121">To polecenie pobiera klucz o nazwie MyKey z klucza o nazwie MyKeyVault i zapisuje kopię zapasową tego klucza w pliku o nazwie Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="0f23e-121">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="0f23e-122">Przykład 3. Kopię zapasową poprzednio pobranego klucza do określonej nazwy pliku i nadpisanie pliku docelowego bez monitu.</span><span class="sxs-lookup"><span data-stu-id="0f23e-122">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="0f23e-123">To polecenie tworzy kopię zapasową klucza o nazwie $key. Nazwa w magazynie o nazwie $key. Nazwa magazynu do pliku o nazwie Backup.blob, bezgłośnie nadpisując plik, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="0f23e-123">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="0f23e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f23e-124">PARAMETERS</span></span>

### <span data-ttu-id="0f23e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f23e-125">-DefaultProfile</span></span>
<span data-ttu-id="0f23e-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0f23e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f23e-127">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0f23e-127">-Force</span></span>
<span data-ttu-id="0f23e-128">Zastępowanie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="0f23e-128">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="0f23e-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="0f23e-129">-HsmName</span></span>
<span data-ttu-id="0f23e-130">Nazwa HSM.</span><span class="sxs-lookup"><span data-stu-id="0f23e-130">HSM name.</span></span> <span data-ttu-id="0f23e-131">Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="0f23e-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f23e-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f23e-132">-InputObject</span></span>
<span data-ttu-id="0f23e-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span><span class="sxs-lookup"><span data-stu-id="0f23e-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="0f23e-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0f23e-134">-Name</span></span>
<span data-ttu-id="0f23e-135">Określa nazwę klucza do kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0f23e-135">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f23e-136">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="0f23e-136">-OutputFile</span></span>
<span data-ttu-id="0f23e-137">Określa plik wyjściowy, w którym jest przechowywany obiekt blob kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0f23e-137">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="0f23e-138">Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="0f23e-138">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="0f23e-139">Jeśli określisz nazwę istniejącego pliku wyjściowego, operacja nie zostanie ukończona i zostanie wyświetlony komunikat o błędzie informujący, że plik kopii zapasowej już istnieje.</span><span class="sxs-lookup"><span data-stu-id="0f23e-139">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="0f23e-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0f23e-140">-VaultName</span></span>
<span data-ttu-id="0f23e-141">Określa nazwę magazynu kluczy zawierającego klucz do kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0f23e-141">Specifies the name of the key vault that contains the key to back up.</span></span>

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

### <span data-ttu-id="0f23e-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f23e-142">-Confirm</span></span>
<span data-ttu-id="0f23e-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0f23e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f23e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f23e-144">-WhatIf</span></span>
<span data-ttu-id="0f23e-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f23e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f23e-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0f23e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f23e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f23e-147">CommonParameters</span></span>
<span data-ttu-id="0f23e-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f23e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f23e-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f23e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f23e-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f23e-150">INPUTS</span></span>

### <span data-ttu-id="0f23e-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0f23e-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="0f23e-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f23e-152">OUTPUTS</span></span>

### <span data-ttu-id="0f23e-153">System.String</span><span class="sxs-lookup"><span data-stu-id="0f23e-153">System.String</span></span>

## <span data-ttu-id="0f23e-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0f23e-154">NOTES</span></span>

## <span data-ttu-id="0f23e-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f23e-155">RELATED LINKS</span></span>

[<span data-ttu-id="0f23e-156">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0f23e-156">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="0f23e-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0f23e-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="0f23e-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0f23e-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="0f23e-159">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0f23e-159">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

