---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 36b93041a2dfa4ba64779b2a92aeee50da53ce44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886577"
---
# <span data-ttu-id="ed9a5-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="ed9a5-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="ed9a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9a5-103">Umożliwia odrejestrowanie elementu, który został usunięty.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-103">Rehydrates a soft-deleted Item</span></span>

## <span data-ttu-id="ed9a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed9a5-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed9a5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ed9a5-105">DESCRIPTION</span></span>
<span data-ttu-id="ed9a5-106">Polecenie cmdlet Undo-AzRecoveryServicesBackupItemDeletion umożliwia przerejestrowanie elementu, który został usunięty.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet rehydrates a soft-deleted item.</span></span>
<span data-ttu-id="ed9a5-107">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ed9a5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed9a5-108">EXAMPLES</span></span>

### <span data-ttu-id="ed9a5-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed9a5-109">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="ed9a5-110">Pierwsze polecenie uzyskuje tablicę kontenerów kopii zapasowych, a następnie zapisuje je w tablicy $Cont.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-110">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="ed9a5-111">Drugie polecenie pobiera element kopii zapasowej odpowiadający pierwszemu kontenerowi, a następnie zapisuje go w zmiennej $PI.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-111">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="ed9a5-112">Trzecia komenda wyłącza ochronę kopii zapasowych elementu w $PI \[ 0 \] i umieszcza element w stanie softdeleted.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-112">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="ed9a5-113">Czwarte polecenie Nowy element, który jest w stanie softdeleted.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-113">The fourth command the new item which is in a softdeleted state.</span></span>
<span data-ttu-id="ed9a5-114">Ostatnie polecenie umożliwia rehydratacji maszyny wirtualnej softdeleted.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-114">The last command rehydrates the softdeleted VM.</span></span>


## <span data-ttu-id="ed9a5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed9a5-115">PARAMETERS</span></span>

### <span data-ttu-id="ed9a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9a5-116">-DefaultProfile</span></span>
<span data-ttu-id="ed9a5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed9a5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ed9a5-118">-Force</span></span>
<span data-ttu-id="ed9a5-119">Force wyłącza ochronę kopii zapasowej (zapobiega wyświetlaniu okna dialogowego potwierdzenia).</span><span class="sxs-lookup"><span data-stu-id="ed9a5-119">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="ed9a5-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="ed9a5-121">-Item</span><span class="sxs-lookup"><span data-stu-id="ed9a5-121">-Item</span></span>
<span data-ttu-id="ed9a5-122">Określa element kopii zapasowej, dla którego to polecenie cmdlet wyłącza ochronę.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-122">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="ed9a5-123">Aby uzyskać AzureRmRecoveryServicesBackupItem, użyj polecenia cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-123">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="ed9a5-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ed9a5-124">-VaultId</span></span>
<span data-ttu-id="ed9a5-125">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ed9a5-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ed9a5-126">-Confirm</span></span>
<span data-ttu-id="ed9a5-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed9a5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed9a5-128">-WhatIf</span></span>
<span data-ttu-id="ed9a5-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed9a5-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed9a5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9a5-131">CommonParameters</span></span>
<span data-ttu-id="ed9a5-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed9a5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9a5-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed9a5-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9a5-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed9a5-134">INPUTS</span></span>

### <span data-ttu-id="ed9a5-135">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="ed9a5-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="ed9a5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ed9a5-136">System.String</span></span>

## <span data-ttu-id="ed9a5-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed9a5-137">OUTPUTS</span></span>

### <span data-ttu-id="ed9a5-138">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="ed9a5-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ed9a5-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed9a5-139">NOTES</span></span>

## <span data-ttu-id="ed9a5-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed9a5-140">RELATED LINKS</span></span>

[<span data-ttu-id="ed9a5-141">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ed9a5-141">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="ed9a5-142">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ed9a5-142">Get-AzRecoveryServicesBackupItem</span></span>]()

