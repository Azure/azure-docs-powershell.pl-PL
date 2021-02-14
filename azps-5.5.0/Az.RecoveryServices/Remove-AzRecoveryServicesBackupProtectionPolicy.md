---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c3f4bb9b7c3d2b862ff78fdb35517f5837ffedf0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183890"
---
# <span data-ttu-id="fd4a0-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fd4a0-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="fd4a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd4a0-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4a0-103">Usuwa zasady ochrony kopii zapasowej z magazynu.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="fd4a0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fd4a0-104">SYNTAX</span></span>

### <span data-ttu-id="fd4a0-105">PolicyName (Default)</span><span class="sxs-lookup"><span data-stu-id="fd4a0-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd4a0-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="fd4a0-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd4a0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fd4a0-107">DESCRIPTION</span></span>
<span data-ttu-id="fd4a0-108">Polecenie **cmdlet Remove-AzRecoveryServicesBackupProtectionPolicy** usuwa zasady kopii zapasowej dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="fd4a0-109">Zanim będzie można usunąć zasady ochrony kopii zapasowej, nie mogą zawierać skojarzonych elementów kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="fd4a0-110">Przed usunięciem zasad upewnij się, że każdy skojarzony element jest skojarzony z innymi zasadami.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="fd4a0-111">Aby skojarzyć inne zasady z elementem kopii zapasowej, użyj Enable-AzRecoveryServicesBackupProtection cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="fd4a0-112">Ustaw kontekst magazynu za pomocą Set-AzRecoveryServicesVaultContext cmdlet przed użyciem bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="fd4a0-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fd4a0-113">EXAMPLES</span></span>

### <span data-ttu-id="fd4a0-114">Przykład 1. Usuwanie zasad</span><span class="sxs-lookup"><span data-stu-id="fd4a0-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="fd4a0-115">Pierwsze polecenie pobiera zasady ochrony kopii zapasowej o nazwie NewPolicy, a następnie zapisuje je w $Pol danych.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="fd4a0-116">Drugie polecenie usuwa obiekt zasad w $Pol.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="fd4a0-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fd4a0-117">Example 2</span></span>

<span data-ttu-id="fd4a0-118">Usuwa zasady ochrony kopii zapasowej z magazynu.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="fd4a0-119">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="fd4a0-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="fd4a0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd4a0-120">PARAMETERS</span></span>

### <span data-ttu-id="fd4a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd4a0-121">-DefaultProfile</span></span>
<span data-ttu-id="fd4a0-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd4a0-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="fd4a0-123">-Force</span></span>
<span data-ttu-id="fd4a0-124">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd4a0-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fd4a0-125">-Name</span></span>
<span data-ttu-id="fd4a0-126">Określa nazwę zasad ochrony kopii zapasowej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-126">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd4a0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd4a0-127">-PassThru</span></span>
<span data-ttu-id="fd4a0-128">Zwróć zasady do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="fd4a0-129">— Zasady</span><span class="sxs-lookup"><span data-stu-id="fd4a0-129">-Policy</span></span>
<span data-ttu-id="fd4a0-130">Określa zasady ochrony kopii zapasowej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="fd4a0-131">Aby uzyskać obiekt **BackupPolicy,** użyj Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd4a0-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="fd4a0-132">-VaultId</span></span>
<span data-ttu-id="fd4a0-133">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fd4a0-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd4a0-134">-Confirm</span></span>
<span data-ttu-id="fd4a0-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd4a0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd4a0-136">-WhatIf</span></span>
<span data-ttu-id="fd4a0-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="fd4a0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4a0-138">CommonParameters</span></span>
<span data-ttu-id="fd4a0-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd4a0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4a0-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd4a0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4a0-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd4a0-141">INPUTS</span></span>

### <span data-ttu-id="fd4a0-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="fd4a0-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="fd4a0-143">System.String</span><span class="sxs-lookup"><span data-stu-id="fd4a0-143">System.String</span></span>

## <span data-ttu-id="fd4a0-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd4a0-144">OUTPUTS</span></span>

### <span data-ttu-id="fd4a0-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="fd4a0-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="fd4a0-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fd4a0-146">NOTES</span></span>

## <span data-ttu-id="fd4a0-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd4a0-147">RELATED LINKS</span></span>

[<span data-ttu-id="fd4a0-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fd4a0-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="fd4a0-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fd4a0-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="fd4a0-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fd4a0-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


