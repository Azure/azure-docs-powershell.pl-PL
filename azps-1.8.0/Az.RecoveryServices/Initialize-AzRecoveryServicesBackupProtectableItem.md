---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 0fd0473cccdf8fbef3d3bab941ab6b3ce7813a63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708643"
---
# <span data-ttu-id="60f02-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="60f02-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="60f02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60f02-102">SYNOPSIS</span></span>
<span data-ttu-id="60f02-103">To polecenie wyzwala odnajdowanie wszelkich niechronionych elementów danego typu obciążenia w danym kontenerze.</span><span class="sxs-lookup"><span data-stu-id="60f02-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="60f02-104">Jeśli aplikacja bazy danych nie jest chroniona automatycznie, użyj tego polecenia, aby odkryć nowe DBs, ilekroć zostaną dodane i kontynuować ochronę.</span><span class="sxs-lookup"><span data-stu-id="60f02-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="60f02-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60f02-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60f02-106">Opis</span><span class="sxs-lookup"><span data-stu-id="60f02-106">DESCRIPTION</span></span>
<span data-ttu-id="60f02-107">polecenie cmdlet bada konkretne obciążenia w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="60f02-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="60f02-108">Spowoduje to wyzwolenie operacji, która tworzy elementy, które mogą być chronione.</span><span class="sxs-lookup"><span data-stu-id="60f02-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="60f02-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60f02-109">EXAMPLES</span></span>

### <span data-ttu-id="60f02-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60f02-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container –WorkloadType “MSSQL”
```

<span data-ttu-id="60f02-111">Polecenie cmdlet wykonuje operację wykrywania nowych elementów chronionych.</span><span class="sxs-lookup"><span data-stu-id="60f02-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="60f02-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60f02-112">PARAMETERS</span></span>

### <span data-ttu-id="60f02-113">-Kontener</span><span class="sxs-lookup"><span data-stu-id="60f02-113">-Container</span></span>
<span data-ttu-id="60f02-114">Kontener, w którym znajduje się element</span><span class="sxs-lookup"><span data-stu-id="60f02-114">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60f02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f02-115">-DefaultProfile</span></span>
<span data-ttu-id="60f02-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60f02-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60f02-117">-VaultId</span><span class="sxs-lookup"><span data-stu-id="60f02-117">-VaultId</span></span>
<span data-ttu-id="60f02-118">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="60f02-118">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="60f02-119">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="60f02-119">-WorkloadType</span></span>
<span data-ttu-id="60f02-120">Typ obciążenia pracą zasobu (na przykład: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="60f02-120">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f02-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f02-121">CommonParameters</span></span>
<span data-ttu-id="60f02-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60f02-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f02-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60f02-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f02-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60f02-124">INPUTS</span></span>

### <span data-ttu-id="60f02-125">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="60f02-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="60f02-126">System. String</span><span class="sxs-lookup"><span data-stu-id="60f02-126">System.String</span></span>

## <span data-ttu-id="60f02-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60f02-127">OUTPUTS</span></span>

### <span data-ttu-id="60f02-128">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="60f02-128">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="60f02-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60f02-129">NOTES</span></span>

## <span data-ttu-id="60f02-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60f02-130">RELATED LINKS</span></span>