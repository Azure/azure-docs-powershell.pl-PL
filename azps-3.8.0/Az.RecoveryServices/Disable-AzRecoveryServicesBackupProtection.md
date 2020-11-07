---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: d0b2d15b3f2515969e423e8ac8d019a1413fcad7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896281"
---
# <span data-ttu-id="61073-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="61073-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="61073-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61073-102">SYNOPSIS</span></span>
<span data-ttu-id="61073-103">Wyłącza ochronę elementu chronionego kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="61073-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="61073-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61073-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61073-105">Opis</span><span class="sxs-lookup"><span data-stu-id="61073-105">DESCRIPTION</span></span>
<span data-ttu-id="61073-106">Polecenie cmdlet **disable-AzRecoveryServicesBackupProtection** wyłącza ochronę elementu chronionego usługą Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="61073-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="61073-107">To polecenie cmdlet zatrzymuje regularne Planowanie kopii zapasowej elementu.</span><span class="sxs-lookup"><span data-stu-id="61073-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="61073-108">To polecenie cmdlet umożliwia również usunięcie istniejących punktów odzyskiwania dla elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="61073-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="61073-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="61073-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="61073-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61073-110">EXAMPLES</span></span>

### <span data-ttu-id="61073-111">Przykład 1: Wyłączanie ochrony przed kopiami zapasowymi</span><span class="sxs-lookup"><span data-stu-id="61073-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="61073-112">Pierwsze polecenie uzyskuje tablicę kontenerów kopii zapasowych, a następnie zapisuje je w tablicy $Cont.</span><span class="sxs-lookup"><span data-stu-id="61073-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="61073-113">Drugie polecenie pobiera element kopii zapasowej odpowiadający pierwszemu kontenerowi, a następnie zapisuje go w zmiennej $PI.</span><span class="sxs-lookup"><span data-stu-id="61073-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="61073-114">Ostatnie polecenie wyłącza ochronę kopii zapasowych elementu w $PI \[ 0 \] , ale zachowuje dane.</span><span class="sxs-lookup"><span data-stu-id="61073-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="61073-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61073-115">PARAMETERS</span></span>

### <span data-ttu-id="61073-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61073-116">-DefaultProfile</span></span>
<span data-ttu-id="61073-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="61073-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61073-118">-Force</span><span class="sxs-lookup"><span data-stu-id="61073-118">-Force</span></span>
<span data-ttu-id="61073-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="61073-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="61073-120">-Item</span><span class="sxs-lookup"><span data-stu-id="61073-120">-Item</span></span>
<span data-ttu-id="61073-121">Określa element kopii zapasowej, dla którego to polecenie cmdlet wyłącza ochronę.</span><span class="sxs-lookup"><span data-stu-id="61073-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="61073-122">Aby uzyskać **AzureRmRecoveryServicesBackupItem** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="61073-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="61073-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="61073-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="61073-124">Wskazuje, że to polecenie cmdlet usuwa istniejące punkty odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="61073-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="61073-125">Aby później usunąć zapisane punkty odzyskiwania, uruchom ponownie to polecenie cmdlet i określ ten parametr.</span><span class="sxs-lookup"><span data-stu-id="61073-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="61073-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="61073-126">-VaultId</span></span>
<span data-ttu-id="61073-127">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="61073-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="61073-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61073-128">-Confirm</span></span>
<span data-ttu-id="61073-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61073-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61073-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61073-130">-WhatIf</span></span>
<span data-ttu-id="61073-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61073-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61073-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="61073-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61073-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61073-133">CommonParameters</span></span>
<span data-ttu-id="61073-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61073-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61073-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61073-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61073-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61073-136">INPUTS</span></span>

### <span data-ttu-id="61073-137">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="61073-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="61073-138">System. String</span><span class="sxs-lookup"><span data-stu-id="61073-138">System.String</span></span>

## <span data-ttu-id="61073-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61073-139">OUTPUTS</span></span>

### <span data-ttu-id="61073-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="61073-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="61073-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61073-141">NOTES</span></span>

## <span data-ttu-id="61073-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61073-142">RELATED LINKS</span></span>

[<span data-ttu-id="61073-143">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="61073-143">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="61073-144">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="61073-144">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="61073-145">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="61073-145">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


