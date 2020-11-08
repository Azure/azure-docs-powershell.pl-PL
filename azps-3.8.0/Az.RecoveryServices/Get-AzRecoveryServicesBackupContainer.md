---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: c7efdf68250b0936ffd62293891eb9ebf47ad833
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049855"
---
# <span data-ttu-id="dfe3d-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="dfe3d-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="dfe3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dfe3d-102">SYNOPSIS</span></span>

<span data-ttu-id="dfe3d-103">Pobiera kontenery kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-103">Gets Backup containers.</span></span>

## <span data-ttu-id="dfe3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dfe3d-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfe3d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dfe3d-105">DESCRIPTION</span></span>

<span data-ttu-id="dfe3d-106">Polecenie cmdlet **Get-AzRecoveryServicesBackupContainer** Pobiera kontener kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="dfe3d-107">Kontener kopii zapasowych hermetyzuje źródła danych, które są modelowane jako elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="dfe3d-108">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="dfe3d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dfe3d-109">EXAMPLES</span></span>

### <span data-ttu-id="dfe3d-110">Przykład 1: uzyskiwanie określonego kontenera</span><span class="sxs-lookup"><span data-stu-id="dfe3d-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="dfe3d-111">To polecenie uzyskuje kontener o nazwie V2VM typu AzureVM.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="dfe3d-112">Przykład 2: pobieranie wszystkich kontenerów określonego typu</span><span class="sxs-lookup"><span data-stu-id="dfe3d-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="dfe3d-113">To polecenie pobiera wszystkie kontenery systemu Windows chronione za pomocą agenta kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="dfe3d-114">Parametr **BackupManagementType** jest wymagany tylko w przypadku kontenerów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="dfe3d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dfe3d-115">PARAMETERS</span></span>

### <span data-ttu-id="dfe3d-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="dfe3d-116">-BackupManagementType</span></span>

<span data-ttu-id="dfe3d-117">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-117">Specifies the backup management type.</span></span>
<span data-ttu-id="dfe3d-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dfe3d-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfe3d-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="dfe3d-119">AzureVM</span></span>
- <span data-ttu-id="dfe3d-120">OBSŁUGUJE</span><span class="sxs-lookup"><span data-stu-id="dfe3d-120">MARS</span></span>
- <span data-ttu-id="dfe3d-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="dfe3d-121">AzureSQL</span></span>
- <span data-ttu-id="dfe3d-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="dfe3d-122">AzureStorage</span></span>

<span data-ttu-id="dfe3d-123">Ten parametr służy do rozróżnienia komputerów z systemem Windows, których kopie zapasowe są wykonywane przy użyciu agenta MARS lub innych aparatów kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureSQL, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe3d-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="dfe3d-124">-ContainerType</span></span>

<span data-ttu-id="dfe3d-125">Określa typ kontenera kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-125">Specifies the backup container type.</span></span>
<span data-ttu-id="dfe3d-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dfe3d-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfe3d-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="dfe3d-127">AzureVM</span></span>
- <span data-ttu-id="dfe3d-128">Microsoft</span><span class="sxs-lookup"><span data-stu-id="dfe3d-128">Windows</span></span>
- <span data-ttu-id="dfe3d-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="dfe3d-129">AzureSQL</span></span>
- <span data-ttu-id="dfe3d-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="dfe3d-130">AzureStorage</span></span>
- <span data-ttu-id="dfe3d-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="dfe3d-131">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe3d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe3d-132">-DefaultProfile</span></span>

<span data-ttu-id="dfe3d-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfe3d-134">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="dfe3d-134">-FriendlyName</span></span>

<span data-ttu-id="dfe3d-135">Określa przyjazną nazwę kontenera do pobrania.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-135">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe3d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe3d-136">-ResourceGroupName</span></span>

<span data-ttu-id="dfe3d-137">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="dfe3d-138">Ten parametr dotyczy tylko maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-138">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe3d-139">-Status</span><span class="sxs-lookup"><span data-stu-id="dfe3d-139">-Status</span></span>

<span data-ttu-id="dfe3d-140">Określa stan rejestracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-140">Specifies the container registration status.</span></span>
<span data-ttu-id="dfe3d-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dfe3d-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfe3d-142">Zarejestrować</span><span class="sxs-lookup"><span data-stu-id="dfe3d-142">Registered</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe3d-143">-VaultId</span><span class="sxs-lookup"><span data-stu-id="dfe3d-143">-VaultId</span></span>

<span data-ttu-id="dfe3d-144">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-144">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe3d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe3d-145">CommonParameters</span></span>
<span data-ttu-id="dfe3d-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfe3d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe3d-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfe3d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe3d-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfe3d-148">INPUTS</span></span>

### <span data-ttu-id="dfe3d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="dfe3d-149">System.String</span></span>

## <span data-ttu-id="dfe3d-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dfe3d-150">OUTPUTS</span></span>

### <span data-ttu-id="dfe3d-151">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="dfe3d-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="dfe3d-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dfe3d-152">NOTES</span></span>

## <span data-ttu-id="dfe3d-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dfe3d-153">RELATED LINKS</span></span>

[<span data-ttu-id="dfe3d-154">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="dfe3d-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="dfe3d-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="dfe3d-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="dfe3d-156">Wyrejestrowanie — AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="dfe3d-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
