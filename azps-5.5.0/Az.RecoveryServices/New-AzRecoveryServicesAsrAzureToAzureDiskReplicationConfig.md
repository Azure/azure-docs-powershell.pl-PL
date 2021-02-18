---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: c94fbf200de5ce56cc3116b1dc7a60052f9c19f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192898"
---
# <span data-ttu-id="03c9b-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="03c9b-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="03c9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="03c9b-103">Tworzy obiekt mapowania dysku, aby zreplikować dysk w maszynce wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="03c9b-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="03c9b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="03c9b-104">SYNTAX</span></span>

### <span data-ttu-id="03c9b-105">AzureToAzure (domyślne)</span><span class="sxs-lookup"><span data-stu-id="03c9b-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03c9b-106">AzureToAzureManagedChat</span><span class="sxs-lookup"><span data-stu-id="03c9b-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c9b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="03c9b-107">DESCRIPTION</span></span>
<span data-ttu-id="03c9b-108">Tworzy obiekt mapowania dysku, który mapuje dysk maszyny wirtualnej platformy Azure na konto pamięci podręcznej i docelowe konto magazynu (region odzyskiwania), które ma być używane do replikowania dysku.</span><span class="sxs-lookup"><span data-stu-id="03c9b-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="03c9b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="03c9b-109">EXAMPLES</span></span>

### <span data-ttu-id="03c9b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03c9b-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="03c9b-111">Utwórz obiekt mapowania dysku, aby zreplikować dysk maszyn wirtualnych platformy Azure. Używany podczas operacji Azure To Azure EnableDr i ponownej ochrony.</span><span class="sxs-lookup"><span data-stu-id="03c9b-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="03c9b-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="03c9b-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="03c9b-113">Utwórz obiekt mapowania dysków zarządzanych, aby zreplikować dysk maszyn wirtualnych platformy Azure. Używany podczas operacji Azure To Azure EnableDr i ponownej ochrony.</span><span class="sxs-lookup"><span data-stu-id="03c9b-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="03c9b-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="03c9b-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="03c9b-115">Utwórz obiekt mapowania dysków zarządzanych z ustawieniami szyfrowania jednodniowego dla replikowania dysków maszyn wirtualnych platformy Azure. Używany podczas operacji Azure To Azure EnableDr i ponownie chroń operację.</span><span class="sxs-lookup"><span data-stu-id="03c9b-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="03c9b-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="03c9b-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="03c9b-117">Utwórz obiekt mapowania dysku zarządzanego z identyfikatorem szyfrowania dysku docelowego, aby replikować dysk maszyn wirtualnych platformy Azure. Używany podczas operacji Azure To Azure EnableDr i ponownej ochrony.</span><span class="sxs-lookup"><span data-stu-id="03c9b-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="03c9b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03c9b-118">PARAMETERS</span></span>

### <span data-ttu-id="03c9b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c9b-119">-DefaultProfile</span></span>
<span data-ttu-id="03c9b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="03c9b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03c9b-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="03c9b-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="03c9b-122">Określa tajny adres URL szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="03c9b-122">Specifies the disk encryption secret url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="03c9b-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="03c9b-124">Określa magazyn klucza szyfrowania dysku, ARM identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="03c9b-124">Specifies the disk encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-125">- DiskId</span><span class="sxs-lookup"><span data-stu-id="03c9b-125">-DiskId</span></span>
<span data-ttu-id="03c9b-126">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="03c9b-126">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-127">-FailoverName</span><span class="sxs-lookup"><span data-stu-id="03c9b-127">-FailoverDiskName</span></span>
<span data-ttu-id="03c9b-128">Określa nazwę dysku utworzonego podczas trybu failover.</span><span class="sxs-lookup"><span data-stu-id="03c9b-128">Specifies the name of the disk created during failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="03c9b-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="03c9b-130">Określa klucz adresu URL szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="03c9b-130">Specifies the key encryption Url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="03c9b-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="03c9b-132">Określa klucz klucza szyfrowania magazynu ARM identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="03c9b-132">Specifies the key encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="03c9b-133">-LogStorageAccountId</span></span>
<span data-ttu-id="03c9b-134">Określa identyfikator konta magazynu w dzienniku lub pamięci podręcznej, który ma być używany do przechowywania dzienników replikacji.</span><span class="sxs-lookup"><span data-stu-id="03c9b-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="03c9b-135">-Managed Jednak</span><span class="sxs-lookup"><span data-stu-id="03c9b-135">-ManagedDisk</span></span>
<span data-ttu-id="03c9b-136">Określa dane wejściowe dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="03c9b-136">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="03c9b-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="03c9b-138">Określa identyfikator konta magazynu platformy Azure, do których chcesz zreplikować dane.</span><span class="sxs-lookup"><span data-stu-id="03c9b-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-139">-RecoveryCryptEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="03c9b-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="03c9b-140">Określa identyfikator zestawu szyfrowania dysku platformy Azure, który ma być używany do odzyskiwania dysków.</span><span class="sxs-lookup"><span data-stu-id="03c9b-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-141">-RecoveryReplicaCountAccountType</span><span class="sxs-lookup"><span data-stu-id="03c9b-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="03c9b-142">Określa typ konta replikowanego dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="03c9b-142">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="03c9b-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="03c9b-144">Określa identyfikator grupy zasobów odzyskiwania dla replikowanego dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="03c9b-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-145">-RecoveryTargetGetAccountType</span><span class="sxs-lookup"><span data-stu-id="03c9b-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="03c9b-146">Określa dysk docelowy odzyskiwania dla replikowanego dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="03c9b-146">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-147">-TfoNameName</span><span class="sxs-lookup"><span data-stu-id="03c9b-147">-TfoDiskName</span></span>
<span data-ttu-id="03c9b-148">Określa nazwę dysku utworzonego podczas testowania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="03c9b-148">Specifies the name of the disk created during test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-149">- VhdUri</span><span class="sxs-lookup"><span data-stu-id="03c9b-149">-VhdUri</span></span>
<span data-ttu-id="03c9b-150">Określ wartość URI VHD dysku, do których odpowiada to mapowanie.</span><span class="sxs-lookup"><span data-stu-id="03c9b-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c9b-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03c9b-151">-Confirm</span></span>
<span data-ttu-id="03c9b-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="03c9b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c9b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c9b-153">-WhatIf</span></span>
<span data-ttu-id="03c9b-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03c9b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c9b-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="03c9b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c9b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c9b-156">CommonParameters</span></span>
<span data-ttu-id="03c9b-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c9b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c9b-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03c9b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c9b-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03c9b-159">INPUTS</span></span>

### <span data-ttu-id="03c9b-160">Brak</span><span class="sxs-lookup"><span data-stu-id="03c9b-160">None</span></span>

## <span data-ttu-id="03c9b-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03c9b-161">OUTPUTS</span></span>

### <span data-ttu-id="03c9b-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureChatReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="03c9b-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="03c9b-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="03c9b-163">NOTES</span></span>

## <span data-ttu-id="03c9b-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03c9b-164">RELATED LINKS</span></span>
