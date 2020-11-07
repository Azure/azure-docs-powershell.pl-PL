---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 6dfff295981ab341d05790e18ed6e4d5c5b0e822
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896142"
---
# <span data-ttu-id="63ff6-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="63ff6-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="63ff6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="63ff6-103">Te polecenia umożliwiają użytkownikom automatyczną ochronę wszystkich istniejących niechronionych DBs oraz wszystkich baz danych, które zostaną dodane później do danych zasad.</span><span class="sxs-lookup"><span data-stu-id="63ff6-103">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="63ff6-104">Usługa Kopia zapasowa Azure będzie regularnie skanowała kontenery chronione automatycznie w poszukiwaniu nowych DBs i automatycznie je chronić.</span><span class="sxs-lookup"><span data-stu-id="63ff6-104">Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="63ff6-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63ff6-105">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63ff6-106">Opis</span><span class="sxs-lookup"><span data-stu-id="63ff6-106">DESCRIPTION</span></span>
<span data-ttu-id="63ff6-107">Polecenie cmdlet **enable-AzRecoveryServicesBackupAutoProtection** ustawia zasady ochrony automatycznego tworzenia kopii zapasowych Azure dotyczące elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="63ff6-107">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets Azure auto Backup protection policy on an protectable item.</span></span>

## <span data-ttu-id="63ff6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63ff6-108">EXAMPLES</span></span>

### <span data-ttu-id="63ff6-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="63ff6-109">Example 1</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL" -Policy $Pol
```

<span data-ttu-id="63ff6-110">Pierwsze polecenie cmdlet Pobiera domyślny obiekt zasad, a następnie zapisuje go w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="63ff6-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="63ff6-111">Drugie polecenie cmdlet ustawia zasady ochrony kopii zapasowych dla AzureWorkload przy użyciu zasad w $Pol.</span><span class="sxs-lookup"><span data-stu-id="63ff6-111">The second cmdlet sets the Backup protection policy for the AzureWorkload using the policy in $Pol.</span></span>

## <span data-ttu-id="63ff6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63ff6-112">PARAMETERS</span></span>

### <span data-ttu-id="63ff6-113">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="63ff6-113">-BackupManagementType</span></span>
<span data-ttu-id="63ff6-114">Typ zarządzania kopią zapasową zasobu (na przykład MAB, DPM, AzureWorkload).</span><span class="sxs-lookup"><span data-stu-id="63ff6-114">Backup Management type of the resource (for example: MAB, DPM, AzureWorkload).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63ff6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ff6-115">-DefaultProfile</span></span>
<span data-ttu-id="63ff6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63ff6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63ff6-117">-InputItem</span><span class="sxs-lookup"><span data-stu-id="63ff6-117">-InputItem</span></span>
<span data-ttu-id="63ff6-118">Określa obiekt elementu, który można chronić, który może zostać przekazany jako dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="63ff6-118">Specifies the protectable item object that can be passed as an input.</span></span>

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

### <span data-ttu-id="63ff6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63ff6-119">-PassThru</span></span>
<span data-ttu-id="63ff6-120">Zwraca wynik automatycznej ochrony.</span><span class="sxs-lookup"><span data-stu-id="63ff6-120">Return the result for auto protection.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63ff6-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="63ff6-121">-Policy</span></span>
<span data-ttu-id="63ff6-122">Obiekt zasad ochrony.</span><span class="sxs-lookup"><span data-stu-id="63ff6-122">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63ff6-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="63ff6-123">-VaultId</span></span>
<span data-ttu-id="63ff6-124">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="63ff6-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="63ff6-125">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="63ff6-125">-WorkloadType</span></span>
<span data-ttu-id="63ff6-126">Typ obciążenia pracą zasobu (na przykład: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="63ff6-126">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63ff6-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63ff6-127">-Confirm</span></span>
<span data-ttu-id="63ff6-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63ff6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63ff6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63ff6-129">-WhatIf</span></span>
<span data-ttu-id="63ff6-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63ff6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63ff6-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63ff6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63ff6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ff6-132">CommonParameters</span></span>
<span data-ttu-id="63ff6-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63ff6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ff6-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63ff6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ff6-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63ff6-135">INPUTS</span></span>

### <span data-ttu-id="63ff6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="63ff6-136">System.String</span></span>

## <span data-ttu-id="63ff6-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63ff6-137">OUTPUTS</span></span>

### <span data-ttu-id="63ff6-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="63ff6-138">System.Object</span></span>

## <span data-ttu-id="63ff6-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63ff6-139">NOTES</span></span>

## <span data-ttu-id="63ff6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63ff6-140">RELATED LINKS</span></span>
