---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: c94fbf200de5ce56cc3116b1dc7a60052f9c19f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063253"
---
# <span data-ttu-id="19135-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="19135-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="19135-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19135-102">SYNOPSIS</span></span>
<span data-ttu-id="19135-103">Tworzy obiekt mapowania dysku dla dysków maszyny wirtualnej platformy Azure, które mają być replikowane.</span><span class="sxs-lookup"><span data-stu-id="19135-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="19135-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19135-104">SYNTAX</span></span>

### <span data-ttu-id="19135-105">AzureToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="19135-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19135-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="19135-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19135-107">Opis</span><span class="sxs-lookup"><span data-stu-id="19135-107">DESCRIPTION</span></span>
<span data-ttu-id="19135-108">Tworzy obiekt mapowania dysku, który mapuje dysk maszyny wirtualnej platformy Azure na konto magazynu w pamięci podręcznej i docelowe konto magazynu (region odzyskiwania) do użycia w celu zreplikowania dysku.</span><span class="sxs-lookup"><span data-stu-id="19135-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="19135-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19135-109">EXAMPLES</span></span>

### <span data-ttu-id="19135-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="19135-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="19135-111">Utwórz obiekt mapowania dysku na potrzeby replikowania dysków maszyny wirtualnej platformy Azure. Używane podczas operacji na platformie Azure do platformy Azure i ponownej ochrony.</span><span class="sxs-lookup"><span data-stu-id="19135-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="19135-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="19135-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="19135-113">Utwórz obiekt mapowania dysku zarządzanego dla dysków z maszyną wirtualną platformy Azure, które mają zostać zreplikowane. Używane podczas operacji na platformie Azure do platformy Azure i ponownej ochrony.</span><span class="sxs-lookup"><span data-stu-id="19135-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="19135-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="19135-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="19135-115">Utwórz obiekt mapowania dysku zarządzanego z jednym z ustawień szyfrowania przechodzenia na dyski maszyny wirtualnej platformy Azure, które mają zostać zreplikowane. Używane podczas operacji na platformie Azure do platformy Azure i ponownej ochrony.</span><span class="sxs-lookup"><span data-stu-id="19135-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="19135-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="19135-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="19135-117">Utwórz obiekt mapowania dysku zarządzanego z identyfikatorem zestawu szyfrowania dysku docelowego na potrzeby replikowania dysków maszyny wirtualnej platformy Azure. Używane podczas operacji na platformie Azure do platformy Azure i ponownej ochrony.</span><span class="sxs-lookup"><span data-stu-id="19135-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="19135-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19135-118">PARAMETERS</span></span>

### <span data-ttu-id="19135-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19135-119">-DefaultProfile</span></span>
<span data-ttu-id="19135-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19135-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19135-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="19135-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="19135-122">Określa tajny adres URL szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="19135-122">Specifies the disk encryption secret url.</span></span>

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

### <span data-ttu-id="19135-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="19135-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="19135-124">Określa identyfikator ARM magazynu kluczy szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="19135-124">Specifies the disk encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="19135-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="19135-125">-DiskId</span></span>
<span data-ttu-id="19135-126">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="19135-126">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="19135-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="19135-127">-FailoverDiskName</span></span>
<span data-ttu-id="19135-128">Określa nazwę dysku utworzonego podczas pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="19135-128">Specifies the name of the disk created during failover.</span></span>

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

### <span data-ttu-id="19135-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="19135-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="19135-130">Określa adres URL szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="19135-130">Specifies the key encryption Url.</span></span>

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

### <span data-ttu-id="19135-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="19135-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="19135-132">Określa identyfikator ARM magazynu kluczy szyfrowania kluczy.</span><span class="sxs-lookup"><span data-stu-id="19135-132">Specifies the key encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="19135-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="19135-133">-LogStorageAccountId</span></span>
<span data-ttu-id="19135-134">Określa identyfikator konta dziennika lub pamięci podręcznej, który ma być wykorzystywany do przechowywania dzienników replikacji.</span><span class="sxs-lookup"><span data-stu-id="19135-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="19135-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="19135-135">-ManagedDisk</span></span>
<span data-ttu-id="19135-136">Określa dane wejściowe dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="19135-136">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="19135-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="19135-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="19135-138">Określa identyfikator konta usługi Azure Storage, do którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="19135-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="19135-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="19135-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="19135-140">Określa identyfikator zestawu szyfrowanie dysków Azure, który ma być wykorzystywany do odzyskiwania dysków.</span><span class="sxs-lookup"><span data-stu-id="19135-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

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

### <span data-ttu-id="19135-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="19135-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="19135-142">Określa typ konta replikowanego dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="19135-142">Specifies the account type of replicated managed disk.</span></span>

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

### <span data-ttu-id="19135-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="19135-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="19135-144">Określa identyfikator grupy zasobów odzyskiwania dla zreplikowanego dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="19135-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="19135-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="19135-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="19135-146">Określa docelowy dysk odzyskiwania dla zreplikowanego dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="19135-146">Specifies the recovery target disk for replicated managed disk.</span></span>

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

### <span data-ttu-id="19135-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="19135-147">-TfoDiskName</span></span>
<span data-ttu-id="19135-148">Określa nazwę dysku utworzonego podczas testu pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="19135-148">Specifies the name of the disk created during test failover.</span></span>

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

### <span data-ttu-id="19135-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="19135-149">-VhdUri</span></span>
<span data-ttu-id="19135-150">Określ identyfikator URI wirtualnego dysku twardego, do którego odnosi się to mapowanie.</span><span class="sxs-lookup"><span data-stu-id="19135-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="19135-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19135-151">-Confirm</span></span>
<span data-ttu-id="19135-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19135-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19135-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19135-153">-WhatIf</span></span>
<span data-ttu-id="19135-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19135-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19135-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="19135-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19135-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19135-156">CommonParameters</span></span>
<span data-ttu-id="19135-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19135-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19135-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19135-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19135-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19135-159">INPUTS</span></span>

### <span data-ttu-id="19135-160">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="19135-160">None</span></span>

## <span data-ttu-id="19135-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19135-161">OUTPUTS</span></span>

### <span data-ttu-id="19135-162">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="19135-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="19135-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19135-163">NOTES</span></span>

## <span data-ttu-id="19135-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19135-164">RELATED LINKS</span></span>
