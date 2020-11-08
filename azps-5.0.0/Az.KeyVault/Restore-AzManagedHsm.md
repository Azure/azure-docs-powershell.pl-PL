---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
ms.openlocfilehash: 97e5c836d7d6b209d31851264047c6df894d77a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234676"
---
# <span data-ttu-id="a27df-101">Restore-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a27df-101">Restore-AzManagedHsm</span></span>

## <span data-ttu-id="a27df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a27df-102">SYNOPSIS</span></span>
<span data-ttu-id="a27df-103">Umożliwia całkowite przywrócenie zarządzanego modułu HSM z kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="a27df-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="a27df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a27df-104">SYNTAX</span></span>

### <span data-ttu-id="a27df-105">InteractiveStorageName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a27df-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a27df-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="a27df-106">InteractiveStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a27df-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="a27df-107">InputObjectStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a27df-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="a27df-108">InputObjectStorageName</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a27df-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a27df-109">DESCRIPTION</span></span>
<span data-ttu-id="a27df-110">Umożliwia całkowite przywrócenie zarządzanego modułu HSM z kopii zapasowej przechowywanej na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="a27df-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="a27df-111">Użyj `Backup-AzManagedHsm` do wykonania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="a27df-111">Use `Backup-AzManagedHsm` to backup.</span></span>

## <span data-ttu-id="a27df-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a27df-112">EXAMPLES</span></span>

### <span data-ttu-id="a27df-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a27df-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="a27df-114">Przykład przywraca kopię zapasową przechowywaną w folderze o nazwie "mhsm-myHsm-2020101308504935" kontenera magazynu "https://{AccountName}. blob. Core. Windows. NET/{ContainerName}".</span><span class="sxs-lookup"><span data-stu-id="a27df-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="a27df-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a27df-115">PARAMETERS</span></span>

### <span data-ttu-id="a27df-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="a27df-116">-BackupFolder</span></span>
<span data-ttu-id="a27df-117">Nazwa folderu kopii zapasowej, na przykład "mhsm- *-2020101309020403". Można go również zagnieżdżać, na przykład "kopia zapasowa/mhsm-* -2020101309020403".</span><span class="sxs-lookup"><span data-stu-id="a27df-117">Folder name of the backup, e.g. 'mhsm- *-2020101309020403'. It can also be nested such as 'backups/mhsm-* -2020101309020403'.</span></span>

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

### <span data-ttu-id="a27df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27df-118">-DefaultProfile</span></span>
<span data-ttu-id="a27df-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a27df-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a27df-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="a27df-120">-HsmObject</span></span>
<span data-ttu-id="a27df-121">Obiekt Managed HSM</span><span class="sxs-lookup"><span data-stu-id="a27df-121">Managed HSM object</span></span>

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

### <span data-ttu-id="a27df-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a27df-122">-Name</span></span>
<span data-ttu-id="a27df-123">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="a27df-123">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases: HsmName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a27df-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a27df-124">-PassThru</span></span>
<span data-ttu-id="a27df-125">Zwraca wartość true, gdy HSM jest przywracany.</span><span class="sxs-lookup"><span data-stu-id="a27df-125">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="a27df-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="a27df-126">-SasToken</span></span>
<span data-ttu-id="a27df-127">Token dostępu współdzielonego (SAS, Access Signature) umożliwiający uwierzytelnienie konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a27df-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="a27df-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a27df-128">-StorageAccountName</span></span>
<span data-ttu-id="a27df-129">Nazwa konta magazynu, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="a27df-129">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="a27df-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="a27df-130">-StorageContainerName</span></span>
<span data-ttu-id="a27df-131">Nazwa kontenera obiektów blob, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="a27df-131">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="a27df-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="a27df-132">-StorageContainerUri</span></span>
<span data-ttu-id="a27df-133">Identyfikator URI kontenera magazynu, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="a27df-133">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="a27df-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a27df-134">-Confirm</span></span>
<span data-ttu-id="a27df-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a27df-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a27df-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a27df-136">-WhatIf</span></span>
<span data-ttu-id="a27df-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a27df-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a27df-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a27df-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a27df-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27df-139">CommonParameters</span></span>
<span data-ttu-id="a27df-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a27df-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27df-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a27df-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27df-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a27df-142">INPUTS</span></span>

### <span data-ttu-id="a27df-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a27df-143">None</span></span>

## <span data-ttu-id="a27df-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a27df-144">OUTPUTS</span></span>

### <span data-ttu-id="a27df-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a27df-145">System.Boolean</span></span>

## <span data-ttu-id="a27df-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a27df-146">NOTES</span></span>

## <span data-ttu-id="a27df-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a27df-147">RELATED LINKS</span></span>
