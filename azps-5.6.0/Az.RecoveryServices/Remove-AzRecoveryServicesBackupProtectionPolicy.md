---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 4723fd3087b2f547659e72c1af6b0f5cb7764cf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953121"
---
# <span data-ttu-id="5faec-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5faec-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="5faec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5faec-102">SYNOPSIS</span></span>
<span data-ttu-id="5faec-103">Usuwa zasady ochrony kopii zapasowej z magazynu.</span><span class="sxs-lookup"><span data-stu-id="5faec-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="5faec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5faec-104">SYNTAX</span></span>

### <span data-ttu-id="5faec-105">PolicyName (Default)</span><span class="sxs-lookup"><span data-stu-id="5faec-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5faec-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="5faec-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5faec-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5faec-107">DESCRIPTION</span></span>
<span data-ttu-id="5faec-108">Polecenie **cmdlet Remove-AzRecoveryServicesBackupProtectionPolicy** usuwa zasady kopii zapasowej dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="5faec-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="5faec-109">Zanim będzie można usunąć zasady ochrony kopii zapasowej, nie mogą zawierać skojarzonych elementów kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="5faec-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="5faec-110">Przed usunięciem zasad upewnij się, że każdy skojarzony element jest skojarzony z innymi zasadami.</span><span class="sxs-lookup"><span data-stu-id="5faec-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="5faec-111">Aby skojarzyć inne zasady z elementem kopii zapasowej, użyj Enable-AzRecoveryServicesBackupProtection cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5faec-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="5faec-112">Ustaw kontekst magazynu za pomocą Set-AzRecoveryServicesVaultContext cmdlet przed użyciem bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5faec-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5faec-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5faec-113">EXAMPLES</span></span>

### <span data-ttu-id="5faec-114">Przykład 1. Usuwanie zasad</span><span class="sxs-lookup"><span data-stu-id="5faec-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="5faec-115">Pierwsze polecenie pobiera zasady ochrony kopii zapasowej o nazwie NewPolicy, a następnie zapisuje je w $Pol danych.</span><span class="sxs-lookup"><span data-stu-id="5faec-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="5faec-116">Drugie polecenie usuwa obiekt zasad w $Pol.</span><span class="sxs-lookup"><span data-stu-id="5faec-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="5faec-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5faec-117">Example 2</span></span>

<span data-ttu-id="5faec-118">Usuwa zasady ochrony kopii zapasowej z magazynu.</span><span class="sxs-lookup"><span data-stu-id="5faec-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="5faec-119">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="5faec-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="5faec-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5faec-120">PARAMETERS</span></span>

### <span data-ttu-id="5faec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5faec-121">-DefaultProfile</span></span>
<span data-ttu-id="5faec-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5faec-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5faec-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5faec-123">-Force</span></span>
<span data-ttu-id="5faec-124">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5faec-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5faec-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5faec-125">-Name</span></span>
<span data-ttu-id="5faec-126">Określa nazwę zasad ochrony kopii zapasowej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5faec-126">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="5faec-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5faec-127">-PassThru</span></span>
<span data-ttu-id="5faec-128">Zwróć zasady do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5faec-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="5faec-129">— Zasady</span><span class="sxs-lookup"><span data-stu-id="5faec-129">-Policy</span></span>
<span data-ttu-id="5faec-130">Określa zasady ochrony kopii zapasowej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5faec-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="5faec-131">Aby uzyskać obiekt **BackupPolicy,** użyj Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5faec-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="5faec-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5faec-132">-VaultId</span></span>
<span data-ttu-id="5faec-133">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5faec-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5faec-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5faec-134">-Confirm</span></span>
<span data-ttu-id="5faec-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5faec-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5faec-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5faec-136">-WhatIf</span></span>
<span data-ttu-id="5faec-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5faec-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="5faec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5faec-138">CommonParameters</span></span>
<span data-ttu-id="5faec-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5faec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5faec-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5faec-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5faec-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5faec-141">INPUTS</span></span>

### <span data-ttu-id="5faec-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="5faec-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="5faec-143">System.String</span><span class="sxs-lookup"><span data-stu-id="5faec-143">System.String</span></span>

## <span data-ttu-id="5faec-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5faec-144">OUTPUTS</span></span>

### <span data-ttu-id="5faec-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="5faec-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="5faec-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5faec-146">NOTES</span></span>

## <span data-ttu-id="5faec-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5faec-147">RELATED LINKS</span></span>

[<span data-ttu-id="5faec-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5faec-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="5faec-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5faec-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="5faec-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5faec-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


