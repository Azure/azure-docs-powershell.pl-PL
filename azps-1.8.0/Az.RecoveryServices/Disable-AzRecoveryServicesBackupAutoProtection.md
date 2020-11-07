---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 2613761db4a975f1bd4e04458ccdc5df81c0a2d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708727"
---
# <span data-ttu-id="2ed06-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="2ed06-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="2ed06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ed06-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed06-103">Wyłącza automatyczne tworzenie kopii zapasowej dla elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="2ed06-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="2ed06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ed06-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ed06-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ed06-105">DESCRIPTION</span></span>
<span data-ttu-id="2ed06-106">Polecenie cmdlet **disable-AzRecoveryServicesBackupAutoProtection** wyłącza ochronę elementu z ochroną.</span><span class="sxs-lookup"><span data-stu-id="2ed06-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="2ed06-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ed06-107">EXAMPLES</span></span>

### <span data-ttu-id="2ed06-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ed06-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="2ed06-109">Pierwsze polecenie cmdlet wyłącza zasady ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="2ed06-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="2ed06-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ed06-110">PARAMETERS</span></span>

### <span data-ttu-id="2ed06-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="2ed06-111">-BackupManagementType</span></span>
<span data-ttu-id="2ed06-112">Typ zarządzania kopią zapasową zasobu (na przykład MAB, DPM).</span><span class="sxs-lookup"><span data-stu-id="2ed06-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed06-113">-DefaultProfile</span></span>
<span data-ttu-id="2ed06-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed06-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed06-115">-InputItem</span><span class="sxs-lookup"><span data-stu-id="2ed06-115">-InputItem</span></span>
<span data-ttu-id="2ed06-116">Identyfikator elementu</span><span class="sxs-lookup"><span data-stu-id="2ed06-116">Item Id</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ed06-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ed06-117">-PassThru</span></span>
<span data-ttu-id="2ed06-118">Zwraca wynik automatycznej ochrony.</span><span class="sxs-lookup"><span data-stu-id="2ed06-118">Return the result for auto protection.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed06-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2ed06-119">-VaultId</span></span>
<span data-ttu-id="2ed06-120">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2ed06-120">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ed06-121">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="2ed06-121">-WorkloadType</span></span>
<span data-ttu-id="2ed06-122">Typ obciążenia pracą zasobu (na przykład: AzureVM, WindowsServer, AzureFiles).</span><span class="sxs-lookup"><span data-stu-id="2ed06-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed06-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ed06-123">-Confirm</span></span>
<span data-ttu-id="2ed06-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ed06-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed06-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ed06-125">-WhatIf</span></span>
<span data-ttu-id="2ed06-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ed06-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ed06-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2ed06-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed06-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed06-128">CommonParameters</span></span>
<span data-ttu-id="2ed06-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ed06-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2ed06-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed06-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed06-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ed06-131">INPUTS</span></span>

### <span data-ttu-id="2ed06-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2ed06-132">System.String</span></span>

## <span data-ttu-id="2ed06-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ed06-133">OUTPUTS</span></span>

### <span data-ttu-id="2ed06-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ed06-134">System.Boolean</span></span>

## <span data-ttu-id="2ed06-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ed06-135">NOTES</span></span>

## <span data-ttu-id="2ed06-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ed06-136">RELATED LINKS</span></span>
