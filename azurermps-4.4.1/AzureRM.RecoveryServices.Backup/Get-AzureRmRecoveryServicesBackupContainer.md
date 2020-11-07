---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: e6b0633b43bc93c516c9c5b6f4872ecbd6d68520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719005"
---
# <span data-ttu-id="cbd7d-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="cbd7d-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="cbd7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cbd7d-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd7d-103">Pobiera kontenery kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbd7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cbd7d-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbd7d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cbd7d-105">DESCRIPTION</span></span>
<span data-ttu-id="cbd7d-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupContainer** Pobiera kontener kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="cbd7d-107">Kontener kopii zapasowych hermetyzuje źródła danych, które są modelowane jako elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>

<span data-ttu-id="cbd7d-108">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="cbd7d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cbd7d-109">EXAMPLES</span></span>

### <span data-ttu-id="cbd7d-110">Przykład 1: uzyskiwanie określonego kontenera</span><span class="sxs-lookup"><span data-stu-id="cbd7d-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="cbd7d-111">To polecenie uzyskuje kontener o nazwie V2VM typu AzureVM.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="cbd7d-112">Przykład 2: pobieranie wszystkich kontenerów określonego typu</span><span class="sxs-lookup"><span data-stu-id="cbd7d-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="cbd7d-113">To polecenie pobiera wszystkie kontenery systemu Windows chronione za pomocą agenta kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="cbd7d-114">Parametr *BackupManagementType* jest wymagany tylko w przypadku kontenerów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="cbd7d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cbd7d-115">PARAMETERS</span></span>

### <span data-ttu-id="cbd7d-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="cbd7d-116">-BackupManagementType</span></span>
<span data-ttu-id="cbd7d-117">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-117">Specifies the backup management type.</span></span>
<span data-ttu-id="cbd7d-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="cbd7d-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbd7d-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="cbd7d-119">AzureVM</span></span>
- <span data-ttu-id="cbd7d-120">OBSŁUGUJE</span><span class="sxs-lookup"><span data-stu-id="cbd7d-120">MARS</span></span>
- <span data-ttu-id="cbd7d-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="cbd7d-121">AzureSQL</span></span>

<span data-ttu-id="cbd7d-122">Ten parametr służy do rozróżnienia komputerów z systemem Windows, których kopie zapasowe są wykonywane przy użyciu agenta MARS lub innych aparatów kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-122">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, AzureSQL

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd7d-123">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="cbd7d-123">-ContainerType</span></span>
<span data-ttu-id="cbd7d-124">Określa typ kontenera kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-124">Specifies the backup container type.</span></span>
<span data-ttu-id="cbd7d-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="cbd7d-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbd7d-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="cbd7d-126">AzureVM</span></span> 
- <span data-ttu-id="cbd7d-127">Microsoft</span><span class="sxs-lookup"><span data-stu-id="cbd7d-127">Windows</span></span>
- <span data-ttu-id="cbd7d-128">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="cbd7d-128">AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, Windows, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd7d-129">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cbd7d-129">-FriendlyName</span></span>
<span data-ttu-id="cbd7d-130">Określa przyjazną nazwę kontenera do pobrania.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-130">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="cbd7d-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cbd7d-131">-Name</span></span>
<span data-ttu-id="cbd7d-132">Określa nazwę kontenera do pobrania.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-132">Specifies the name of the container to get.</span></span>

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

### <span data-ttu-id="cbd7d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd7d-133">-ResourceGroupName</span></span>
<span data-ttu-id="cbd7d-134">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="cbd7d-135">Ten parametr dotyczy tylko maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-135">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="cbd7d-136">-Status</span><span class="sxs-lookup"><span data-stu-id="cbd7d-136">-Status</span></span>
<span data-ttu-id="cbd7d-137">Określa stan rejestracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-137">Specifies the container registration status.</span></span>
<span data-ttu-id="cbd7d-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="cbd7d-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbd7d-139">Zarejestrować</span><span class="sxs-lookup"><span data-stu-id="cbd7d-139">Registered</span></span>

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

### <span data-ttu-id="cbd7d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd7d-140">-DefaultProfile</span></span>
<span data-ttu-id="cbd7d-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbd7d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd7d-142">CommonParameters</span></span>
<span data-ttu-id="cbd7d-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd7d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd7d-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd7d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd7d-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbd7d-145">INPUTS</span></span>

## <span data-ttu-id="cbd7d-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cbd7d-146">OUTPUTS</span></span>

### <span data-ttu-id="cbd7d-147">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="cbd7d-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="cbd7d-148">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. modele. ContainerBase]</span><span class="sxs-lookup"><span data-stu-id="cbd7d-148">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase]</span></span>

## <span data-ttu-id="cbd7d-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cbd7d-149">NOTES</span></span>

## <span data-ttu-id="cbd7d-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbd7d-150">RELATED LINKS</span></span>

[<span data-ttu-id="cbd7d-151">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="cbd7d-151">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="cbd7d-152">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="cbd7d-152">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="cbd7d-153">Wyrejestrowanie — AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="cbd7d-153">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


