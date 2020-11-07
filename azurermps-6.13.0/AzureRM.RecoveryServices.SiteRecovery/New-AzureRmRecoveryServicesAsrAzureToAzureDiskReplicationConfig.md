---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 19ba256176c47b5841b9d124d186f376f0ecce7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716575"
---
# <span data-ttu-id="d010b-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="d010b-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="d010b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d010b-102">SYNOPSIS</span></span>
<span data-ttu-id="d010b-103">Tworzy obiekt mapowania dysku dla dysków maszyny wirtualnej platformy Azure, które mają być replikowane.</span><span class="sxs-lookup"><span data-stu-id="d010b-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d010b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d010b-104">SYNTAX</span></span>

### <span data-ttu-id="d010b-105">AzureToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d010b-105">AzureToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d010b-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="d010b-106">AzureToAzureManagedDisk</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d010b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d010b-107">DESCRIPTION</span></span>
<span data-ttu-id="d010b-108">Tworzy obiekt mapowania dysku, który mapuje dysk maszyny wirtualnej platformy Azure na konto magazynu w pamięci podręcznej i docelowe konto magazynu (region odzyskiwania) do użycia w celu zreplikowania dysku.</span><span class="sxs-lookup"><span data-stu-id="d010b-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="d010b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d010b-109">EXAMPLES</span></span>

### <span data-ttu-id="d010b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d010b-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="d010b-111">Utwórz obiekt mapowania dysku na potrzeby replikowania dysków maszyny wirtualnej platformy Azure. Używane podczas operacji włączania funkcji Azure to Azure do platformy Azure i ochrony.</span><span class="sxs-lookup"><span data-stu-id="d010b-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="d010b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d010b-112">PARAMETERS</span></span>

### <span data-ttu-id="d010b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d010b-113">-DefaultProfile</span></span>
<span data-ttu-id="d010b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d010b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d010b-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="d010b-115">-DiskId</span></span>
<span data-ttu-id="d010b-116">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="d010b-116">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="d010b-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d010b-117">-LogStorageAccountId</span></span>
<span data-ttu-id="d010b-118">Określa identyfikator konta dziennika lub pamięci podręcznej, który ma być wykorzystywany do przechowywania dzienników replikacji.</span><span class="sxs-lookup"><span data-stu-id="d010b-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="d010b-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="d010b-119">-ManagedDisk</span></span>
<span data-ttu-id="d010b-120">Określa dane wejściowe dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="d010b-120">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="d010b-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d010b-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="d010b-122">Określa identyfikator konta usługi Azure Storage, do którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="d010b-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="d010b-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="d010b-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="d010b-124">Określa typ konta replikowanego dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="d010b-124">Specifies the account type of replicated managed disk.</span></span>

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

### <span data-ttu-id="d010b-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="d010b-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="d010b-126">Określa identyfikator grupy zasobów odzyskiwania dla zreplikowanego dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="d010b-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="d010b-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="d010b-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="d010b-128">Określa docelowy dysk odzyskiwania dla zreplikowanego dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="d010b-128">Specifies the recovery target disk for replicated managed disk.</span></span>

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

### <span data-ttu-id="d010b-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="d010b-129">-VhdUri</span></span>
<span data-ttu-id="d010b-130">Określ identyfikator URI wirtualnego dysku twardego, do którego odnosi się to mapowanie.</span><span class="sxs-lookup"><span data-stu-id="d010b-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="d010b-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d010b-131">-Confirm</span></span>
<span data-ttu-id="d010b-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d010b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d010b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d010b-133">-WhatIf</span></span>
<span data-ttu-id="d010b-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d010b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d010b-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d010b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d010b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d010b-136">CommonParameters</span></span>
<span data-ttu-id="d010b-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d010b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d010b-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d010b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d010b-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d010b-139">INPUTS</span></span>

### <span data-ttu-id="d010b-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d010b-140">None</span></span>

## <span data-ttu-id="d010b-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d010b-141">OUTPUTS</span></span>

### <span data-ttu-id="d010b-142">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="d010b-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="d010b-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d010b-143">NOTES</span></span>

## <span data-ttu-id="d010b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d010b-144">RELATED LINKS</span></span>
