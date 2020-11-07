---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 357256d1c1a754915cbebc978e5c4ccf4440ccf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718288"
---
# <span data-ttu-id="d1ecb-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d1ecb-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="d1ecb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ecb-103">Umożliwia tworzenie kopii zapasowej elementu z określonymi zasadami ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1ecb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1ecb-104">SYNTAX</span></span>

### <span data-ttu-id="d1ecb-105">AzureVMComputeEnableProtection (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d1ecb-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1ecb-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="d1ecb-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1ecb-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="d1ecb-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 -StorageAccountName <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1ecb-108">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="d1ecb-108">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1ecb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d1ecb-109">DESCRIPTION</span></span>
<span data-ttu-id="d1ecb-110">Polecenie cmdlet **enable-AzureRmRecoveryServicesBackupProtection** ustawia zasady ochrony kopii zapasowych Azure dla elementu.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-110">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="d1ecb-111">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d1ecb-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1ecb-112">EXAMPLES</span></span>

### <span data-ttu-id="d1ecb-113">Przykład 1: Włączanie ochrony przed kopiami zapasowymi dla elementu</span><span class="sxs-lookup"><span data-stu-id="d1ecb-113">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="d1ecb-114">Pierwsze polecenie cmdlet Pobiera domyślny obiekt zasad, a następnie zapisuje go w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-114">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="d1ecb-115">Drugie polecenie cmdlet ustawia zasady ochrony kopii zapasowych dla maszyny wirtualnej ARM o nazwie V2VM przy użyciu zasad w $Pol.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-115">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="d1ecb-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1ecb-116">PARAMETERS</span></span>

### <span data-ttu-id="d1ecb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ecb-117">-DefaultProfile</span></span>
<span data-ttu-id="d1ecb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1ecb-119">-Item</span><span class="sxs-lookup"><span data-stu-id="d1ecb-119">-Item</span></span>
<span data-ttu-id="d1ecb-120">Określa element kopii zapasowej, dla którego to polecenie cmdlet włącza ochronę.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-120">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="d1ecb-121">Aby uzyskać **AzureRmRecoveryServicesBackupItem** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-121">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ecb-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1ecb-122">-Name</span></span>
<span data-ttu-id="d1ecb-123">Określa nazwę elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-123">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ecb-124">-Policy</span><span class="sxs-lookup"><span data-stu-id="d1ecb-124">-Policy</span></span>
<span data-ttu-id="d1ecb-125">Określa zasady ochrony, które to polecenie cmdlet kojarzy z elementem.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="d1ecb-126">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupProtectionPolicy** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-126">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ecb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1ecb-127">-ResourceGroupName</span></span>
<span data-ttu-id="d1ecb-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-128">Specifies the name of the resource group.</span></span>
<span data-ttu-id="d1ecb-129">Ten parametr należy określić tylko dla maszyn wirtualnych ARM.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-129">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ecb-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d1ecb-130">-ServiceName</span></span>
<span data-ttu-id="d1ecb-131">Określa nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-131">Specifies the service name.</span></span>
<span data-ttu-id="d1ecb-132">Ten parametr należy określić tylko dla maszyn wirtualnych ASM.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-132">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ecb-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d1ecb-133">-StorageAccountName</span></span>
<span data-ttu-id="d1ecb-134">Nazwa konta magazynu udziału plików w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="d1ecb-134">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ecb-135">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d1ecb-135">-VaultId</span></span>
<span data-ttu-id="d1ecb-136">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-136">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d1ecb-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1ecb-137">-Confirm</span></span>
<span data-ttu-id="d1ecb-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1ecb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1ecb-139">-WhatIf</span></span>
<span data-ttu-id="d1ecb-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1ecb-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1ecb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ecb-142">CommonParameters</span></span>
<span data-ttu-id="d1ecb-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ecb-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1ecb-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ecb-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1ecb-145">INPUTS</span></span>

### <span data-ttu-id="d1ecb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d1ecb-146">System.String</span></span>
<span data-ttu-id="d1ecb-147">Parametry: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d1ecb-147">Parameters: VaultId (ByValue)</span></span>

### <span data-ttu-id="d1ecb-148">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="d1ecb-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="d1ecb-149">Parametry: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d1ecb-149">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="d1ecb-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1ecb-150">OUTPUTS</span></span>

### <span data-ttu-id="d1ecb-151">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="d1ecb-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d1ecb-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1ecb-152">NOTES</span></span>

## <span data-ttu-id="d1ecb-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1ecb-153">RELATED LINKS</span></span>

[<span data-ttu-id="d1ecb-154">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d1ecb-154">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="d1ecb-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d1ecb-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


