---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: 8be76f6eb5cf56e5f4612a175c067a7647576a4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354937"
---
# <span data-ttu-id="e86d8-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="e86d8-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="e86d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e86d8-102">SYNOPSIS</span></span>
<span data-ttu-id="e86d8-103">Umożliwia całkowite przywrócenie zarządzanego modułu HSM z kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e86d8-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="e86d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e86d8-104">SYNTAX</span></span>

### <span data-ttu-id="e86d8-105">InteractiveStorageName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e86d8-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] [-HsmName] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e86d8-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="e86d8-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] [-HsmName] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e86d8-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="e86d8-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e86d8-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="e86d8-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e86d8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e86d8-109">DESCRIPTION</span></span>
<span data-ttu-id="e86d8-110">Umożliwia całkowite przywrócenie zarządzanego modułu HSM z kopii zapasowej przechowywanej na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="e86d8-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="e86d8-111">Użyj `Backup-AzKeyVault` do wykonania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e86d8-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="e86d8-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e86d8-112">EXAMPLES</span></span>

### <span data-ttu-id="e86d8-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e86d8-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="e86d8-114">Przykład przywraca kopię zapasową przechowywaną w folderze o nazwie "mhsm-myHsm-2020101308504935" kontenera magazynu "https://{AccountName}. blob. Core. Windows. NET/{ContainerName}".</span><span class="sxs-lookup"><span data-stu-id="e86d8-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="e86d8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e86d8-115">PARAMETERS</span></span>

### <span data-ttu-id="e86d8-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="e86d8-116">-BackupFolder</span></span>
<span data-ttu-id="e86d8-117">Nazwa folderu kopii zapasowej, na przykład "mhsm-*-2020101309020403". Można go również zagnieżdżać, na przykład "kopia zapasowa/mhsm-*-2020101309020403".</span><span class="sxs-lookup"><span data-stu-id="e86d8-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

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

### <span data-ttu-id="e86d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e86d8-118">-DefaultProfile</span></span>
<span data-ttu-id="e86d8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e86d8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e86d8-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="e86d8-120">-HsmName</span></span>
<span data-ttu-id="e86d8-121">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="e86d8-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="e86d8-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="e86d8-122">-HsmObject</span></span>
<span data-ttu-id="e86d8-123">Obiekt Managed HSM</span><span class="sxs-lookup"><span data-stu-id="e86d8-123">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86d8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e86d8-124">-PassThru</span></span>
<span data-ttu-id="e86d8-125">Zwraca wartość true, gdy HSM jest przywracany.</span><span class="sxs-lookup"><span data-stu-id="e86d8-125">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="e86d8-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="e86d8-126">-SasToken</span></span>
<span data-ttu-id="e86d8-127">Token dostępu współdzielonego (SAS, Access Signature) umożliwiający uwierzytelnienie konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e86d8-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="e86d8-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e86d8-128">-StorageAccountName</span></span>
<span data-ttu-id="e86d8-129">Nazwa konta magazynu, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="e86d8-129">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="e86d8-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="e86d8-130">-StorageContainerName</span></span>
<span data-ttu-id="e86d8-131">Nazwa kontenera obiektów blob, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="e86d8-131">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="e86d8-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="e86d8-132">-StorageContainerUri</span></span>
<span data-ttu-id="e86d8-133">Identyfikator URI kontenera magazynu, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="e86d8-133">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="e86d8-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e86d8-134">-Confirm</span></span>
<span data-ttu-id="e86d8-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e86d8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e86d8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e86d8-136">-WhatIf</span></span>
<span data-ttu-id="e86d8-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e86d8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e86d8-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e86d8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e86d8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e86d8-139">CommonParameters</span></span>
<span data-ttu-id="e86d8-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e86d8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e86d8-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e86d8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e86d8-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e86d8-142">INPUTS</span></span>

### <span data-ttu-id="e86d8-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e86d8-143">None</span></span>

## <span data-ttu-id="e86d8-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e86d8-144">OUTPUTS</span></span>

### <span data-ttu-id="e86d8-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e86d8-145">System.Boolean</span></span>

## <span data-ttu-id="e86d8-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e86d8-146">NOTES</span></span>

## <span data-ttu-id="e86d8-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e86d8-147">RELATED LINKS</span></span>
