---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/remove-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d687834c41f354897f64ca3300c7c8eaa47940b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526682"
---
# <span data-ttu-id="20277-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="20277-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="20277-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20277-102">SYNOPSIS</span></span>
<span data-ttu-id="20277-103">Usuwa zasady ochrony kopii zapasowej z magazynu.</span><span class="sxs-lookup"><span data-stu-id="20277-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20277-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20277-104">SYNTAX</span></span>

### <span data-ttu-id="20277-105">PolicyName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="20277-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20277-106">Policyobject</span><span class="sxs-lookup"><span data-stu-id="20277-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20277-107">Opis</span><span class="sxs-lookup"><span data-stu-id="20277-107">DESCRIPTION</span></span>
<span data-ttu-id="20277-108">Polecenie cmdlet **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** usuwa zasady tworzenia kopii zapasowych dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="20277-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>

<span data-ttu-id="20277-109">Przed usunięciem zasad ochrony kopii zapasowej zasady nie mogą zawierać żadnych elementów kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="20277-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="20277-110">Przed usunięciem zasad upewnij się, że każdy skojarzony element jest skojarzony z innymi zasadami.</span><span class="sxs-lookup"><span data-stu-id="20277-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="20277-111">Aby skojarzyć inne zasady z elementem kopii zapasowej, użyj polecenia cmdlet Enable-AzureRmRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="20277-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>

<span data-ttu-id="20277-112">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="20277-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="20277-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20277-113">EXAMPLES</span></span>

### <span data-ttu-id="20277-114">Przykład 1: usuwanie zasad</span><span class="sxs-lookup"><span data-stu-id="20277-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="20277-115">Pierwsze polecenie uzyskuje zasady ochrony kopii zapasowej o nazwie NewPolicy, a następnie zapisuje je w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="20277-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="20277-116">Drugie polecenie usuwa obiekt zasady w $Pol.</span><span class="sxs-lookup"><span data-stu-id="20277-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="20277-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20277-117">PARAMETERS</span></span>

### <span data-ttu-id="20277-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20277-118">-DefaultProfile</span></span>
<span data-ttu-id="20277-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20277-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20277-120">-Force</span><span class="sxs-lookup"><span data-stu-id="20277-120">-Force</span></span>
<span data-ttu-id="20277-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="20277-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20277-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="20277-122">-Name</span></span>
<span data-ttu-id="20277-123">Określa nazwę zasad ochrony kopii zapasowych, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="20277-123">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: String
Parameter Sets: PolicyName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20277-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20277-124">-PassThru</span></span>
<span data-ttu-id="20277-125">Zwraca zasady, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="20277-125">Return the policy to be deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20277-126">-Policy</span><span class="sxs-lookup"><span data-stu-id="20277-126">-Policy</span></span>
<span data-ttu-id="20277-127">Określa zasady ochrony kopii zapasowej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="20277-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="20277-128">Aby uzyskać obiekt **BackupPolicy** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="20277-128">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: PolicyObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20277-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20277-129">-Confirm</span></span>
<span data-ttu-id="20277-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20277-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20277-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20277-131">-WhatIf</span></span>
<span data-ttu-id="20277-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20277-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20277-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="20277-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20277-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20277-134">CommonParameters</span></span>
<span data-ttu-id="20277-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20277-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20277-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20277-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20277-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20277-137">INPUTS</span></span>

### <span data-ttu-id="20277-138">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="20277-138">PolicyBase</span></span>
<span data-ttu-id="20277-139">Parametr "Policy" przyjmuje wartość typu "PolicyBase" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="20277-139">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="20277-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20277-140">OUTPUTS</span></span>

## <span data-ttu-id="20277-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20277-141">NOTES</span></span>

## <span data-ttu-id="20277-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20277-142">RELATED LINKS</span></span>

[<span data-ttu-id="20277-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="20277-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="20277-144">Nowe — AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="20277-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="20277-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="20277-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


