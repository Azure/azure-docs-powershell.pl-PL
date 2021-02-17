---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: d1cf3757596a56336c25c46bd6c4e38687888d6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243347"
---
# <span data-ttu-id="79c77-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="79c77-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="79c77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79c77-102">SYNOPSIS</span></span>
<span data-ttu-id="79c77-103">W pełni przywraca zarządzany moduł HSM z kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="79c77-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="79c77-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79c77-104">SYNTAX</span></span>

### <span data-ttu-id="79c77-105">InteractiveStorageName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="79c77-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79c77-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="79c77-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageContainerUri <Uri> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79c77-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="79c77-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageContainerUri <Uri>
 -SasToken <SecureString> -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79c77-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="79c77-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79c77-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="79c77-109">DESCRIPTION</span></span>
<span data-ttu-id="79c77-110">W pełni przywraca zarządzany moduł HSM z kopii zapasowej przechowywanej na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="79c77-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="79c77-111">Użyj do `Backup-AzKeyVault` tworzenia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="79c77-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="79c77-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79c77-112">EXAMPLES</span></span>

### <span data-ttu-id="79c77-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79c77-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="79c77-114">Przykład przywraca kopię zapasową przechowywaną w folderze o nazwie "mhsm-myHsm-2020101308504935" kontenera magazynu "https://{accountName}.blob.core.windows.net/{containerName}".</span><span class="sxs-lookup"><span data-stu-id="79c77-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="79c77-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79c77-115">PARAMETERS</span></span>

### <span data-ttu-id="79c77-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="79c77-116">-BackupFolder</span></span>
<span data-ttu-id="79c77-117">Nazwa folderu kopii zapasowej, na przykład "mhsm-*-2020101309020403". Może też być zagnieżdżony, na przykład "kopie zapasowe/mhsm-*-2020101309020403".</span><span class="sxs-lookup"><span data-stu-id="79c77-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

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

### <span data-ttu-id="79c77-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c77-118">-DefaultProfile</span></span>
<span data-ttu-id="79c77-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="79c77-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79c77-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="79c77-120">-HsmName</span></span>
<span data-ttu-id="79c77-121">Nazwa hsm.</span><span class="sxs-lookup"><span data-stu-id="79c77-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="79c77-122">- HsmObject</span><span class="sxs-lookup"><span data-stu-id="79c77-122">-HsmObject</span></span>
<span data-ttu-id="79c77-123">Zarządzany obiekt HSM</span><span class="sxs-lookup"><span data-stu-id="79c77-123">Managed HSM object</span></span>

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

### <span data-ttu-id="79c77-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="79c77-124">-KeyName</span></span>
<span data-ttu-id="79c77-125">Nazwa klucza do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="79c77-125">Key name to restore.</span></span>

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

### <span data-ttu-id="79c77-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79c77-126">-PassThru</span></span>
<span data-ttu-id="79c77-127">Zwraca wartość prawda po przywróceniu HSM.</span><span class="sxs-lookup"><span data-stu-id="79c77-127">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="79c77-128">- SasToken</span><span class="sxs-lookup"><span data-stu-id="79c77-128">-SasToken</span></span>
<span data-ttu-id="79c77-129">Token podpisu dostępu udostępnionego (SAS) do uwierzytelnienia konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="79c77-129">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="79c77-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="79c77-130">-StorageAccountName</span></span>
<span data-ttu-id="79c77-131">Nazwa konta magazynu, na którym będzie przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="79c77-131">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="79c77-132">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="79c77-132">-StorageContainerName</span></span>
<span data-ttu-id="79c77-133">Nazwa kontenera obiektów blob, w którym będzie przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="79c77-133">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="79c77-134">— StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="79c77-134">-StorageContainerUri</span></span>
<span data-ttu-id="79c77-135">URI kontenera magazynu, w którym będzie przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="79c77-135">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="79c77-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79c77-136">-Confirm</span></span>
<span data-ttu-id="79c77-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="79c77-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79c77-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79c77-138">-WhatIf</span></span>
<span data-ttu-id="79c77-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79c77-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79c77-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="79c77-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79c77-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c77-141">CommonParameters</span></span>
<span data-ttu-id="79c77-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c77-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c77-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79c77-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c77-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79c77-144">INPUTS</span></span>

### <span data-ttu-id="79c77-145">Brak</span><span class="sxs-lookup"><span data-stu-id="79c77-145">None</span></span>

## <span data-ttu-id="79c77-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79c77-146">OUTPUTS</span></span>

### <span data-ttu-id="79c77-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="79c77-147">System.Boolean</span></span>

## <span data-ttu-id="79c77-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79c77-148">NOTES</span></span>

## <span data-ttu-id="79c77-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79c77-149">RELATED LINKS</span></span>
