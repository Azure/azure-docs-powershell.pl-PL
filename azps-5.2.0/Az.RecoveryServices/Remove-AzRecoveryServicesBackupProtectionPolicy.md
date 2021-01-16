---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c3f4bb9b7c3d2b862ff78fdb35517f5837ffedf0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329112"
---
# <span data-ttu-id="40dc9-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="40dc9-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="40dc9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="40dc9-103">Usuwa zasady ochrony kopii zapasowej z magazynu.</span><span class="sxs-lookup"><span data-stu-id="40dc9-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="40dc9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40dc9-104">SYNTAX</span></span>

### <span data-ttu-id="40dc9-105">PolicyName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="40dc9-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40dc9-106">Policyobject</span><span class="sxs-lookup"><span data-stu-id="40dc9-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40dc9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="40dc9-107">DESCRIPTION</span></span>
<span data-ttu-id="40dc9-108">Polecenie cmdlet **Remove-AzRecoveryServicesBackupProtectionPolicy** usuwa zasady tworzenia kopii zapasowych dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="40dc9-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="40dc9-109">Przed usunięciem zasad ochrony kopii zapasowej zasady nie mogą zawierać żadnych elementów kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="40dc9-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="40dc9-110">Przed usunięciem zasad upewnij się, że każdy skojarzony element jest skojarzony z innymi zasadami.</span><span class="sxs-lookup"><span data-stu-id="40dc9-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="40dc9-111">Aby skojarzyć inne zasady z elementem kopii zapasowej, użyj polecenia cmdlet Enable-AzRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="40dc9-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="40dc9-112">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="40dc9-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="40dc9-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40dc9-113">EXAMPLES</span></span>

### <span data-ttu-id="40dc9-114">Przykład 1: usuwanie zasad</span><span class="sxs-lookup"><span data-stu-id="40dc9-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="40dc9-115">Pierwsze polecenie uzyskuje zasady ochrony kopii zapasowej o nazwie NewPolicy, a następnie zapisuje je w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="40dc9-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="40dc9-116">Drugie polecenie usuwa obiekt zasady w $Pol.</span><span class="sxs-lookup"><span data-stu-id="40dc9-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="40dc9-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="40dc9-117">Example 2</span></span>

<span data-ttu-id="40dc9-118">Usuwa zasady ochrony kopii zapasowej z magazynu.</span><span class="sxs-lookup"><span data-stu-id="40dc9-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="40dc9-119">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="40dc9-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="40dc9-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40dc9-120">PARAMETERS</span></span>

### <span data-ttu-id="40dc9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40dc9-121">-DefaultProfile</span></span>
<span data-ttu-id="40dc9-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40dc9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40dc9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="40dc9-123">-Force</span></span>
<span data-ttu-id="40dc9-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="40dc9-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="40dc9-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40dc9-125">-Name</span></span>
<span data-ttu-id="40dc9-126">Określa nazwę zasad ochrony kopii zapasowych, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="40dc9-126">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="40dc9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40dc9-127">-PassThru</span></span>
<span data-ttu-id="40dc9-128">Zwraca zasady, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="40dc9-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="40dc9-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="40dc9-129">-Policy</span></span>
<span data-ttu-id="40dc9-130">Określa zasady ochrony kopii zapasowej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="40dc9-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="40dc9-131">Aby uzyskać obiekt **BackupPolicy** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="40dc9-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="40dc9-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="40dc9-132">-VaultId</span></span>
<span data-ttu-id="40dc9-133">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="40dc9-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="40dc9-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40dc9-134">-Confirm</span></span>
<span data-ttu-id="40dc9-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40dc9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40dc9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40dc9-136">-WhatIf</span></span>
<span data-ttu-id="40dc9-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40dc9-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="40dc9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40dc9-138">CommonParameters</span></span>
<span data-ttu-id="40dc9-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40dc9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40dc9-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40dc9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40dc9-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40dc9-141">INPUTS</span></span>

### <span data-ttu-id="40dc9-142">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="40dc9-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="40dc9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="40dc9-143">System.String</span></span>

## <span data-ttu-id="40dc9-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40dc9-144">OUTPUTS</span></span>

### <span data-ttu-id="40dc9-145">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="40dc9-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="40dc9-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40dc9-146">NOTES</span></span>

## <span data-ttu-id="40dc9-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40dc9-147">RELATED LINKS</span></span>

[<span data-ttu-id="40dc9-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="40dc9-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="40dc9-149">Nowe — AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="40dc9-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="40dc9-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="40dc9-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


