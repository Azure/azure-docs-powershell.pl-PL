---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: b900e9b137c8268969ef1eb715f0b79356abc720
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886633"
---
# <span data-ttu-id="2305a-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2305a-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="2305a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2305a-102">SYNOPSIS</span></span>
<span data-ttu-id="2305a-103">Usuwa zasady ochrony kopii zapasowej z magazynu.</span><span class="sxs-lookup"><span data-stu-id="2305a-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="2305a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2305a-104">SYNTAX</span></span>

### <span data-ttu-id="2305a-105">PolicyName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2305a-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2305a-106">Policyobject</span><span class="sxs-lookup"><span data-stu-id="2305a-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2305a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2305a-107">DESCRIPTION</span></span>
<span data-ttu-id="2305a-108">Polecenie cmdlet **Remove-AzRecoveryServicesBackupProtectionPolicy** usuwa zasady tworzenia kopii zapasowych dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="2305a-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="2305a-109">Przed usunięciem zasad ochrony kopii zapasowej zasady nie mogą zawierać żadnych elementów kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2305a-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="2305a-110">Przed usunięciem zasad upewnij się, że każdy skojarzony element jest skojarzony z innymi zasadami.</span><span class="sxs-lookup"><span data-stu-id="2305a-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="2305a-111">Aby skojarzyć inne zasady z elementem kopii zapasowej, użyj polecenia cmdlet Enable-AzRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="2305a-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="2305a-112">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="2305a-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2305a-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2305a-113">EXAMPLES</span></span>

### <span data-ttu-id="2305a-114">Przykład 1: usuwanie zasad</span><span class="sxs-lookup"><span data-stu-id="2305a-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="2305a-115">Pierwsze polecenie uzyskuje zasady ochrony kopii zapasowej o nazwie NewPolicy, a następnie zapisuje je w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="2305a-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="2305a-116">Drugie polecenie usuwa obiekt zasady w $Pol.</span><span class="sxs-lookup"><span data-stu-id="2305a-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="2305a-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2305a-117">PARAMETERS</span></span>

### <span data-ttu-id="2305a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2305a-118">-DefaultProfile</span></span>
<span data-ttu-id="2305a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2305a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2305a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2305a-120">-Force</span></span>
<span data-ttu-id="2305a-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2305a-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2305a-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2305a-122">-Name</span></span>
<span data-ttu-id="2305a-123">Określa nazwę zasad ochrony kopii zapasowych, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="2305a-123">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="2305a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2305a-124">-PassThru</span></span>
<span data-ttu-id="2305a-125">Zwraca zasady, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="2305a-125">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="2305a-126">-Policy</span><span class="sxs-lookup"><span data-stu-id="2305a-126">-Policy</span></span>
<span data-ttu-id="2305a-127">Określa zasady ochrony kopii zapasowej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="2305a-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="2305a-128">Aby uzyskać obiekt **BackupPolicy** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="2305a-128">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="2305a-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2305a-129">-VaultId</span></span>
<span data-ttu-id="2305a-130">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2305a-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2305a-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2305a-131">-Confirm</span></span>
<span data-ttu-id="2305a-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2305a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2305a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2305a-133">-WhatIf</span></span>
<span data-ttu-id="2305a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2305a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2305a-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2305a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2305a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2305a-136">CommonParameters</span></span>
<span data-ttu-id="2305a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2305a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2305a-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2305a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2305a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2305a-139">INPUTS</span></span>

### <span data-ttu-id="2305a-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="2305a-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="2305a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2305a-141">System.String</span></span>

## <span data-ttu-id="2305a-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2305a-142">OUTPUTS</span></span>

### <span data-ttu-id="2305a-143">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="2305a-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="2305a-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2305a-144">NOTES</span></span>

## <span data-ttu-id="2305a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2305a-145">RELATED LINKS</span></span>

[<span data-ttu-id="2305a-146">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2305a-146">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="2305a-147">Nowe — AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2305a-147">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="2305a-148">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2305a-148">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


