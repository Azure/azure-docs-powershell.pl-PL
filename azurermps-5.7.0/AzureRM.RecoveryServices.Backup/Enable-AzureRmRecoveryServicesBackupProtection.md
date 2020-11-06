---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: efe4392fd57c5cb0beb6731fefb83878001b489b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526730"
---
# <span data-ttu-id="f97e0-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f97e0-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="f97e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f97e0-102">SYNOPSIS</span></span>
<span data-ttu-id="f97e0-103">Umożliwia tworzenie kopii zapasowej elementu z określonymi zasadami ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="f97e0-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f97e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f97e0-104">SYNTAX</span></span>

### <span data-ttu-id="f97e0-105">AzureVMComputeEnableProtection (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f97e0-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f97e0-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="f97e0-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f97e0-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="f97e0-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f97e0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f97e0-108">DESCRIPTION</span></span>
<span data-ttu-id="f97e0-109">Polecenie cmdlet **enable-AzureRmRecoveryServicesBackupProtection** ustawia zasady ochrony kopii zapasowych Azure dla elementu.</span><span class="sxs-lookup"><span data-stu-id="f97e0-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="f97e0-110">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="f97e0-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f97e0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f97e0-111">EXAMPLES</span></span>

### <span data-ttu-id="f97e0-112">Przykład 1: Włączanie ochrony przed kopiami zapasowymi dla elementu</span><span class="sxs-lookup"><span data-stu-id="f97e0-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="f97e0-113">Pierwsze polecenie cmdlet Pobiera domyślny obiekt zasad, a następnie zapisuje go w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="f97e0-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="f97e0-114">Drugie polecenie cmdlet ustawia zasady ochrony kopii zapasowych dla maszyny wirtualnej ARM o nazwie V2VM przy użyciu zasad w $Pol.</span><span class="sxs-lookup"><span data-stu-id="f97e0-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="f97e0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f97e0-115">PARAMETERS</span></span>

### <span data-ttu-id="f97e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f97e0-116">-DefaultProfile</span></span>
<span data-ttu-id="f97e0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f97e0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f97e0-118">-Item</span><span class="sxs-lookup"><span data-stu-id="f97e0-118">-Item</span></span>
<span data-ttu-id="f97e0-119">Określa element kopii zapasowej, dla którego to polecenie cmdlet włącza ochronę.</span><span class="sxs-lookup"><span data-stu-id="f97e0-119">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="f97e0-120">Aby uzyskać **AzureRmRecoveryServicesBackupItem** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="f97e0-120">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f97e0-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f97e0-121">-Name</span></span>
<span data-ttu-id="f97e0-122">Określa nazwę elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f97e0-122">Specifies the name of the Backup item.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f97e0-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="f97e0-123">-Policy</span></span>
<span data-ttu-id="f97e0-124">Określa zasady ochrony, które to polecenie cmdlet kojarzy z elementem.</span><span class="sxs-lookup"><span data-stu-id="f97e0-124">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="f97e0-125">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupProtectionPolicy** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f97e0-125">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97e0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f97e0-126">-ResourceGroupName</span></span>
<span data-ttu-id="f97e0-127">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f97e0-127">Specifies the name of the resource group.</span></span>
<span data-ttu-id="f97e0-128">Ten parametr należy określić tylko dla maszyn wirtualnych ARM.</span><span class="sxs-lookup"><span data-stu-id="f97e0-128">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f97e0-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f97e0-129">-ServiceName</span></span>
<span data-ttu-id="f97e0-130">Określa nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="f97e0-130">Specifies the service name.</span></span>
<span data-ttu-id="f97e0-131">Ten parametr należy określić tylko dla maszyn wirtualnych ASM.</span><span class="sxs-lookup"><span data-stu-id="f97e0-131">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f97e0-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f97e0-132">-Confirm</span></span>
<span data-ttu-id="f97e0-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f97e0-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97e0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f97e0-134">-WhatIf</span></span>
<span data-ttu-id="f97e0-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f97e0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f97e0-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f97e0-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f97e0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f97e0-137">CommonParameters</span></span>
<span data-ttu-id="f97e0-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f97e0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f97e0-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f97e0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f97e0-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f97e0-140">INPUTS</span></span>

### <span data-ttu-id="f97e0-141">ItemBase</span><span class="sxs-lookup"><span data-stu-id="f97e0-141">ItemBase</span></span>
<span data-ttu-id="f97e0-142">Parametr "element" akceptuje wartość typu "ItemBase" z potoku</span><span class="sxs-lookup"><span data-stu-id="f97e0-142">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="f97e0-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f97e0-143">OUTPUTS</span></span>

### <span data-ttu-id="f97e0-144">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="f97e0-144">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f97e0-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f97e0-145">NOTES</span></span>

## <span data-ttu-id="f97e0-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f97e0-146">RELATED LINKS</span></span>

[<span data-ttu-id="f97e0-147">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f97e0-147">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="f97e0-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f97e0-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


