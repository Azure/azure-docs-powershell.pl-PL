---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 75f5e487c7cb1d434d12d6c02122991195c01066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991145"
---
# <span data-ttu-id="d0b36-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d0b36-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d0b36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0b36-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b36-103">Kopii zapasowej konta magazynu zarządzanego przez usługę KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d0b36-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="d0b36-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d0b36-104">SYNTAX</span></span>

### <span data-ttu-id="d0b36-105">ByStorageAccountName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="d0b36-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0b36-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d0b36-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0b36-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d0b36-107">DESCRIPTION</span></span>
<span data-ttu-id="d0b36-108">Polecenie **cmdlet Backup-AzKeyVaultManagedStorageAccount** kopii zapasowej określonego zarządzanego konta magazynu w magazynie kluczy przez pobranie go i przechowywanie w pliku.</span><span class="sxs-lookup"><span data-stu-id="d0b36-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="d0b36-109">Pobrana zawartość jest zaszyfrowana, więc nie można jej używać poza magazynem kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0b36-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="d0b36-110">Możesz przywrócić kopię zapasową konta magazynu do dowolnego magazynu kluczy w subskrypcji, z których została ona zbędna, o ile magazyn znajduje się w tej samej lokalizacji geograficznej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0b36-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="d0b36-111">Typowe powody, dla których należy używać tego polecenia cmdlet, to:</span><span class="sxs-lookup"><span data-stu-id="d0b36-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="d0b36-112">Chcesz zachować kopię offline konta magazynu na wypadek przypadkowego usunięcia oryginału z magazynu.</span><span class="sxs-lookup"><span data-stu-id="d0b36-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="d0b36-113">Utworzono konto magazynu zarządzanego przy użyciu magazynu kluczy, a teraz chcesz sklonować obiekt w inny region platformy Azure, aby można było używać go ze wszystkich wystąpień aplikacji rozproszonej.</span><span class="sxs-lookup"><span data-stu-id="d0b36-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="d0b36-114">Użyj polecenia cmdlet **Backup-AzKeyVaultManagedStorageAccount,** aby pobrać konto magazynu zarządzanego w postaci zaszyfrowanej, a następnie użyj polecenia cmdlet **Restore-AzKeyVaultManagedStorageAccount** i określ magazyn kluczy w drugim regionie.</span><span class="sxs-lookup"><span data-stu-id="d0b36-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="d0b36-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d0b36-115">EXAMPLES</span></span>

### <span data-ttu-id="d0b36-116">Przykład 1. Tworzy kopię zapasową zarządzanego konta magazynu z automatycznie wygenerowaną nazwą pliku</span><span class="sxs-lookup"><span data-stu-id="d0b36-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="d0b36-117">To polecenie pobiera konto magazynu zarządzanego o nazwie MyMSAK z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego zarządzanego konta magazynu w pliku, który jest automatycznie nazwany dla Ciebie, i wyświetla nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="d0b36-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="d0b36-118">Przykład 2. Kopii zapasowej zarządzanego konta magazynu pod określoną nazwą pliku</span><span class="sxs-lookup"><span data-stu-id="d0b36-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="d0b36-119">To polecenie pobiera konto magazynu zarządzanego o nazwie MyMSAK z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego zarządzanego konta magazynu w pliku o nazwie Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="d0b36-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="d0b36-120">Przykład 3. Kopię zapasową poprzednio pobranego zarządzanego konta magazynu pod określoną nazwą pliku i nadpisanie pliku docelowego bez monitu.</span><span class="sxs-lookup"><span data-stu-id="d0b36-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="d0b36-121">To polecenie tworzy kopię zapasową zarządzanego konta magazynu o nazwie $msak. Nazwa w magazynie o nazwie $msak. Nazwa magazynu do pliku o nazwie Backup.blob, bezgłośnie nadpisując plik, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="d0b36-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="d0b36-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0b36-122">PARAMETERS</span></span>

### <span data-ttu-id="d0b36-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b36-123">-DefaultProfile</span></span>
<span data-ttu-id="d0b36-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0b36-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0b36-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d0b36-125">-Force</span></span>
<span data-ttu-id="d0b36-126">Zastępowanie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="d0b36-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="d0b36-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0b36-127">-InputObject</span></span>
<span data-ttu-id="d0b36-128">Pakiet konta magazynu, który ma zostać kopii zapasowej, potokowany z danych wyjściowych połączenia pobierania.</span><span class="sxs-lookup"><span data-stu-id="d0b36-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b36-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d0b36-129">-Name</span></span>
<span data-ttu-id="d0b36-130">Tajna nazwa.</span><span class="sxs-lookup"><span data-stu-id="d0b36-130">Secret name.</span></span>
<span data-ttu-id="d0b36-131">Polecenie cmdlet konstruuje nazwę FQDN tajemnicy przed nazwą magazynu, obecnie wybranym środowiskiem i nazwą tajną.</span><span class="sxs-lookup"><span data-stu-id="d0b36-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b36-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="d0b36-132">-OutputFile</span></span>
<span data-ttu-id="d0b36-133">Plik wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="d0b36-133">Output file.</span></span>
<span data-ttu-id="d0b36-134">Plik wyjściowy do przechowywania kopii zapasowej konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d0b36-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="d0b36-135">Jeśli nie zostanie określona, zostanie wygenerowana domyślna nazwa pliku.</span><span class="sxs-lookup"><span data-stu-id="d0b36-135">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="d0b36-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d0b36-136">-VaultName</span></span>
<span data-ttu-id="d0b36-137">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="d0b36-137">Vault name.</span></span>
<span data-ttu-id="d0b36-138">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="d0b36-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b36-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0b36-139">-Confirm</span></span>
<span data-ttu-id="d0b36-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d0b36-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0b36-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0b36-141">-WhatIf</span></span>
<span data-ttu-id="d0b36-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0b36-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0b36-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d0b36-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0b36-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b36-144">CommonParameters</span></span>
<span data-ttu-id="d0b36-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0b36-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b36-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0b36-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b36-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0b36-147">INPUTS</span></span>

### <span data-ttu-id="d0b36-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d0b36-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="d0b36-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0b36-149">OUTPUTS</span></span>

### <span data-ttu-id="d0b36-150">System.String</span><span class="sxs-lookup"><span data-stu-id="d0b36-150">System.String</span></span>

## <span data-ttu-id="d0b36-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d0b36-151">NOTES</span></span>

## <span data-ttu-id="d0b36-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0b36-152">RELATED LINKS</span></span>
