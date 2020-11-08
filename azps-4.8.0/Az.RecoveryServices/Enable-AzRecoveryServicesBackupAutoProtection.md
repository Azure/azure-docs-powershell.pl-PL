---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: e47ed3d2859a78837c57803789721005a5248204
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219295"
---
# <span data-ttu-id="4312b-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="4312b-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="4312b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4312b-102">SYNOPSIS</span></span>
<span data-ttu-id="4312b-103">Polecenie cmdlet **enable-AzRecoveryServicesBackupAutoProtection** konfiguruje automatyczną ochronę bieżących i przyszłych DBS SQL w danym wystąpieniu za pomocą podanych zasad.</span><span class="sxs-lookup"><span data-stu-id="4312b-103">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets up automatic protection of current and any future SQL DBs within the given instance with the supplied policy.</span></span>

## <span data-ttu-id="4312b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4312b-104">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4312b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4312b-105">DESCRIPTION</span></span>
<span data-ttu-id="4312b-106">To polecenie umożliwia użytkownikom automatyczną ochronę wszystkich istniejących niechronionych DBs SQL oraz wszystkich baz danych, które zostaną dodane później do danych zasad.</span><span class="sxs-lookup"><span data-stu-id="4312b-106">This command allows users to automatically protect all existing unprotected SQL DBs and any DB which will be added later with the given policy.</span></span>  <span data-ttu-id="4312b-107">Ponieważ instrukcja jest operacją tworzenia kopii zapasowej wszystkich przyszłych DBs, operacja jest wykonywana na poziomie SQLInstance, usługa kopia zapasowa Azure będzie regularnie skanować kontenery chronione automatycznie w poszukiwaniu nowych DBs i automatycznie je chronić.</span><span class="sxs-lookup"><span data-stu-id="4312b-107">Since the instruction is to back up all future DBs, the operation is done at a SQLInstance level, Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="4312b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4312b-108">EXAMPLES</span></span>

### <span data-ttu-id="4312b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4312b-109">Example 1</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultSQLPolicy"
PS C:\> $SQLInstance = Get-AzRecoveryServicesBackupProtectableItem -workloadType MSSQL -ItemType SQLInstance -VaultId $targetVault.ID -Name "MSSQLInstance" -ServerName "TestSQLServer" 
PS C:\> Enable-AzRecoveryServicesBackupAutoProtection -InputItem $SQLInstance -BackupManagementType AzureWorkload -WorkloadType MSSQL -Policy $Pol -VaultId $targetvault.ID 
```

<span data-ttu-id="4312b-110">Pierwsze polecenie cmdlet Pobiera domyślny obiekt zasad, a następnie zapisuje go w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="4312b-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="4312b-111">Drugie polecenie cmdlet pobiera odpowiednie wystąpienie SQL, które jest elementem z ochroną.</span><span class="sxs-lookup"><span data-stu-id="4312b-111">The second cmdlet fetches the relevant SQLInstance which is a protectable item.</span></span> <span data-ttu-id="4312b-112">Polecenie trzecia konfiguruje automatyczną ochronę tego wystąpienia przy użyciu zasad w $Pol.</span><span class="sxs-lookup"><span data-stu-id="4312b-112">The 3rd command then sets up auto protection for this instance using the policy in $Pol.</span></span>

### <span data-ttu-id="4312b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4312b-113">Example 2</span></span>

<span data-ttu-id="4312b-114">Te polecenia umożliwiają użytkownikom automatyczną ochronę wszystkich istniejących niechronionych DBs oraz wszystkich baz danych, które zostaną dodane później do danych zasad.</span><span class="sxs-lookup"><span data-stu-id="4312b-114">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="4312b-115">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="4312b-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType AzureVM -InputItem <ProtectableItemBase> -Policy $Pol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="4312b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4312b-116">PARAMETERS</span></span>

### <span data-ttu-id="4312b-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="4312b-117">-BackupManagementType</span></span>
<span data-ttu-id="4312b-118">Klasa zasobów chronionych.</span><span class="sxs-lookup"><span data-stu-id="4312b-118">The class of resources being protected.</span></span> <span data-ttu-id="4312b-119">Obecnie obsługiwane są wartości dla tego polecenia cmdlet to MAB, AzureWorkload, AzureVM</span><span class="sxs-lookup"><span data-stu-id="4312b-119">Currently the values supported for this cmdlet are MAB, AzureWorkload, AzureVM</span></span>

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

### <span data-ttu-id="4312b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4312b-120">-DefaultProfile</span></span>
<span data-ttu-id="4312b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4312b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4312b-122">-InputItem</span><span class="sxs-lookup"><span data-stu-id="4312b-122">-InputItem</span></span>
<span data-ttu-id="4312b-123">Określa obiekt elementu, który można chronić, który może zostać przekazany jako dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="4312b-123">Specifies the protectable item object that can be passed as an input.</span></span> <span data-ttu-id="4312b-124">Bieżąca obsługiwana wartość jest obiektem protectableItem typu "SQLInstance".</span><span class="sxs-lookup"><span data-stu-id="4312b-124">The current supported value is a protectableItem object of type "SQLInstance".</span></span> 

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

### <span data-ttu-id="4312b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4312b-125">-PassThru</span></span>
<span data-ttu-id="4312b-126">Zwraca wynik automatycznej ochrony.</span><span class="sxs-lookup"><span data-stu-id="4312b-126">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="4312b-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="4312b-127">-Policy</span></span>
<span data-ttu-id="4312b-128">Obiekt zasad ochrony.</span><span class="sxs-lookup"><span data-stu-id="4312b-128">Protection policy object.</span></span>

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

### <span data-ttu-id="4312b-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4312b-129">-VaultId</span></span>
<span data-ttu-id="4312b-130">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="4312b-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4312b-131">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="4312b-131">-WorkloadType</span></span>
<span data-ttu-id="4312b-132">Typ obciążenia pracą zasobu.</span><span class="sxs-lookup"><span data-stu-id="4312b-132">Workload type of the resource.</span></span> <span data-ttu-id="4312b-133">Bieżące obsługiwane wartości to AzureVM, WindowsServer, MSSQL</span><span class="sxs-lookup"><span data-stu-id="4312b-133">The current supported values are AzureVM, WindowsServer, MSSQL</span></span>

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

### <span data-ttu-id="4312b-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4312b-134">-Confirm</span></span>
<span data-ttu-id="4312b-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4312b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4312b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4312b-136">-WhatIf</span></span>
<span data-ttu-id="4312b-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4312b-137">Shows what would happen if the cmdlet runs.</span></span>


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

### <span data-ttu-id="4312b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4312b-138">CommonParameters</span></span>
<span data-ttu-id="4312b-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4312b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4312b-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4312b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4312b-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4312b-141">INPUTS</span></span>

### <span data-ttu-id="4312b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4312b-142">System.String</span></span>

## <span data-ttu-id="4312b-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4312b-143">OUTPUTS</span></span>

### <span data-ttu-id="4312b-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="4312b-144">System.Object</span></span>

## <span data-ttu-id="4312b-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4312b-145">NOTES</span></span>

## <span data-ttu-id="4312b-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4312b-146">RELATED LINKS</span></span>
