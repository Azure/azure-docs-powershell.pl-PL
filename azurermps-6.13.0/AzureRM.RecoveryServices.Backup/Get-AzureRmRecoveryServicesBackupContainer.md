---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c47c3e51d970302281af5a7ae3a6175f4af79739
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718287"
---
# <span data-ttu-id="315bd-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="315bd-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="315bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="315bd-102">SYNOPSIS</span></span>
<span data-ttu-id="315bd-103">Pobiera kontenery kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="315bd-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="315bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="315bd-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="315bd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="315bd-105">DESCRIPTION</span></span>
<span data-ttu-id="315bd-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupContainer** Pobiera kontener kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="315bd-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="315bd-107">Kontener kopii zapasowych hermetyzuje źródła danych, które są modelowane jako elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="315bd-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="315bd-108">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="315bd-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="315bd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="315bd-109">EXAMPLES</span></span>

### <span data-ttu-id="315bd-110">Przykład 1: uzyskiwanie określonego kontenera</span><span class="sxs-lookup"><span data-stu-id="315bd-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="315bd-111">To polecenie uzyskuje kontener o nazwie V2VM typu AzureVM.</span><span class="sxs-lookup"><span data-stu-id="315bd-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="315bd-112">Przykład 2: pobieranie wszystkich kontenerów określonego typu</span><span class="sxs-lookup"><span data-stu-id="315bd-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="315bd-113">To polecenie pobiera wszystkie kontenery systemu Windows chronione za pomocą agenta kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="315bd-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="315bd-114">Parametr *BackupManagementType* jest wymagany tylko w przypadku kontenerów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="315bd-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="315bd-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="315bd-115">PARAMETERS</span></span>

### <span data-ttu-id="315bd-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="315bd-116">-BackupManagementType</span></span>
<span data-ttu-id="315bd-117">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="315bd-117">Specifies the backup management type.</span></span>
<span data-ttu-id="315bd-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="315bd-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="315bd-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="315bd-119">AzureVM</span></span>
- <span data-ttu-id="315bd-120">OBSŁUGUJE</span><span class="sxs-lookup"><span data-stu-id="315bd-120">MARS</span></span>
- <span data-ttu-id="315bd-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="315bd-121">AzureSQL</span></span>
- <span data-ttu-id="315bd-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="315bd-122">AzureStorage</span></span>

<span data-ttu-id="315bd-123">Ten parametr służy do rozróżnienia komputerów z systemem Windows, których kopie zapasowe są wykonywane przy użyciu agenta MARS lub innych aparatów kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="315bd-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="315bd-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="315bd-124">-ContainerType</span></span>
<span data-ttu-id="315bd-125">Określa typ kontenera kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="315bd-125">Specifies the backup container type.</span></span>
<span data-ttu-id="315bd-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="315bd-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="315bd-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="315bd-127">AzureVM</span></span> 
- <span data-ttu-id="315bd-128">Microsoft</span><span class="sxs-lookup"><span data-stu-id="315bd-128">Windows</span></span>
- <span data-ttu-id="315bd-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="315bd-129">AzureSQL</span></span>
- <span data-ttu-id="315bd-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="315bd-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="315bd-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="315bd-131">-DefaultProfile</span></span>
<span data-ttu-id="315bd-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="315bd-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="315bd-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="315bd-133">-FriendlyName</span></span>
<span data-ttu-id="315bd-134">Określa przyjazną nazwę kontenera do pobrania.</span><span class="sxs-lookup"><span data-stu-id="315bd-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="315bd-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="315bd-135">-Name</span></span>
<span data-ttu-id="315bd-136">Określa nazwę kontenera do pobrania.</span><span class="sxs-lookup"><span data-stu-id="315bd-136">Specifies the name of the container to get.</span></span>

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

### <span data-ttu-id="315bd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="315bd-137">-ResourceGroupName</span></span>
<span data-ttu-id="315bd-138">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="315bd-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="315bd-139">Ten parametr dotyczy tylko maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="315bd-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="315bd-140">-Status</span><span class="sxs-lookup"><span data-stu-id="315bd-140">-Status</span></span>
<span data-ttu-id="315bd-141">Określa stan rejestracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="315bd-141">Specifies the container registration status.</span></span>
<span data-ttu-id="315bd-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="315bd-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="315bd-143">Zarejestrować</span><span class="sxs-lookup"><span data-stu-id="315bd-143">Registered</span></span>

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

### <span data-ttu-id="315bd-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="315bd-144">-VaultId</span></span>
<span data-ttu-id="315bd-145">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="315bd-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="315bd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="315bd-146">CommonParameters</span></span>
<span data-ttu-id="315bd-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="315bd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="315bd-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="315bd-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="315bd-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="315bd-149">INPUTS</span></span>

### <span data-ttu-id="315bd-150">System. String</span><span class="sxs-lookup"><span data-stu-id="315bd-150">System.String</span></span>
<span data-ttu-id="315bd-151">Parametry: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="315bd-151">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="315bd-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="315bd-152">OUTPUTS</span></span>

### <span data-ttu-id="315bd-153">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="315bd-153">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="315bd-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="315bd-154">NOTES</span></span>

## <span data-ttu-id="315bd-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="315bd-155">RELATED LINKS</span></span>

[<span data-ttu-id="315bd-156">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="315bd-156">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="315bd-157">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="315bd-157">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="315bd-158">Wyrejestrowanie — AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="315bd-158">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


