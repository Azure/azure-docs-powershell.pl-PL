---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
ms.openlocfilehash: 5353adade342b7f73cf60ff6b0befa88f4a3da73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224286"
---
# <span data-ttu-id="a1176-101">Backup-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a1176-101">Backup-AzManagedHsm</span></span>

## <span data-ttu-id="a1176-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1176-102">SYNOPSIS</span></span>
<span data-ttu-id="a1176-103">Pełne tworzenie kopii zapasowej zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="a1176-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="a1176-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1176-104">SYNTAX</span></span>

### <span data-ttu-id="a1176-105">InteractiveStorageName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a1176-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1176-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="a1176-106">InteractiveStorageUri</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1176-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="a1176-107">InputObjectStorageUri</span></span>
```
Backup-AzManagedHsm -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1176-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="a1176-108">InputObjectStorageName</span></span>
```
Backup-AzManagedHsm -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1176-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a1176-109">DESCRIPTION</span></span>
<span data-ttu-id="a1176-110">Pełne wykonywanie kopii zapasowej zarządzanego modułu HSM na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="a1176-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="a1176-111">Użyj, `Restore-AzManagedHsm` Aby przywrócić kopię zapasową.</span><span class="sxs-lookup"><span data-stu-id="a1176-111">Use `Restore-AzManagedHsm` to restore the backup.</span></span>

## <span data-ttu-id="a1176-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1176-112">EXAMPLES</span></span>

### <span data-ttu-id="a1176-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a1176-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="a1176-114">Polecenie cmdlet spowoduje utworzenie folderu (zwykle nazywanego `mhsm-{name}-{timestamp}` ) w kontenerze magazynu, zapisanie kopii zapasowej w tym folderze i wyjście z folderu o identyfikatorze URI.</span><span class="sxs-lookup"><span data-stu-id="a1176-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="a1176-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1176-115">PARAMETERS</span></span>

### <span data-ttu-id="a1176-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1176-116">-DefaultProfile</span></span>
<span data-ttu-id="a1176-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1176-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1176-118">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="a1176-118">-HsmObject</span></span>
<span data-ttu-id="a1176-119">Obiekt Managed HSM</span><span class="sxs-lookup"><span data-stu-id="a1176-119">Managed HSM object</span></span>

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

### <span data-ttu-id="a1176-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1176-120">-Name</span></span>
<span data-ttu-id="a1176-121">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="a1176-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="a1176-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="a1176-122">-SasToken</span></span>
<span data-ttu-id="a1176-123">Token dostępu współdzielonego (SAS, Access Signature) umożliwiający uwierzytelnienie konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a1176-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="a1176-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a1176-124">-StorageAccountName</span></span>
<span data-ttu-id="a1176-125">Nazwa konta magazynu, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="a1176-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="a1176-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="a1176-126">-StorageContainerName</span></span>
<span data-ttu-id="a1176-127">Nazwa kontenera obiektów blob, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="a1176-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="a1176-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="a1176-128">-StorageContainerUri</span></span>
<span data-ttu-id="a1176-129">Identyfikator URI kontenera magazynu, w którym ma być przechowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="a1176-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="a1176-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1176-130">-Confirm</span></span>
<span data-ttu-id="a1176-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1176-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1176-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1176-132">-WhatIf</span></span>
<span data-ttu-id="a1176-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1176-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1176-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a1176-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1176-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1176-135">CommonParameters</span></span>
<span data-ttu-id="a1176-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1176-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1176-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1176-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1176-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1176-138">INPUTS</span></span>

### <span data-ttu-id="a1176-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a1176-139">None</span></span>

## <span data-ttu-id="a1176-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1176-140">OUTPUTS</span></span>

### <span data-ttu-id="a1176-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a1176-141">System.String</span></span>

## <span data-ttu-id="a1176-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1176-142">NOTES</span></span>

## <span data-ttu-id="a1176-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1176-143">RELATED LINKS</span></span>
