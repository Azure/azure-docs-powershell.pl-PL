---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: bd4945436c840323121be7a4450a0042acf67cde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183938"
---
# <span data-ttu-id="f6d90-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f6d90-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="f6d90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6d90-102">SYNOPSIS</span></span>

<span data-ttu-id="f6d90-103">Pobiera kontenery kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f6d90-103">Gets Backup containers.</span></span>

## <span data-ttu-id="f6d90-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f6d90-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6d90-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f6d90-105">DESCRIPTION</span></span>

<span data-ttu-id="f6d90-106">Polecenie **cmdlet Get-AzRecoveryServicesBackupContainer** pobiera kontener kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f6d90-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span> <span data-ttu-id="f6d90-107">Kontener kopii zapasowej zawiera źródła danych modelowane jako elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f6d90-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="f6d90-108">W przypadku typu kontenerowego "Azure VM" dane wyjściowe zawiera listę wszystkich kontenerów, których nazwa jest dokładnie taka sama jak nazwa przekazywana jako wartość parametru Przyjazna nazwa.</span><span class="sxs-lookup"><span data-stu-id="f6d90-108">For Container type "Azure VM" , the output lists all the containers whose name exactly matches to the one passed  as the value for Friendly Name parameter.</span></span> <span data-ttu-id="f6d90-109">W przypadku innych typów kontenerów dane wyjściowe dają listę kontenerów o nazwie podobnej do wartości przekazywanej dla parametru Przyjazna nazwa.</span><span class="sxs-lookup"><span data-stu-id="f6d90-109">For other container types,  output gives a list of containers with name similar to the value passed for Friendly name parameter.</span></span>
<span data-ttu-id="f6d90-110">Ustaw kontekst magazynu przy użyciu parametru -VaultId.</span><span class="sxs-lookup"><span data-stu-id="f6d90-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="f6d90-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f6d90-111">EXAMPLES</span></span>

### <span data-ttu-id="f6d90-112">Przykład 1. Uzyskiwanie określonego kontenera</span><span class="sxs-lookup"><span data-stu-id="f6d90-112">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="f6d90-113">To polecenie pobiera kontener o nazwie V2VM typu AzureVM.</span><span class="sxs-lookup"><span data-stu-id="f6d90-113">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="f6d90-114">Przykład 2. Uzyskiwanie wszystkich kontenerów określonego typu</span><span class="sxs-lookup"><span data-stu-id="f6d90-114">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="f6d90-115">To polecenie pobiera wszystkie kontenery systemu Windows, które są chronione przez agenta kopii zapasowej azure.</span><span class="sxs-lookup"><span data-stu-id="f6d90-115">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="f6d90-116">Parametr **BackupManagementType jest** wymagany tylko dla kontenerów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="f6d90-116">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="f6d90-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6d90-117">PARAMETERS</span></span>

### <span data-ttu-id="f6d90-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="f6d90-118">-BackupManagementType</span></span>

<span data-ttu-id="f6d90-119">Klasa zasobów, które są chronione.</span><span class="sxs-lookup"><span data-stu-id="f6d90-119">The class of resources being protected.</span></span> <span data-ttu-id="f6d90-120">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f6d90-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6d90-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f6d90-121">AzureVM</span></span>
- <span data-ttu-id="f6d90-122">MARS</span><span class="sxs-lookup"><span data-stu-id="f6d90-122">MARS</span></span>
- <span data-ttu-id="f6d90-123">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="f6d90-123">AzureWorkload</span></span>
- <span data-ttu-id="f6d90-124">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="f6d90-124">AzureStorage</span></span>

<span data-ttu-id="f6d90-125">Ten parametr jest używany do odróżniania komputerów z systemem Windows, dla których jest tworzyć kopie zapasowe przy użyciu agenta MARS lub innych aparatów kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="f6d90-125">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="f6d90-126">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="f6d90-126">-ContainerType</span></span>

<span data-ttu-id="f6d90-127">Określa typ kontenera kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f6d90-127">Specifies the backup container type.</span></span>
<span data-ttu-id="f6d90-128">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f6d90-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6d90-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f6d90-129">AzureVM</span></span>
- <span data-ttu-id="f6d90-130">Windows</span><span class="sxs-lookup"><span data-stu-id="f6d90-130">Windows</span></span>
- <span data-ttu-id="f6d90-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="f6d90-131">AzureStorage</span></span>
- <span data-ttu-id="f6d90-132">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="f6d90-132">AzureVMAppContainer</span></span>

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

### <span data-ttu-id="f6d90-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d90-133">-DefaultProfile</span></span>

<span data-ttu-id="f6d90-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6d90-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6d90-135">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f6d90-135">-FriendlyName</span></span>

<span data-ttu-id="f6d90-136">Określa przyjazną nazwę kontenera do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="f6d90-136">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="f6d90-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6d90-137">-ResourceGroupName</span></span>

<span data-ttu-id="f6d90-138">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6d90-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="f6d90-139">Ten parametr jest tylko dla maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f6d90-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="f6d90-140">— Status</span><span class="sxs-lookup"><span data-stu-id="f6d90-140">-Status</span></span>

<span data-ttu-id="f6d90-141">Określa stan rejestracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="f6d90-141">Specifies the container registration status.</span></span>
<span data-ttu-id="f6d90-142">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f6d90-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6d90-143">Zarejestrowano</span><span class="sxs-lookup"><span data-stu-id="f6d90-143">Registered</span></span>

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

### <span data-ttu-id="f6d90-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f6d90-144">-VaultId</span></span>

<span data-ttu-id="f6d90-145">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="f6d90-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f6d90-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d90-146">CommonParameters</span></span>
<span data-ttu-id="f6d90-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6d90-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d90-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6d90-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d90-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6d90-149">INPUTS</span></span>

### <span data-ttu-id="f6d90-150">System.String</span><span class="sxs-lookup"><span data-stu-id="f6d90-150">System.String</span></span>

## <span data-ttu-id="f6d90-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6d90-151">OUTPUTS</span></span>

### <span data-ttu-id="f6d90-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="f6d90-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="f6d90-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f6d90-153">NOTES</span></span>

## <span data-ttu-id="f6d90-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6d90-154">RELATED LINKS</span></span>

[<span data-ttu-id="f6d90-155">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f6d90-155">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="f6d90-156">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="f6d90-156">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="f6d90-157">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f6d90-157">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
