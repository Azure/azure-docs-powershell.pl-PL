---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: bb0f3b18697b3f9e17b8e1744361346e68c47357
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960250"
---
# <span data-ttu-id="bac80-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="bac80-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="bac80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bac80-102">SYNOPSIS</span></span>
<span data-ttu-id="bac80-103">Wyłącza ochronę elementu chronionego kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="bac80-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="bac80-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bac80-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bac80-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bac80-105">DESCRIPTION</span></span>
<span data-ttu-id="bac80-106">Polecenie **cmdlet Disable-AzRecoveryServicesBackupProtection** wyłącza ochronę elementu chronionego za pomocą kopii zapasowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bac80-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="bac80-107">To polecenie cmdlet zatrzymuje regularną zaplanowaną kopię zapasową elementu.</span><span class="sxs-lookup"><span data-stu-id="bac80-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="bac80-108">To polecenie cmdlet może również usunąć istniejące punkty odzyskiwania elementu kopii zapasowej, jeśli jest wykonywane za pomocą parametru RemoveRecoveryPoints.</span><span class="sxs-lookup"><span data-stu-id="bac80-108">This cmdlet can also delete existing recovery points for the backup item if executed with RemoveRecoveryPoints parameter.</span></span>
<span data-ttu-id="bac80-109">Ustaw kontekst magazynu za pomocą Set-AzRecoveryServicesVaultContext cmdlet przed użyciem bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bac80-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="bac80-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bac80-110">EXAMPLES</span></span>

### <span data-ttu-id="bac80-111">Przykład 1. Wyłączanie ochrony kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="bac80-111">Example 1: Disable Backup protection</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="bac80-112">Pierwsze polecenie pobiera tablicę kontenerów kopii zapasowej, a następnie przechowuje je w $Cont tablicy.</span><span class="sxs-lookup"><span data-stu-id="bac80-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="bac80-113">Drugie polecenie pobiera element kopii zapasowej odpowiadający pierwszeowi elementowi kontenera, a następnie przechowuje go w $PI zmienną.</span><span class="sxs-lookup"><span data-stu-id="bac80-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="bac80-114">Ostatnie polecenie wyłącza ochronę kopii zapasowej elementu w $PI \[ 0, ale \] zachowuje dane.</span><span class="sxs-lookup"><span data-stu-id="bac80-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

### <span data-ttu-id="bac80-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bac80-115">Example 2</span></span>

<span data-ttu-id="bac80-116">Wyłącza ochronę elementu chronionego kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="bac80-116">Disables protection for a Backup-protected item.</span></span> <span data-ttu-id="bac80-117">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="bac80-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints -VaultId $vault.ID
```

## <span data-ttu-id="bac80-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bac80-118">PARAMETERS</span></span>

### <span data-ttu-id="bac80-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac80-119">-DefaultProfile</span></span>
<span data-ttu-id="bac80-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bac80-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bac80-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="bac80-121">-Force</span></span>
<span data-ttu-id="bac80-122">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bac80-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bac80-123">— element</span><span class="sxs-lookup"><span data-stu-id="bac80-123">-Item</span></span>
<span data-ttu-id="bac80-124">Określa element kopii zapasowej, dla którego to polecenie cmdlet wyłącza ochronę.</span><span class="sxs-lookup"><span data-stu-id="bac80-124">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="bac80-125">Aby uzyskać element **AzureRmRecoveryServicesBackupItem,** użyj Get-AzRecoveryServicesBackupItem cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bac80-125">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="bac80-126">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="bac80-126">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="bac80-127">Wskazuje, że to polecenie cmdlet usuwa istniejące punkty odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="bac80-127">Indicates that this cmdlet deletes existing recovery points.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac80-128">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bac80-128">-VaultId</span></span>
<span data-ttu-id="bac80-129">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="bac80-129">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="bac80-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bac80-130">-Confirm</span></span>
<span data-ttu-id="bac80-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bac80-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac80-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bac80-132">-WhatIf</span></span>
<span data-ttu-id="bac80-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bac80-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bac80-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bac80-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac80-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac80-135">CommonParameters</span></span>
<span data-ttu-id="bac80-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bac80-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac80-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bac80-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac80-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bac80-138">INPUTS</span></span>

### <span data-ttu-id="bac80-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="bac80-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="bac80-140">System.String</span><span class="sxs-lookup"><span data-stu-id="bac80-140">System.String</span></span>

## <span data-ttu-id="bac80-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bac80-141">OUTPUTS</span></span>

### <span data-ttu-id="bac80-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="bac80-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="bac80-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bac80-143">NOTES</span></span>

## <span data-ttu-id="bac80-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bac80-144">RELATED LINKS</span></span>

[<span data-ttu-id="bac80-145">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="bac80-145">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="bac80-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bac80-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="bac80-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="bac80-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


