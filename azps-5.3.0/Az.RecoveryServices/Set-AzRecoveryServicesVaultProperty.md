---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: e6bd0284d9ce5b5cb6973fce6aae5e16a4c06883
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500109"
---
# <span data-ttu-id="6f14b-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="6f14b-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="6f14b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f14b-102">SYNOPSIS</span></span>
<span data-ttu-id="6f14b-103">Aktualizuje właściwości magazynu.</span><span class="sxs-lookup"><span data-stu-id="6f14b-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="6f14b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f14b-104">SYNTAX</span></span>

### <span data-ttu-id="6f14b-105">AzureRSVaultSoftDelteParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6f14b-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f14b-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f14b-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f14b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6f14b-107">DESCRIPTION</span></span>
<span data-ttu-id="6f14b-108">Polecenie cmdlet **Set-AzRecoveryServicesVaultProperty** aktualizuje właściwości magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6f14b-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="6f14b-109">Za pomocą tego polecenia cmdlet można włączać/wyłączać funkcję usuwania nieprawidłowych lub ustawić szyfrowanie CMK dla magazynu zawierającego dwa różne zestawy parametrów.</span><span class="sxs-lookup"><span data-stu-id="6f14b-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="6f14b-110">Właściwość **SoftDeleteFeatureState** magazynu może być wyłączona tylko wtedy, gdy w magazynie nie ma zarejestrowanych kontenerów.</span><span class="sxs-lookup"><span data-stu-id="6f14b-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="6f14b-111">InfrastructurEncryption można ustawić tylko wtedy, gdy użytkownik po raz pierwszy zaktualizuje magazyn CMK.</span><span class="sxs-lookup"><span data-stu-id="6f14b-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="6f14b-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f14b-112">EXAMPLES</span></span>

### <span data-ttu-id="6f14b-113">Przykład 1: aktualizowanie SoftDeleteFeatureState magazynu</span><span class="sxs-lookup"><span data-stu-id="6f14b-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="6f14b-114">Pierwsze polecenie pobiera obiekt magazynu, a następnie zapisuje go w zmiennej $vault.</span><span class="sxs-lookup"><span data-stu-id="6f14b-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="6f14b-115">Drugie polecenie aktualizuje stan "włączony" dla właściwości SoftDeleteFeatureState magazynu.</span><span class="sxs-lookup"><span data-stu-id="6f14b-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="6f14b-116">Przykład 2: aktualizowanie CMK szyfrowania magazynu</span><span class="sxs-lookup"><span data-stu-id="6f14b-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="6f14b-117">Pierwsze polecenie cmdlet umożliwia zaktualizowanie właściwości szyfrowania RSVault.</span><span class="sxs-lookup"><span data-stu-id="6f14b-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="6f14b-118">Drugie polecenie cmdlet umożliwia pobieranie magazynu kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6f14b-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="6f14b-119">Trzecie polecenie cmdlet uzyskuje klucz z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="6f14b-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="6f14b-120">Czwarty przycisk polecenia cmdlet aktualizuje klucz szyfrowania klienta zarządzany w RSVault.</span><span class="sxs-lookup"><span data-stu-id="6f14b-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="6f14b-121">Użyj parametru-InfrastructureEncryption param, aby włączyć szyfrowanie infrastruktury po raz pierwszy.</span><span class="sxs-lookup"><span data-stu-id="6f14b-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="6f14b-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f14b-122">PARAMETERS</span></span>

### <span data-ttu-id="6f14b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f14b-123">-DefaultProfile</span></span>
<span data-ttu-id="6f14b-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f14b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f14b-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="6f14b-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="6f14b-126">SoftDeleteFeatureState usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="6f14b-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6f14b-127">-EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="6f14b-127">-EncryptionKeyId</span></span>
<span data-ttu-id="6f14b-128">KeyId klucza szyfrowania, który ma być stosowany do CMK.</span><span class="sxs-lookup"><span data-stu-id="6f14b-128">KeyId of the encryption key to be used for CMK.</span></span>

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

### <span data-ttu-id="6f14b-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f14b-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="6f14b-130">Identyfikator subskrypcji magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="6f14b-130">Subscription Id of the Key Vault.</span></span>

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

### <span data-ttu-id="6f14b-131">-InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="6f14b-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="6f14b-132">Umożliwia szyfrowanie infrastruktury w tym magazynie.</span><span class="sxs-lookup"><span data-stu-id="6f14b-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="6f14b-133">Podczas konfigurowania szyfrowania należy włączyć szyfrowanie infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="6f14b-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

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

### <span data-ttu-id="6f14b-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6f14b-134">-VaultId</span></span>
<span data-ttu-id="6f14b-135">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="6f14b-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6f14b-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6f14b-136">-Confirm</span></span>
<span data-ttu-id="6f14b-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f14b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f14b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f14b-138">-WhatIf</span></span>
<span data-ttu-id="6f14b-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f14b-139">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="6f14b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f14b-140">CommonParameters</span></span>
<span data-ttu-id="6f14b-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f14b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f14b-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f14b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f14b-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f14b-143">INPUTS</span></span>

### <span data-ttu-id="6f14b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6f14b-144">System.String</span></span>

### <span data-ttu-id="6f14b-145">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="6f14b-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="6f14b-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f14b-146">OUTPUTS</span></span>

### <span data-ttu-id="6f14b-147">Microsoft. Azure. Management. RecoveryServices. Backup. models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="6f14b-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="6f14b-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f14b-148">NOTES</span></span>

## <span data-ttu-id="6f14b-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f14b-149">RELATED LINKS</span></span>

[<span data-ttu-id="6f14b-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6f14b-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="6f14b-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="6f14b-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
