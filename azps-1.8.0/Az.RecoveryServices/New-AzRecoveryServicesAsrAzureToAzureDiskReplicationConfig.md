---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 1f67da2d15aca003853bcb21846535bad4e2a066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708642"
---
# <span data-ttu-id="e8c36-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="e8c36-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="e8c36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8c36-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c36-103">Tworzy obiekt mapowania dysku dla dysków maszyny wirtualnej platformy Azure, które mają być replikowane.</span><span class="sxs-lookup"><span data-stu-id="e8c36-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="e8c36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8c36-104">SYNTAX</span></span>

### <span data-ttu-id="e8c36-105">AzureToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e8c36-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8c36-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e8c36-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8c36-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e8c36-107">DESCRIPTION</span></span>
<span data-ttu-id="e8c36-108">Tworzy obiekt mapowania dysku, który mapuje dysk maszyny wirtualnej platformy Azure na konto magazynu w pamięci podręcznej i docelowe konto magazynu (region odzyskiwania) do użycia w celu zreplikowania dysku.</span><span class="sxs-lookup"><span data-stu-id="e8c36-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="e8c36-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8c36-109">EXAMPLES</span></span>

### <span data-ttu-id="e8c36-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8c36-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="e8c36-111">Utwórz obiekt mapowania dysku na potrzeby replikowania dysków maszyny wirtualnej platformy Azure. Używane podczas operacji włączania funkcji Azure to Azure do platformy Azure i ochrony.</span><span class="sxs-lookup"><span data-stu-id="e8c36-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="e8c36-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8c36-112">PARAMETERS</span></span>

### <span data-ttu-id="e8c36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c36-113">-DefaultProfile</span></span>
<span data-ttu-id="e8c36-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8c36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8c36-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="e8c36-115">-DiskId</span></span>
<span data-ttu-id="e8c36-116">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e8c36-116">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="e8c36-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e8c36-117">-LogStorageAccountId</span></span>
<span data-ttu-id="e8c36-118">Określa identyfikator konta dziennika lub pamięci podręcznej, który ma być wykorzystywany do przechowywania dzienników replikacji.</span><span class="sxs-lookup"><span data-stu-id="e8c36-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="e8c36-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e8c36-119">-ManagedDisk</span></span>
<span data-ttu-id="e8c36-120">Określa dane wejściowe dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e8c36-120">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="e8c36-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e8c36-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="e8c36-122">Określa identyfikator konta usługi Azure Storage, do którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="e8c36-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="e8c36-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="e8c36-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="e8c36-124">Określa typ konta replikowanego dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e8c36-124">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8c36-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="e8c36-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="e8c36-126">Określa identyfikator grupy zasobów odzyskiwania dla zreplikowanego dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e8c36-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="e8c36-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="e8c36-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="e8c36-128">Określa docelowy dysk odzyskiwania dla zreplikowanego dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e8c36-128">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8c36-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="e8c36-129">-VhdUri</span></span>
<span data-ttu-id="e8c36-130">Określ identyfikator URI wirtualnego dysku twardego, do którego odnosi się to mapowanie.</span><span class="sxs-lookup"><span data-stu-id="e8c36-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="e8c36-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8c36-131">-Confirm</span></span>
<span data-ttu-id="e8c36-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8c36-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8c36-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8c36-133">-WhatIf</span></span>
<span data-ttu-id="e8c36-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8c36-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8c36-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8c36-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8c36-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c36-136">CommonParameters</span></span>
<span data-ttu-id="e8c36-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8c36-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c36-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8c36-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c36-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8c36-139">INPUTS</span></span>

### <span data-ttu-id="e8c36-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e8c36-140">None</span></span>

## <span data-ttu-id="e8c36-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8c36-141">OUTPUTS</span></span>

### <span data-ttu-id="e8c36-142">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="e8c36-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="e8c36-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8c36-143">NOTES</span></span>

## <span data-ttu-id="e8c36-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8c36-144">RELATED LINKS</span></span>
