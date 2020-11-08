---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063829"
---
# <span data-ttu-id="bb7ba-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="bb7ba-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="bb7ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb7ba-102">SYNOPSIS</span></span>
<span data-ttu-id="bb7ba-103">Jeśli element kopii zapasowej zostanie usunięty i zaprezentować go w stanie nieusuniętym, to polecenie przełączy element z powrotem do stanu, w którym dane są zawsze zachowywane.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="bb7ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb7ba-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb7ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb7ba-105">DESCRIPTION</span></span>
<span data-ttu-id="bb7ba-106">Polecenie cmdlet Undo-AzRecoveryServicesBackupItemDeletion powoduje przywrócenie elementu usuniętego z usunięcia do stanu, w którym ochrona jest zatrzymana, ale dane są zawsze zachowywane.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="bb7ba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb7ba-107">EXAMPLES</span></span>

### <span data-ttu-id="bb7ba-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb7ba-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="bb7ba-109">Pierwsze polecenie uzyskuje tablicę kontenerów kopii zapasowych, a następnie zapisuje je w tablicy $Cont.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="bb7ba-110">Drugie polecenie pobiera element kopii zapasowej odpowiadający pierwszemu kontenerowi, a następnie zapisuje go w zmiennej $PI.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="bb7ba-111">Trzecia komenda wyłącza ochronę kopii zapasowych elementu w $PI \[ 0 \] i umieszcza element w stanie softdeleted.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="bb7ba-112">W czwartym poleceniu jest pobierany element, który jest w stanie softdeleted.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="bb7ba-113">Ostatnie polecenie powoduje, że maszyna wirtualna softdeleted jest zatrzymywana w stanie, w którym ochrona jest zatrzymana, ale dane są zawsze zachowywane.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="bb7ba-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bb7ba-114">Example 2</span></span>

<span data-ttu-id="bb7ba-115">Umożliwia odrejestrowanie nietrwałego elementu.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="bb7ba-116">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="bb7ba-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="bb7ba-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb7ba-117">PARAMETERS</span></span>

### <span data-ttu-id="bb7ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb7ba-118">-DefaultProfile</span></span>
<span data-ttu-id="bb7ba-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb7ba-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bb7ba-120">-Force</span></span>
<span data-ttu-id="bb7ba-121">Force wyłącza ochronę kopii zapasowej (zapobiega wyświetlaniu okna dialogowego potwierdzenia).</span><span class="sxs-lookup"><span data-stu-id="bb7ba-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="bb7ba-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="bb7ba-123">-Item</span><span class="sxs-lookup"><span data-stu-id="bb7ba-123">-Item</span></span>
<span data-ttu-id="bb7ba-124">Określa element kopii zapasowej, dla którego to polecenie cmdlet powoduje przywrócenie usunięcia.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="bb7ba-125">Aby uzyskać AzureRmRecoveryServicesBackupItem, użyj polecenia cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="bb7ba-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bb7ba-126">-VaultId</span></span>
<span data-ttu-id="bb7ba-127">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="bb7ba-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb7ba-128">-Confirm</span></span>
<span data-ttu-id="bb7ba-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb7ba-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb7ba-130">-WhatIf</span></span>
<span data-ttu-id="bb7ba-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb7ba-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb7ba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb7ba-133">CommonParameters</span></span>
<span data-ttu-id="bb7ba-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb7ba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb7ba-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb7ba-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb7ba-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb7ba-136">INPUTS</span></span>

### <span data-ttu-id="bb7ba-137">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="bb7ba-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="bb7ba-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bb7ba-138">System.String</span></span>

## <span data-ttu-id="bb7ba-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb7ba-139">OUTPUTS</span></span>

### <span data-ttu-id="bb7ba-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="bb7ba-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="bb7ba-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb7ba-141">NOTES</span></span>

## <span data-ttu-id="bb7ba-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb7ba-142">RELATED LINKS</span></span>

[<span data-ttu-id="bb7ba-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bb7ba-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="bb7ba-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="bb7ba-144">Get-AzRecoveryServicesBackupItem</span></span>]()

