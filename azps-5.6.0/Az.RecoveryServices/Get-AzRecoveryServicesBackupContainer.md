---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 0fb1df2d72259c6c0f427a9a66f4cf271cc0cbfa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984289"
---
# <span data-ttu-id="30d98-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="30d98-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="30d98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30d98-102">SYNOPSIS</span></span>

<span data-ttu-id="30d98-103">Pobiera kontenery kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="30d98-103">Gets Backup containers.</span></span>

## <span data-ttu-id="30d98-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="30d98-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30d98-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="30d98-105">DESCRIPTION</span></span>

<span data-ttu-id="30d98-106">Polecenie **cmdlet Get-AzRecoveryServicesBackupContainer** pobiera kontener kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="30d98-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span> <span data-ttu-id="30d98-107">Kontener kopii zapasowej zawiera źródła danych modelowane jako elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="30d98-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="30d98-108">W przypadku typu kontenerowego "Azure VM" dane wyjściowe zawiera listę wszystkich kontenerów, których nazwa jest dokładnie taka sama jak nazwa przekazywana jako wartość parametru Przyjazna nazwa.</span><span class="sxs-lookup"><span data-stu-id="30d98-108">For Container type "Azure VM" , the output lists all the containers whose name exactly matches to the one passed  as the value for Friendly Name parameter.</span></span> <span data-ttu-id="30d98-109">W przypadku innych typów kontenerów dane wyjściowe będą zawierały listę kontenerów o nazwie podobnej do wartości przekazywanej dla parametru Przyjazna nazwa.</span><span class="sxs-lookup"><span data-stu-id="30d98-109">For other container types,  output gives a list of containers with name similar to the value passed for Friendly name parameter.</span></span>
<span data-ttu-id="30d98-110">Ustaw kontekst magazynu przy użyciu parametru -VaultId.</span><span class="sxs-lookup"><span data-stu-id="30d98-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="30d98-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="30d98-111">EXAMPLES</span></span>

### <span data-ttu-id="30d98-112">Przykład 1. Uzyskiwanie określonego kontenera</span><span class="sxs-lookup"><span data-stu-id="30d98-112">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="30d98-113">To polecenie pobiera kontener o nazwie V2VM typu AzureVM.</span><span class="sxs-lookup"><span data-stu-id="30d98-113">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="30d98-114">Przykład 2. Uzyskiwanie wszystkich kontenerów określonego typu</span><span class="sxs-lookup"><span data-stu-id="30d98-114">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="30d98-115">To polecenie pobiera wszystkie kontenery systemu Windows, które są chronione przez agenta kopii zapasowej azure.</span><span class="sxs-lookup"><span data-stu-id="30d98-115">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="30d98-116">Parametr **BackupManagementType** jest wymagany tylko dla kontenerów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="30d98-116">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="30d98-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30d98-117">PARAMETERS</span></span>

### <span data-ttu-id="30d98-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="30d98-118">-BackupManagementType</span></span>

<span data-ttu-id="30d98-119">Klasa zasobów, które są chronione.</span><span class="sxs-lookup"><span data-stu-id="30d98-119">The class of resources being protected.</span></span> <span data-ttu-id="30d98-120">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="30d98-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="30d98-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="30d98-121">AzureVM</span></span>
- <span data-ttu-id="30d98-122">MARS</span><span class="sxs-lookup"><span data-stu-id="30d98-122">MARS</span></span>
- <span data-ttu-id="30d98-123">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="30d98-123">AzureWorkload</span></span>
- <span data-ttu-id="30d98-124">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="30d98-124">AzureStorage</span></span>

<span data-ttu-id="30d98-125">Ten parametr jest używany do odróżniania komputerów z systemem Windows, dla których jest tworzyć kopie zapasowe przy użyciu agenta MARS lub innych aparatów kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="30d98-125">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="30d98-126">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="30d98-126">-ContainerType</span></span>

<span data-ttu-id="30d98-127">Określa typ kontenera kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="30d98-127">Specifies the backup container type.</span></span>
<span data-ttu-id="30d98-128">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="30d98-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="30d98-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="30d98-129">AzureVM</span></span>
- <span data-ttu-id="30d98-130">Windows</span><span class="sxs-lookup"><span data-stu-id="30d98-130">Windows</span></span>
- <span data-ttu-id="30d98-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="30d98-131">AzureStorage</span></span>
- <span data-ttu-id="30d98-132">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="30d98-132">AzureVMAppContainer</span></span>

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

### <span data-ttu-id="30d98-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d98-133">-DefaultProfile</span></span>

<span data-ttu-id="30d98-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="30d98-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30d98-135">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="30d98-135">-FriendlyName</span></span>

<span data-ttu-id="30d98-136">Określa przyjazną nazwę kontenera do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="30d98-136">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="30d98-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30d98-137">-ResourceGroupName</span></span>

<span data-ttu-id="30d98-138">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="30d98-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="30d98-139">Ten parametr jest tylko dla maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="30d98-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="30d98-140">— Status</span><span class="sxs-lookup"><span data-stu-id="30d98-140">-Status</span></span>

<span data-ttu-id="30d98-141">Określa stan rejestracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="30d98-141">Specifies the container registration status.</span></span>
<span data-ttu-id="30d98-142">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="30d98-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="30d98-143">Zarejestrowano</span><span class="sxs-lookup"><span data-stu-id="30d98-143">Registered</span></span>

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

### <span data-ttu-id="30d98-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="30d98-144">-VaultId</span></span>

<span data-ttu-id="30d98-145">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="30d98-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="30d98-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d98-146">CommonParameters</span></span>
<span data-ttu-id="30d98-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30d98-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d98-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30d98-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d98-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30d98-149">INPUTS</span></span>

### <span data-ttu-id="30d98-150">System.String</span><span class="sxs-lookup"><span data-stu-id="30d98-150">System.String</span></span>

## <span data-ttu-id="30d98-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30d98-151">OUTPUTS</span></span>

### <span data-ttu-id="30d98-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="30d98-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="30d98-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="30d98-153">NOTES</span></span>

## <span data-ttu-id="30d98-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30d98-154">RELATED LINKS</span></span>

[<span data-ttu-id="30d98-155">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="30d98-155">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="30d98-156">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="30d98-156">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="30d98-157">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="30d98-157">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
