---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
ms.openlocfilehash: 9f1d18586d0d903f705b3b2be21dd8f864efcf9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986021"
---
# <span data-ttu-id="b3e62-101">Backup-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="b3e62-101">Backup-AzKeyVault</span></span>

## <span data-ttu-id="b3e62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3e62-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e62-103">Pełne tworzenie kopii zapasowej zarządzanego systemu HSM.</span><span class="sxs-lookup"><span data-stu-id="b3e62-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="b3e62-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b3e62-104">SYNTAX</span></span>

### <span data-ttu-id="b3e62-105">InteractiveStorageName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="b3e62-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3e62-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="b3e62-106">InteractiveStorageUri</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3e62-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="b3e62-107">InputObjectStorageUri</span></span>
```
Backup-AzKeyVault -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3e62-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="b3e62-108">InputObjectStorageName</span></span>
```
Backup-AzKeyVault -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3e62-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b3e62-109">DESCRIPTION</span></span>
<span data-ttu-id="b3e62-110">Pełne tworzenie kopii zapasowej zarządzanego modułu HSM na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="b3e62-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="b3e62-111">Użyj, `Restore-AzKeyVault` aby przywrócić kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="b3e62-111">Use `Restore-AzKeyVault` to restore the backup.</span></span>

## <span data-ttu-id="b3e62-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b3e62-112">EXAMPLES</span></span>

### <span data-ttu-id="b3e62-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b3e62-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="b3e62-114">Polecenie cmdlet utworzy folder (o nazwie zwykle nazywanej) w kontenerze magazynu, przechowa kopię zapasową w tym folderze i `mhsm-{name}-{timestamp}` wyprowadzi URI folderu.</span><span class="sxs-lookup"><span data-stu-id="b3e62-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="b3e62-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3e62-115">PARAMETERS</span></span>

### <span data-ttu-id="b3e62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e62-116">-DefaultProfile</span></span>
<span data-ttu-id="b3e62-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3e62-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3e62-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="b3e62-118">-HsmName</span></span>
<span data-ttu-id="b3e62-119">Nazwa hsm.</span><span class="sxs-lookup"><span data-stu-id="b3e62-119">Name of the HSM.</span></span>

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

### <span data-ttu-id="b3e62-120">- HsmObject</span><span class="sxs-lookup"><span data-stu-id="b3e62-120">-HsmObject</span></span>
<span data-ttu-id="b3e62-121">Zarządzany obiekt HSM</span><span class="sxs-lookup"><span data-stu-id="b3e62-121">Managed HSM object</span></span>

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

### <span data-ttu-id="b3e62-122">- SasToken</span><span class="sxs-lookup"><span data-stu-id="b3e62-122">-SasToken</span></span>
<span data-ttu-id="b3e62-123">Token podpisu dostępu udostępnionego (SAS) do uwierzytelnienia konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b3e62-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="b3e62-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b3e62-124">-StorageAccountName</span></span>
<span data-ttu-id="b3e62-125">Nazwa konta magazynu, na którym będzie przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="b3e62-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="b3e62-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="b3e62-126">-StorageContainerName</span></span>
<span data-ttu-id="b3e62-127">Nazwa kontenera obiektów blob, w którym będzie przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="b3e62-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="b3e62-128">— StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="b3e62-128">-StorageContainerUri</span></span>
<span data-ttu-id="b3e62-129">URI kontenera magazynu, w którym będzie przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="b3e62-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="b3e62-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3e62-130">-Confirm</span></span>
<span data-ttu-id="b3e62-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b3e62-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3e62-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e62-132">-WhatIf</span></span>
<span data-ttu-id="b3e62-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3e62-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3e62-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b3e62-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3e62-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e62-135">CommonParameters</span></span>
<span data-ttu-id="b3e62-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e62-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e62-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3e62-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e62-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3e62-138">INPUTS</span></span>

### <span data-ttu-id="b3e62-139">Brak</span><span class="sxs-lookup"><span data-stu-id="b3e62-139">None</span></span>

## <span data-ttu-id="b3e62-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3e62-140">OUTPUTS</span></span>

### <span data-ttu-id="b3e62-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b3e62-141">System.String</span></span>

## <span data-ttu-id="b3e62-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b3e62-142">NOTES</span></span>

## <span data-ttu-id="b3e62-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3e62-143">RELATED LINKS</span></span>
