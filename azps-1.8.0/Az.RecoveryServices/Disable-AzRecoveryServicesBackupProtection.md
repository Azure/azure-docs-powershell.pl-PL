---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 4c023de04cb431e18dc027c0ca3563aa6a2410e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708728"
---
# <span data-ttu-id="77bfc-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="77bfc-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="77bfc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="77bfc-103">Wyłącza ochronę elementu chronionego kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="77bfc-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="77bfc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77bfc-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77bfc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77bfc-105">DESCRIPTION</span></span>
<span data-ttu-id="77bfc-106">Polecenie cmdlet **disable-AzRecoveryServicesBackupProtection** wyłącza ochronę elementu chronionego usługą Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="77bfc-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="77bfc-107">To polecenie cmdlet zatrzymuje regularne Planowanie kopii zapasowej elementu.</span><span class="sxs-lookup"><span data-stu-id="77bfc-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="77bfc-108">To polecenie cmdlet umożliwia również usunięcie istniejących punktów odzyskiwania dla elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="77bfc-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="77bfc-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="77bfc-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="77bfc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77bfc-110">EXAMPLES</span></span>

### <span data-ttu-id="77bfc-111">Przykład 1: Wyłączanie ochrony przed kopiami zapasowymi</span><span class="sxs-lookup"><span data-stu-id="77bfc-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="77bfc-112">Pierwsze polecenie uzyskuje tablicę kontenerów kopii zapasowych, a następnie zapisuje je w tablicy $Cont.</span><span class="sxs-lookup"><span data-stu-id="77bfc-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="77bfc-113">Drugie polecenie pobiera element kopii zapasowej odpowiadający pierwszemu kontenerowi, a następnie zapisuje go w zmiennej $PI.</span><span class="sxs-lookup"><span data-stu-id="77bfc-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="77bfc-114">Ostatnie polecenie wyłącza ochronę kopii zapasowych elementu w $PI \[ 0 \] , ale zachowuje dane.</span><span class="sxs-lookup"><span data-stu-id="77bfc-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="77bfc-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77bfc-115">PARAMETERS</span></span>

### <span data-ttu-id="77bfc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77bfc-116">-DefaultProfile</span></span>
<span data-ttu-id="77bfc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77bfc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77bfc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="77bfc-118">-Force</span></span>
<span data-ttu-id="77bfc-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="77bfc-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77bfc-120">-Item</span><span class="sxs-lookup"><span data-stu-id="77bfc-120">-Item</span></span>
<span data-ttu-id="77bfc-121">Określa element kopii zapasowej, dla którego to polecenie cmdlet wyłącza ochronę.</span><span class="sxs-lookup"><span data-stu-id="77bfc-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="77bfc-122">Aby uzyskać **AzureRmRecoveryServicesBackupItem** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="77bfc-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="77bfc-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="77bfc-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="77bfc-124">Wskazuje, że to polecenie cmdlet usuwa istniejące punkty odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="77bfc-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="77bfc-125">Aby później usunąć zapisane punkty odzyskiwania, uruchom ponownie to polecenie cmdlet i określ ten parametr.</span><span class="sxs-lookup"><span data-stu-id="77bfc-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="77bfc-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="77bfc-126">-VaultId</span></span>
<span data-ttu-id="77bfc-127">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="77bfc-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="77bfc-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77bfc-128">-Confirm</span></span>
<span data-ttu-id="77bfc-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77bfc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77bfc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77bfc-130">-WhatIf</span></span>
<span data-ttu-id="77bfc-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77bfc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77bfc-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="77bfc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77bfc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77bfc-133">CommonParameters</span></span>
<span data-ttu-id="77bfc-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77bfc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77bfc-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77bfc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77bfc-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77bfc-136">INPUTS</span></span>

### <span data-ttu-id="77bfc-137">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="77bfc-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="77bfc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="77bfc-138">System.String</span></span>

## <span data-ttu-id="77bfc-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77bfc-139">OUTPUTS</span></span>

### <span data-ttu-id="77bfc-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="77bfc-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="77bfc-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77bfc-141">NOTES</span></span>

## <span data-ttu-id="77bfc-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77bfc-142">RELATED LINKS</span></span>

[<span data-ttu-id="77bfc-143">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="77bfc-143">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="77bfc-144">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="77bfc-144">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="77bfc-145">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="77bfc-145">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


