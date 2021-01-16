---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
ms.openlocfilehash: 7d2bb9d961b5fba7ecd5e0d83f8d86ac1a930c75
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386402"
---
# <span data-ttu-id="53164-101">Backup-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="53164-101">Backup-AzKeyVault</span></span>

## <span data-ttu-id="53164-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53164-102">SYNOPSIS</span></span>
<span data-ttu-id="53164-103">Pełne tworzenie kopii zapasowej zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="53164-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="53164-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53164-104">SYNTAX</span></span>

### <span data-ttu-id="53164-105">InteractiveStorageName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="53164-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53164-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="53164-106">InteractiveStorageUri</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53164-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="53164-107">InputObjectStorageUri</span></span>
```
Backup-AzKeyVault -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53164-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="53164-108">InputObjectStorageName</span></span>
```
Backup-AzKeyVault -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53164-109">Opis</span><span class="sxs-lookup"><span data-stu-id="53164-109">DESCRIPTION</span></span>
<span data-ttu-id="53164-110">Pełne wykonywanie kopii zapasowej zarządzanego modułu HSM na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="53164-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="53164-111">Użyj, `Restore-AzKeyVault` Aby przywrócić kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="53164-111">Use `Restore-AzKeyVault` to restore the backup.</span></span>

## <span data-ttu-id="53164-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53164-112">EXAMPLES</span></span>

### <span data-ttu-id="53164-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="53164-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="53164-114">Polecenie cmdlet spowoduje utworzenie folderu (zwykle nazywanego `mhsm-{name}-{timestamp}` ) w kontenerze magazynu, zapisanie kopii zapasowej w tym folderze i wyjście z folderu o identyfikatorze URI.</span><span class="sxs-lookup"><span data-stu-id="53164-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="53164-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53164-115">PARAMETERS</span></span>

### <span data-ttu-id="53164-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53164-116">-DefaultProfile</span></span>
<span data-ttu-id="53164-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53164-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53164-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="53164-118">-HsmName</span></span>
<span data-ttu-id="53164-119">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="53164-119">Name of the HSM.</span></span>

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

### <span data-ttu-id="53164-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="53164-120">-HsmObject</span></span>
<span data-ttu-id="53164-121">Obiekt Managed HSM</span><span class="sxs-lookup"><span data-stu-id="53164-121">Managed HSM object</span></span>

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

### <span data-ttu-id="53164-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="53164-122">-SasToken</span></span>
<span data-ttu-id="53164-123">Token dostępu współdzielonego (SAS, Access Signature) umożliwiający uwierzytelnienie konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="53164-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="53164-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="53164-124">-StorageAccountName</span></span>
<span data-ttu-id="53164-125">Nazwa konta magazynu, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="53164-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="53164-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="53164-126">-StorageContainerName</span></span>
<span data-ttu-id="53164-127">Nazwa kontenera obiektów blob, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="53164-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="53164-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="53164-128">-StorageContainerUri</span></span>
<span data-ttu-id="53164-129">Identyfikator URI kontenera magazynu, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="53164-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="53164-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53164-130">-Confirm</span></span>
<span data-ttu-id="53164-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53164-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53164-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53164-132">-WhatIf</span></span>
<span data-ttu-id="53164-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53164-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53164-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="53164-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53164-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53164-135">CommonParameters</span></span>
<span data-ttu-id="53164-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53164-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53164-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53164-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53164-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53164-138">INPUTS</span></span>

### <span data-ttu-id="53164-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="53164-139">None</span></span>

## <span data-ttu-id="53164-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53164-140">OUTPUTS</span></span>

### <span data-ttu-id="53164-141">System. String</span><span class="sxs-lookup"><span data-stu-id="53164-141">System.String</span></span>

## <span data-ttu-id="53164-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53164-142">NOTES</span></span>

## <span data-ttu-id="53164-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53164-143">RELATED LINKS</span></span>
