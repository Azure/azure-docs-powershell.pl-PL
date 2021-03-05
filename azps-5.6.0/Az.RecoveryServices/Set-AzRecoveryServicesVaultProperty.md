---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a88b137b5735984ce6b5f19389d9035b85b1dfe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997382"
---
# <span data-ttu-id="7c3f4-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="7c3f4-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="7c3f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="7c3f4-103">Aktualizuje właściwości magazynu.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="7c3f4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7c3f4-104">SYNTAX</span></span>

### <span data-ttu-id="7c3f4-105">AzureRSVaultSoftDelteParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7c3f4-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c3f4-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c3f4-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c3f4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7c3f4-107">DESCRIPTION</span></span>
<span data-ttu-id="7c3f4-108">Polecenie **cmdlet Set-AzRecoveryServicesVaultProperty** aktualizuje właściwości magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="7c3f4-109">To polecenie cmdlet może służyć do włączania/wyłączania funkcji "miękkiego usuwania" lub ustawienia szyfrowania CMK dla magazynu z dwoma różnymi zestawami parametrów.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="7c3f4-110">**Właściwość SoftDeleteFeatureState** magazynu można wyłączyć tylko wtedy, gdy w magazynie nie ma zarejestrowanych kontenerów.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="7c3f4-111">InfrastructurEncryption można ustawić tylko wtedy, gdy użytkownik po raz pierwszy aktualizuje magazyn CMK.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="7c3f4-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7c3f4-112">EXAMPLES</span></span>

### <span data-ttu-id="7c3f4-113">Przykład 1. Aktualizowanie stanu SoftDeleteFeatureState magazynu</span><span class="sxs-lookup"><span data-stu-id="7c3f4-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="7c3f4-114">Pierwsze polecenie pobiera obiekt magazynu, a następnie przechowuje go w $vault zmienną.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="7c3f4-115">Drugie polecenie aktualizuje właściwość SoftDeleteFeatureState magazynu do stanu "Włączony".</span><span class="sxs-lookup"><span data-stu-id="7c3f4-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="7c3f4-116">Przykład 2. Aktualizowanie szyfrowania CMK magazynu</span><span class="sxs-lookup"><span data-stu-id="7c3f4-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="7c3f4-117">Pierwsze polecenie cmdlet pobiera RSVault w celu zaktualizowania właściwości szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="7c3f4-118">Drugie polecenie cmdlet pobiera magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="7c3f4-119">Trzecie polecenie cmdlet pobierze klucz z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="7c3f4-120">Czwarte polecenie cmdlet aktualizuje klucz szyfrowania zarządzany przez klienta w ramach usługi RSVault.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="7c3f4-121">Użyj paramu -InfrastructureEncryption, aby włączyć szyfrowanie infrastruktury po raz pierwszy.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="7c3f4-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c3f4-122">PARAMETERS</span></span>

### <span data-ttu-id="7c3f4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c3f4-123">-DefaultProfile</span></span>
<span data-ttu-id="7c3f4-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c3f4-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="7c3f4-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="7c3f4-126">SoftDeleteFeatureState magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c3f4-127">- EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="7c3f4-127">-EncryptionKeyId</span></span>
<span data-ttu-id="7c3f4-128">KeyId klucza szyfrowania używanego dla klucza CMK.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-128">KeyId of the encryption key to be used for CMK.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: KeyID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c3f4-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c3f4-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="7c3f4-130">Identyfikator subskrypcji magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-130">Subscription Id of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SubscriptionID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c3f4-131">- InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="7c3f4-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="7c3f4-132">Umożliwia szyfrowanie infrastruktury w tym magazynie.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="7c3f4-133">Podczas konfigurowania szyfrowania musi być włączone szyfrowanie infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c3f4-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7c3f4-134">-VaultId</span></span>
<span data-ttu-id="7c3f4-135">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7c3f4-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7c3f4-136">-Confirm</span></span>
<span data-ttu-id="7c3f4-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c3f4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c3f4-138">-WhatIf</span></span>
<span data-ttu-id="7c3f4-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-139">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="7c3f4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c3f4-140">CommonParameters</span></span>
<span data-ttu-id="7c3f4-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c3f4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c3f4-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c3f4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c3f4-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c3f4-143">INPUTS</span></span>

### <span data-ttu-id="7c3f4-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7c3f4-144">System.String</span></span>

### <span data-ttu-id="7c3f4-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="7c3f4-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="7c3f4-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c3f4-146">OUTPUTS</span></span>

### <span data-ttu-id="7c3f4-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="7c3f4-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="7c3f4-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7c3f4-148">NOTES</span></span>

## <span data-ttu-id="7c3f4-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c3f4-149">RELATED LINKS</span></span>

[<span data-ttu-id="7c3f4-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7c3f4-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="7c3f4-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="7c3f4-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
