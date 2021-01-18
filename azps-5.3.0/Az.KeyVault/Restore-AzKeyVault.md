---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: d1cf3757596a56336c25c46bd6c4e38687888d6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499046"
---
# <span data-ttu-id="7f8f3-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7f8f3-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="7f8f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="7f8f3-103">Umożliwia całkowite przywrócenie zarządzanego modułu HSM z kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="7f8f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f8f3-104">SYNTAX</span></span>

### <span data-ttu-id="7f8f3-105">InteractiveStorageName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7f8f3-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f8f3-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="7f8f3-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageContainerUri <Uri> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f8f3-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="7f8f3-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageContainerUri <Uri>
 -SasToken <SecureString> -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f8f3-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="7f8f3-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f8f3-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7f8f3-109">DESCRIPTION</span></span>
<span data-ttu-id="7f8f3-110">Umożliwia całkowite przywrócenie zarządzanego modułu HSM z kopii zapasowej przechowywanej na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="7f8f3-111">Użyj `Backup-AzKeyVault` do wykonania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="7f8f3-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f8f3-112">EXAMPLES</span></span>

### <span data-ttu-id="7f8f3-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f8f3-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="7f8f3-114">Przykład przywraca kopię zapasową przechowywaną w folderze o nazwie "mhsm-myHsm-2020101308504935" kontenera magazynu "https://{AccountName}. blob. Core. Windows. NET/{ContainerName}".</span><span class="sxs-lookup"><span data-stu-id="7f8f3-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="7f8f3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f8f3-115">PARAMETERS</span></span>

### <span data-ttu-id="7f8f3-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="7f8f3-116">-BackupFolder</span></span>
<span data-ttu-id="7f8f3-117">Nazwa folderu kopii zapasowej, na przykład "mhsm-*-2020101309020403". Można go również zagnieżdżać, na przykład "kopia zapasowa/mhsm-*-2020101309020403".</span><span class="sxs-lookup"><span data-stu-id="7f8f3-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f8f3-118">-DefaultProfile</span></span>
<span data-ttu-id="7f8f3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f8f3-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="7f8f3-120">-HsmName</span></span>
<span data-ttu-id="7f8f3-121">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-121">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="7f8f3-122">-HsmObject</span></span>
<span data-ttu-id="7f8f3-123">Obiekt Managed HSM</span><span class="sxs-lookup"><span data-stu-id="7f8f3-123">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-124">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="7f8f3-124">-KeyName</span></span>
<span data-ttu-id="7f8f3-125">Nazwa klucza do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-125">Key name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f8f3-126">-PassThru</span></span>
<span data-ttu-id="7f8f3-127">Zwraca wartość true, gdy HSM jest przywracany.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-127">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="7f8f3-128">-SasToken</span><span class="sxs-lookup"><span data-stu-id="7f8f3-128">-SasToken</span></span>
<span data-ttu-id="7f8f3-129">Token dostępu współdzielonego (SAS, Access Signature) umożliwiający uwierzytelnienie konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-129">The shared access signature (SAS) token to authenticate the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7f8f3-130">-StorageAccountName</span></span>
<span data-ttu-id="7f8f3-131">Nazwa konta magazynu, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-131">Name of the storage account where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-132">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="7f8f3-132">-StorageContainerName</span></span>
<span data-ttu-id="7f8f3-133">Nazwa kontenera obiektów blob, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-133">Name of the blob container where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-134">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="7f8f3-134">-StorageContainerUri</span></span>
<span data-ttu-id="7f8f3-135">Identyfikator URI kontenera magazynu, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-135">URI of the storage container where the backup is going to be stored.</span></span>

```yaml
Type: System.Uri
Parameter Sets: InteractiveStorageUri, InputObjectStorageUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f8f3-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f8f3-136">-Confirm</span></span>
<span data-ttu-id="7f8f3-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f8f3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f8f3-138">-WhatIf</span></span>
<span data-ttu-id="7f8f3-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f8f3-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f8f3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f8f3-141">CommonParameters</span></span>
<span data-ttu-id="7f8f3-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f8f3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f8f3-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f8f3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f8f3-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f8f3-144">INPUTS</span></span>

### <span data-ttu-id="7f8f3-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7f8f3-145">None</span></span>

## <span data-ttu-id="7f8f3-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f8f3-146">OUTPUTS</span></span>

### <span data-ttu-id="7f8f3-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f8f3-147">System.Boolean</span></span>

## <span data-ttu-id="7f8f3-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f8f3-148">NOTES</span></span>

## <span data-ttu-id="7f8f3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f8f3-149">RELATED LINKS</span></span>
