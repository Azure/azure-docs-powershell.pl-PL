---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186586"
---
# <span data-ttu-id="302eb-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="302eb-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="302eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="302eb-102">SYNOPSIS</span></span>
<span data-ttu-id="302eb-103">Jeśli element kopii zapasowej zostanie usunięty i będzie obecne w stanie "miękkiego usunięcia", to polecenie przywróci stan, w którym dane zostaną zachowane na zawsze.</span><span class="sxs-lookup"><span data-stu-id="302eb-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="302eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="302eb-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="302eb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="302eb-105">DESCRIPTION</span></span>
<span data-ttu-id="302eb-106">Polecenie Undo-AzRecoveryServicesBackupItemDeletion przywróci stan "miękkiego usunięcia" elementu do stanu, w którym ochrona została zatrzymana, ale dane są zachowywane na zawsze.</span><span class="sxs-lookup"><span data-stu-id="302eb-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="302eb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="302eb-107">EXAMPLES</span></span>

### <span data-ttu-id="302eb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="302eb-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="302eb-109">Pierwsze polecenie pobiera tablicę kontenerów kopii zapasowej, a następnie przechowuje je w $Cont tablicy.</span><span class="sxs-lookup"><span data-stu-id="302eb-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="302eb-110">Drugie polecenie pobiera element kopii zapasowej odpowiadający pierwszeowi elementowi kontenera, a następnie przechowuje go w $PI zmienną.</span><span class="sxs-lookup"><span data-stu-id="302eb-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="302eb-111">Trzecie polecenie wyłącza ochronę kopii zapasowej dla elementu w $PI 0 i umieszcza element w stanie \[ \] softdeleted.</span><span class="sxs-lookup"><span data-stu-id="302eb-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="302eb-112">Czwarte polecenie pobiera element, który znajduje się w stanie softdeleted.</span><span class="sxs-lookup"><span data-stu-id="302eb-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="302eb-113">Ostatnie polecenie przywróci stan softdeleted MASZYNY WIRTUALNEj w stanie, w którym ochrona została zatrzymana, ale dane są zachowywane na zawsze.</span><span class="sxs-lookup"><span data-stu-id="302eb-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="302eb-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="302eb-114">Example 2</span></span>

<span data-ttu-id="302eb-115">Ponowne rozsunienie elementu "miękkiego usunięcia".</span><span class="sxs-lookup"><span data-stu-id="302eb-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="302eb-116">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="302eb-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="302eb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="302eb-117">PARAMETERS</span></span>

### <span data-ttu-id="302eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302eb-118">-DefaultProfile</span></span>
<span data-ttu-id="302eb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="302eb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="302eb-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="302eb-120">-Force</span></span>
<span data-ttu-id="302eb-121">Wymuszanie wyłącza ochronę kopii zapasowej (uniemożliwia okno dialogowe potwierdzenia).</span><span class="sxs-lookup"><span data-stu-id="302eb-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="302eb-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="302eb-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="302eb-123">— element</span><span class="sxs-lookup"><span data-stu-id="302eb-123">-Item</span></span>
<span data-ttu-id="302eb-124">Określa element kopii zapasowej, dla którego to polecenie cmdlet przywróci usunięcie.</span><span class="sxs-lookup"><span data-stu-id="302eb-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="302eb-125">Aby uzyskać element AzureRmRecoveryServicesBackupItem, użyj Get-AzRecoveryServicesBackupItem cmdlet.</span><span class="sxs-lookup"><span data-stu-id="302eb-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="302eb-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="302eb-126">-VaultId</span></span>
<span data-ttu-id="302eb-127">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="302eb-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="302eb-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="302eb-128">-Confirm</span></span>
<span data-ttu-id="302eb-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="302eb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="302eb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="302eb-130">-WhatIf</span></span>
<span data-ttu-id="302eb-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="302eb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="302eb-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="302eb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="302eb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302eb-133">CommonParameters</span></span>
<span data-ttu-id="302eb-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="302eb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302eb-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="302eb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302eb-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="302eb-136">INPUTS</span></span>

### <span data-ttu-id="302eb-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="302eb-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="302eb-138">System.String</span><span class="sxs-lookup"><span data-stu-id="302eb-138">System.String</span></span>

## <span data-ttu-id="302eb-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="302eb-139">OUTPUTS</span></span>

### <span data-ttu-id="302eb-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="302eb-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="302eb-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="302eb-141">NOTES</span></span>

## <span data-ttu-id="302eb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="302eb-142">RELATED LINKS</span></span>

[<span data-ttu-id="302eb-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="302eb-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="302eb-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="302eb-144">Get-AzRecoveryServicesBackupItem</span></span>]()

