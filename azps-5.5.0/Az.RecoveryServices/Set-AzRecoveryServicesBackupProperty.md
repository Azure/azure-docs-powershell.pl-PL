---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 17187a1a5caa2de3f39ad7153ee1313e4ee8e3e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191299"
---
# <span data-ttu-id="02a3a-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="02a3a-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="02a3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02a3a-102">SYNOPSIS</span></span>
<span data-ttu-id="02a3a-103">Ustawia właściwości zarządzania kopiami zapasowymi.</span><span class="sxs-lookup"><span data-stu-id="02a3a-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="02a3a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="02a3a-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>  [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-EnableCrossRegionRestore] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02a3a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="02a3a-105">DESCRIPTION</span></span>
<span data-ttu-id="02a3a-106">Polecenie **cmdlet Set-AzRecoveryServicesBackupProperty** ustawia właściwości magazynu kopii zapasowej dla magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="02a3a-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="02a3a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="02a3a-107">EXAMPLES</span></span>

### <span data-ttu-id="02a3a-108">Przykład 1. Ustawianie magazynu georedundantu dla magazynu</span><span class="sxs-lookup"><span data-stu-id="02a3a-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="02a3a-109">Pierwsze polecenie pobiera magazyn o nazwie TestVault, a następnie przechowuje go w zmiennej $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="02a3a-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="02a3a-110">Drugie polecenie ustawia nadmiarowość kopii zapasowej dla $Vault 01 na GeoRedundant.</span><span class="sxs-lookup"><span data-stu-id="02a3a-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="02a3a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02a3a-111">PARAMETERS</span></span>

### <span data-ttu-id="02a3a-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="02a3a-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="02a3a-113">Określa typ nadmiarowości magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="02a3a-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, ZoneRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a3a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a3a-114">-DefaultProfile</span></span>
<span data-ttu-id="02a3a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="02a3a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02a3a-116">— magazyn</span><span class="sxs-lookup"><span data-stu-id="02a3a-116">-Vault</span></span>
<span data-ttu-id="02a3a-117">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="02a3a-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="02a3a-118">Magazyn musi być obiektem **AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="02a3a-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02a3a-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02a3a-119">-Confirm</span></span>
<span data-ttu-id="02a3a-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="02a3a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a3a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a3a-121">-WhatIf</span></span>
<span data-ttu-id="02a3a-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02a3a-122">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="02a3a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a3a-123">CommonParameters</span></span>
<span data-ttu-id="02a3a-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a3a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a3a-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02a3a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a3a-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02a3a-126">INPUTS</span></span>

### <span data-ttu-id="02a3a-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="02a3a-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="02a3a-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02a3a-128">OUTPUTS</span></span>

### <span data-ttu-id="02a3a-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="02a3a-129">System.Void</span></span>

## <span data-ttu-id="02a3a-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="02a3a-130">NOTES</span></span>

## <span data-ttu-id="02a3a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02a3a-131">RELATED LINKS</span></span>

[<span data-ttu-id="02a3a-132">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="02a3a-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="02a3a-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="02a3a-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


