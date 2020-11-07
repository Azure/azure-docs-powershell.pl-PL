---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 73438a3f294aaece7c4649f53559311d95ef4aa0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708680"
---
# <span data-ttu-id="70ca5-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="70ca5-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="70ca5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="70ca5-103">Pobiera kontenery kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="70ca5-103">Gets Backup containers.</span></span>

## <span data-ttu-id="70ca5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70ca5-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70ca5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70ca5-105">DESCRIPTION</span></span>
<span data-ttu-id="70ca5-106">Polecenie cmdlet **Get-AzRecoveryServicesBackupContainer** Pobiera kontener kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="70ca5-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="70ca5-107">Kontener kopii zapasowych hermetyzuje źródła danych, które są modelowane jako elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="70ca5-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="70ca5-108">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="70ca5-108">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="70ca5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70ca5-109">EXAMPLES</span></span>

### <span data-ttu-id="70ca5-110">Przykład 1: uzyskiwanie określonego kontenera</span><span class="sxs-lookup"><span data-stu-id="70ca5-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="70ca5-111">To polecenie uzyskuje kontener o nazwie V2VM typu AzureVM.</span><span class="sxs-lookup"><span data-stu-id="70ca5-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="70ca5-112">Przykład 2: pobieranie wszystkich kontenerów określonego typu</span><span class="sxs-lookup"><span data-stu-id="70ca5-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="70ca5-113">To polecenie pobiera wszystkie kontenery systemu Windows chronione za pomocą agenta kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="70ca5-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="70ca5-114">Parametr *BackupManagementType* jest wymagany tylko w przypadku kontenerów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="70ca5-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="70ca5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70ca5-115">PARAMETERS</span></span>

### <span data-ttu-id="70ca5-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="70ca5-116">-BackupManagementType</span></span>
<span data-ttu-id="70ca5-117">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="70ca5-117">Specifies the backup management type.</span></span>
<span data-ttu-id="70ca5-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="70ca5-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="70ca5-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="70ca5-119">AzureVM</span></span>
- <span data-ttu-id="70ca5-120">OBSŁUGUJE</span><span class="sxs-lookup"><span data-stu-id="70ca5-120">MARS</span></span>
- <span data-ttu-id="70ca5-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="70ca5-121">AzureSQL</span></span>
- <span data-ttu-id="70ca5-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="70ca5-122">AzureStorage</span></span>

<span data-ttu-id="70ca5-123">Ten parametr służy do rozróżnienia komputerów z systemem Windows, których kopie zapasowe są wykonywane przy użyciu agenta MARS lub innych aparatów kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="70ca5-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="70ca5-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="70ca5-124">-ContainerType</span></span>
<span data-ttu-id="70ca5-125">Określa typ kontenera kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="70ca5-125">Specifies the backup container type.</span></span>
<span data-ttu-id="70ca5-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="70ca5-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="70ca5-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="70ca5-127">AzureVM</span></span> 
- <span data-ttu-id="70ca5-128">Microsoft</span><span class="sxs-lookup"><span data-stu-id="70ca5-128">Windows</span></span>
- <span data-ttu-id="70ca5-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="70ca5-129">AzureSQL</span></span>
- <span data-ttu-id="70ca5-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="70ca5-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ca5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ca5-131">-DefaultProfile</span></span>
<span data-ttu-id="70ca5-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70ca5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70ca5-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="70ca5-133">-FriendlyName</span></span>
<span data-ttu-id="70ca5-134">Określa przyjazną nazwę kontenera do pobrania.</span><span class="sxs-lookup"><span data-stu-id="70ca5-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="70ca5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70ca5-135">-ResourceGroupName</span></span>
<span data-ttu-id="70ca5-136">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70ca5-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="70ca5-137">Ten parametr dotyczy tylko maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="70ca5-137">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="70ca5-138">-Status</span><span class="sxs-lookup"><span data-stu-id="70ca5-138">-Status</span></span>
<span data-ttu-id="70ca5-139">Określa stan rejestracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="70ca5-139">Specifies the container registration status.</span></span>
<span data-ttu-id="70ca5-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="70ca5-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="70ca5-141">Zarejestrować</span><span class="sxs-lookup"><span data-stu-id="70ca5-141">Registered</span></span>

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

### <span data-ttu-id="70ca5-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="70ca5-142">-VaultId</span></span>
<span data-ttu-id="70ca5-143">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="70ca5-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="70ca5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ca5-144">CommonParameters</span></span>
<span data-ttu-id="70ca5-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ca5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ca5-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70ca5-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ca5-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70ca5-147">INPUTS</span></span>

### <span data-ttu-id="70ca5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="70ca5-148">System.String</span></span>

## <span data-ttu-id="70ca5-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70ca5-149">OUTPUTS</span></span>

### <span data-ttu-id="70ca5-150">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="70ca5-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="70ca5-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70ca5-151">NOTES</span></span>

## <span data-ttu-id="70ca5-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70ca5-152">RELATED LINKS</span></span>

[<span data-ttu-id="70ca5-153">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="70ca5-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="70ca5-154">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="70ca5-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="70ca5-155">Wyrejestrowanie — AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="70ca5-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)

