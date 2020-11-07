---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 07406378df0439171c5be2e7558e8ac33cb32687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716930"
---
# <span data-ttu-id="869de-101">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="869de-101">Disable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="869de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="869de-102">SYNOPSIS</span></span>
<span data-ttu-id="869de-103">Wyłącza ochronę elementu chronionego kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="869de-103">Disables protection for a Backup-protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="869de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="869de-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="869de-105">Opis</span><span class="sxs-lookup"><span data-stu-id="869de-105">DESCRIPTION</span></span>
<span data-ttu-id="869de-106">Polecenie cmdlet **disable-AzureRmRecoveryServicesBackupProtection** wyłącza ochronę elementu chronionego usługą Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="869de-106">The **Disable-AzureRmRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="869de-107">To polecenie cmdlet zatrzymuje regularne Planowanie kopii zapasowej elementu.</span><span class="sxs-lookup"><span data-stu-id="869de-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="869de-108">To polecenie cmdlet umożliwia również usunięcie istniejących punktów odzyskiwania dla elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="869de-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="869de-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="869de-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="869de-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="869de-110">EXAMPLES</span></span>

### <span data-ttu-id="869de-111">Przykład 1: Wyłączanie ochrony przed kopiami zapasowymi</span><span class="sxs-lookup"><span data-stu-id="869de-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzureRmRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzureRmRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="869de-112">Pierwsze polecenie uzyskuje tablicę kontenerów kopii zapasowych, a następnie zapisuje je w tablicy $Cont.</span><span class="sxs-lookup"><span data-stu-id="869de-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="869de-113">Drugie polecenie pobiera element kopii zapasowej odpowiadający pierwszemu kontenerowi, a następnie zapisuje go w zmiennej $PI.</span><span class="sxs-lookup"><span data-stu-id="869de-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="869de-114">Ostatnie polecenie wyłącza ochronę kopii zapasowych elementu w $PI \[ 0 \] , ale zachowuje dane.</span><span class="sxs-lookup"><span data-stu-id="869de-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="869de-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="869de-115">PARAMETERS</span></span>

### <span data-ttu-id="869de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="869de-116">-DefaultProfile</span></span>
<span data-ttu-id="869de-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="869de-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="869de-118">-Force</span><span class="sxs-lookup"><span data-stu-id="869de-118">-Force</span></span>
<span data-ttu-id="869de-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="869de-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="869de-120">-Item</span><span class="sxs-lookup"><span data-stu-id="869de-120">-Item</span></span>
<span data-ttu-id="869de-121">Określa element kopii zapasowej, dla którego to polecenie cmdlet wyłącza ochronę.</span><span class="sxs-lookup"><span data-stu-id="869de-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="869de-122">Aby uzyskać **AzureRmRecoveryServicesBackupItem** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="869de-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="869de-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="869de-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="869de-124">Wskazuje, że to polecenie cmdlet usuwa istniejące punkty odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="869de-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="869de-125">Aby później usunąć zapisane punkty odzyskiwania, uruchom ponownie to polecenie cmdlet i określ ten parametr.</span><span class="sxs-lookup"><span data-stu-id="869de-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="869de-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="869de-126">-VaultId</span></span>
<span data-ttu-id="869de-127">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="869de-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="869de-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="869de-128">-Confirm</span></span>
<span data-ttu-id="869de-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="869de-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="869de-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="869de-130">-WhatIf</span></span>
<span data-ttu-id="869de-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="869de-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="869de-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="869de-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="869de-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="869de-133">CommonParameters</span></span>
<span data-ttu-id="869de-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="869de-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="869de-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="869de-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="869de-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="869de-136">INPUTS</span></span>

### <span data-ttu-id="869de-137">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="869de-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="869de-138">Parametry: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="869de-138">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="869de-139">System. String</span><span class="sxs-lookup"><span data-stu-id="869de-139">System.String</span></span>
<span data-ttu-id="869de-140">Parametry: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="869de-140">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="869de-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="869de-141">OUTPUTS</span></span>

### <span data-ttu-id="869de-142">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="869de-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="869de-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="869de-143">NOTES</span></span>

## <span data-ttu-id="869de-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="869de-144">RELATED LINKS</span></span>

[<span data-ttu-id="869de-145">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="869de-145">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="869de-146">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="869de-146">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="869de-147">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="869de-147">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


