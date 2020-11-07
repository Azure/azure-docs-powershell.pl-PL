---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: bf1441c62287e786b0c71e705a0b340e5c51f424
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868007"
---
# <span data-ttu-id="ea91b-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea91b-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ea91b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea91b-102">SYNOPSIS</span></span>
<span data-ttu-id="ea91b-103">Wykonywanie kopii zapasowej konta magazynu zarządzanego przez magazyny.</span><span class="sxs-lookup"><span data-stu-id="ea91b-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="ea91b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea91b-104">SYNTAX</span></span>

### <span data-ttu-id="ea91b-105">ByStorageAccountName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea91b-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea91b-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea91b-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea91b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ea91b-107">DESCRIPTION</span></span>
<span data-ttu-id="ea91b-108">Polecenie cmdlet **Backup-AzKeyVaultManagedStorageAccount** wykonuje kopię zapasową określonego zarządzanego konta magazynu w magazynie kluczy przez pobranie go i zapisanie go w pliku.</span><span class="sxs-lookup"><span data-stu-id="ea91b-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="ea91b-109">Ponieważ pobrana zawartość jest szyfrowana, nie można jej użyć poza magazynem kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ea91b-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="ea91b-110">Możesz przywrócić kopię zapasową konta magazynu do dowolnego magazynu kluczy w subskrypcji, z której wykonano kopię zapasową, o ile magazyn jest w tej samej geograficznej platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ea91b-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="ea91b-111">Typowe przyczyny korzystania z tego polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ea91b-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="ea91b-112">Chcesz zachować kopię w trybie offline konta magazynu na wypadek, gdyby przypadkowo usunął oryginalny z magazynu.</span><span class="sxs-lookup"><span data-stu-id="ea91b-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="ea91b-113">Utworzono zarządzane konto magazynu za pomocą magazynu kluczy i chcesz teraz sklonować obiekt do innego obszaru platformy Azure, aby można go było używać we wszystkich wystąpieniach aplikacji rozproszonej.</span><span class="sxs-lookup"><span data-stu-id="ea91b-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="ea91b-114">Użyj polecenia cmdlet **Backup-AzKeyVaultManagedStorageAccount** , aby pobrać zarządzane konto magazynu w zaszyfrowanej postaci, a następnie użyj polecenia cmdlet **Restore-AzKeyVaultManagedStorageAccount** i określ Magazyn kluczy w drugim regionie.</span><span class="sxs-lookup"><span data-stu-id="ea91b-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="ea91b-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea91b-115">EXAMPLES</span></span>

### <span data-ttu-id="ea91b-116">Przykład 1: wykonywanie kopii zapasowej zarządzanego konta magazynu z automatycznie wygenerowaną nazwą pliku</span><span class="sxs-lookup"><span data-stu-id="ea91b-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="ea91b-117">To polecenie pobiera zarządzane konto magazynu o nazwie MyMSAK z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego konta zarządzanego magazynu do pliku, którego nazwa jest automatycznie nazywana, i wyświetla nazwę pliku.</span><span class="sxs-lookup"><span data-stu-id="ea91b-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="ea91b-118">Przykład 2: wykonywanie kopii zapasowej zarządzanego konta magazynu pod określoną nazwą pliku</span><span class="sxs-lookup"><span data-stu-id="ea91b-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="ea91b-119">To polecenie pobiera zarządzane konto magazynu o nazwie MyMSAK z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego konta zarządzanego magazynu do pliku o nazwie Backup. blob.</span><span class="sxs-lookup"><span data-stu-id="ea91b-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="ea91b-120">Przykład 3: wykonywanie kopii zapasowej uprzednio pobranego konta zarządzanego magazynu do określonej nazwy pliku, zastępując plik docelowy bez monitowania.</span><span class="sxs-lookup"><span data-stu-id="ea91b-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="ea91b-121">To polecenie tworzy kopię zapasową zarządzanego konta magazynu o nazwie $msak. Nazwa w magazynie o nazwie $msak. Element magazynname do pliku o nazwie Backup. blob, w cichym zastępowaniu pliku, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="ea91b-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="ea91b-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea91b-122">PARAMETERS</span></span>

### <span data-ttu-id="ea91b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea91b-123">-DefaultProfile</span></span>
<span data-ttu-id="ea91b-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea91b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea91b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ea91b-125">-Force</span></span>
<span data-ttu-id="ea91b-126">Zastąpienie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="ea91b-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="ea91b-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ea91b-127">-InputObject</span></span>
<span data-ttu-id="ea91b-128">Pakiet kont magazynu, którego kopia zapasowa jest planowana, przeprowadzonym na podstawie danych wyjściowych rozmowy.</span><span class="sxs-lookup"><span data-stu-id="ea91b-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="ea91b-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea91b-129">-Name</span></span>
<span data-ttu-id="ea91b-130">Nazwa tajna.</span><span class="sxs-lookup"><span data-stu-id="ea91b-130">Secret name.</span></span>
<span data-ttu-id="ea91b-131">Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i sekretu.</span><span class="sxs-lookup"><span data-stu-id="ea91b-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="ea91b-132">-Plik_wyjściowy</span><span class="sxs-lookup"><span data-stu-id="ea91b-132">-OutputFile</span></span>
<span data-ttu-id="ea91b-133">Plik wyjściowy.</span><span class="sxs-lookup"><span data-stu-id="ea91b-133">Output file.</span></span>
<span data-ttu-id="ea91b-134">Plik wyjściowy do przechowywania kopii zapasowej konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ea91b-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="ea91b-135">Jeśli nie podano tego parametru, zostanie wygenerowana domyślna nazwa pliku.</span><span class="sxs-lookup"><span data-stu-id="ea91b-135">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="ea91b-136">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="ea91b-136">-VaultName</span></span>
<span data-ttu-id="ea91b-137">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="ea91b-137">Vault name.</span></span>
<span data-ttu-id="ea91b-138">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="ea91b-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ea91b-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea91b-139">-Confirm</span></span>
<span data-ttu-id="ea91b-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea91b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea91b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea91b-141">-WhatIf</span></span>
<span data-ttu-id="ea91b-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea91b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea91b-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea91b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea91b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea91b-144">CommonParameters</span></span>
<span data-ttu-id="ea91b-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea91b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea91b-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea91b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea91b-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea91b-147">INPUTS</span></span>

### <span data-ttu-id="ea91b-148">Microsoft. Azure. Commands. platforming. models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ea91b-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="ea91b-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea91b-149">OUTPUTS</span></span>

### <span data-ttu-id="ea91b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ea91b-150">System.String</span></span>

## <span data-ttu-id="ea91b-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea91b-151">NOTES</span></span>

## <span data-ttu-id="ea91b-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea91b-152">RELATED LINKS</span></span>
