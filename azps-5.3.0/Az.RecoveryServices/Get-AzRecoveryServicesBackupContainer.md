---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 90532c6d314c78e6b7242ec480b95991138719de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501375"
---
# <span data-ttu-id="f3d19-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f3d19-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="f3d19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3d19-102">SYNOPSIS</span></span>

<span data-ttu-id="f3d19-103">Pobiera kontenery kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="f3d19-103">Gets Backup containers.</span></span>

## <span data-ttu-id="f3d19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3d19-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3d19-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f3d19-105">DESCRIPTION</span></span>

<span data-ttu-id="f3d19-106">Polecenie cmdlet **Get-AzRecoveryServicesBackupContainer** Pobiera kontener kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="f3d19-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="f3d19-107">Kontener kopii zapasowych hermetyzuje źródła danych, które są modelowane jako elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f3d19-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="f3d19-108">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="f3d19-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="f3d19-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3d19-109">EXAMPLES</span></span>

### <span data-ttu-id="f3d19-110">Przykład 1: uzyskiwanie określonego kontenera</span><span class="sxs-lookup"><span data-stu-id="f3d19-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="f3d19-111">To polecenie uzyskuje kontener o nazwie V2VM typu AzureVM.</span><span class="sxs-lookup"><span data-stu-id="f3d19-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="f3d19-112">Przykład 2: pobieranie wszystkich kontenerów określonego typu</span><span class="sxs-lookup"><span data-stu-id="f3d19-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="f3d19-113">To polecenie pobiera wszystkie kontenery systemu Windows chronione za pomocą agenta kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f3d19-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="f3d19-114">Parametr **BackupManagementType** jest wymagany tylko w przypadku kontenerów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="f3d19-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="f3d19-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3d19-115">PARAMETERS</span></span>

### <span data-ttu-id="f3d19-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="f3d19-116">-BackupManagementType</span></span>

<span data-ttu-id="f3d19-117">Klasa zasobów chronionych.</span><span class="sxs-lookup"><span data-stu-id="f3d19-117">The class of resources being protected.</span></span> <span data-ttu-id="f3d19-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f3d19-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3d19-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f3d19-119">AzureVM</span></span>
- <span data-ttu-id="f3d19-120">OBSŁUGUJE</span><span class="sxs-lookup"><span data-stu-id="f3d19-120">MARS</span></span>
- <span data-ttu-id="f3d19-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="f3d19-121">AzureWorkload</span></span>
- <span data-ttu-id="f3d19-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="f3d19-122">AzureStorage</span></span>

<span data-ttu-id="f3d19-123">Ten parametr służy do rozróżnienia komputerów z systemem Windows, których kopie zapasowe są wykonywane przy użyciu agenta MARS lub innych aparatów kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="f3d19-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureWorkload, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d19-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="f3d19-124">-ContainerType</span></span>

<span data-ttu-id="f3d19-125">Określa typ kontenera kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="f3d19-125">Specifies the backup container type.</span></span>
<span data-ttu-id="f3d19-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f3d19-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3d19-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f3d19-127">AzureVM</span></span>
- <span data-ttu-id="f3d19-128">Microsoft</span><span class="sxs-lookup"><span data-stu-id="f3d19-128">Windows</span></span>
- <span data-ttu-id="f3d19-129">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="f3d19-129">AzureStorage</span></span>
- <span data-ttu-id="f3d19-130">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="f3d19-130">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d19-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d19-131">-DefaultProfile</span></span>

<span data-ttu-id="f3d19-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3d19-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3d19-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f3d19-133">-FriendlyName</span></span>

<span data-ttu-id="f3d19-134">Określa przyjazną nazwę kontenera do pobrania.</span><span class="sxs-lookup"><span data-stu-id="f3d19-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="f3d19-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3d19-135">-ResourceGroupName</span></span>

<span data-ttu-id="f3d19-136">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f3d19-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="f3d19-137">Ten parametr dotyczy tylko maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f3d19-137">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="f3d19-138">-Status</span><span class="sxs-lookup"><span data-stu-id="f3d19-138">-Status</span></span>

<span data-ttu-id="f3d19-139">Określa stan rejestracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="f3d19-139">Specifies the container registration status.</span></span>
<span data-ttu-id="f3d19-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f3d19-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3d19-141">Zarejestrować</span><span class="sxs-lookup"><span data-stu-id="f3d19-141">Registered</span></span>

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

### <span data-ttu-id="f3d19-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f3d19-142">-VaultId</span></span>

<span data-ttu-id="f3d19-143">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="f3d19-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f3d19-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d19-144">CommonParameters</span></span>
<span data-ttu-id="f3d19-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3d19-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d19-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3d19-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d19-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3d19-147">INPUTS</span></span>

### <span data-ttu-id="f3d19-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f3d19-148">System.String</span></span>

## <span data-ttu-id="f3d19-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3d19-149">OUTPUTS</span></span>

### <span data-ttu-id="f3d19-150">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="f3d19-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="f3d19-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3d19-151">NOTES</span></span>

## <span data-ttu-id="f3d19-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3d19-152">RELATED LINKS</span></span>

[<span data-ttu-id="f3d19-153">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f3d19-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="f3d19-154">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="f3d19-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="f3d19-155">Wyrejestrowanie — AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f3d19-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
