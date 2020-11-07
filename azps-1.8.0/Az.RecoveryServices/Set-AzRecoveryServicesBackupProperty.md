---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 6912f54810baeeab795e5f2efca4a51ecafe1c93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708573"
---
# <span data-ttu-id="7e170-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="7e170-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="7e170-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e170-102">SYNOPSIS</span></span>
<span data-ttu-id="7e170-103">Ustawia właściwości zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="7e170-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="7e170-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e170-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e170-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7e170-105">DESCRIPTION</span></span>
<span data-ttu-id="7e170-106">Polecenie cmdlet **Set-AzRecoveryServicesBackupProperty** ustawia właściwości magazynu kopii zapasowej dla magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7e170-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="7e170-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e170-107">EXAMPLES</span></span>

### <span data-ttu-id="7e170-108">Przykład 1: Ustawianie magazynu geonadmiarowości w magazynie</span><span class="sxs-lookup"><span data-stu-id="7e170-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="7e170-109">Pierwsze polecenie uzyskuje magazyn o nazwie TestVault, a następnie zapisuje go w zmiennej $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="7e170-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="7e170-110">Drugie polecenie ustawia nadmiarowość miejsca do magazynowania kopii zapasowej $Vault 01 do georezerwowania.</span><span class="sxs-lookup"><span data-stu-id="7e170-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="7e170-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e170-111">PARAMETERS</span></span>

### <span data-ttu-id="7e170-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="7e170-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="7e170-113">Określa typ nadmiarowości miejsca do magazynowania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="7e170-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e170-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e170-114">-DefaultProfile</span></span>
<span data-ttu-id="7e170-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e170-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e170-116">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="7e170-116">-Vault</span></span>
<span data-ttu-id="7e170-117">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="7e170-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="7e170-118">Magazyn musi być obiektem **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="7e170-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="7e170-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e170-119">-Confirm</span></span>
<span data-ttu-id="7e170-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e170-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e170-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e170-121">-WhatIf</span></span>
<span data-ttu-id="7e170-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e170-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e170-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e170-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e170-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e170-124">CommonParameters</span></span>
<span data-ttu-id="7e170-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e170-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e170-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e170-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e170-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e170-127">INPUTS</span></span>

### <span data-ttu-id="7e170-128">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="7e170-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7e170-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e170-129">OUTPUTS</span></span>

### <span data-ttu-id="7e170-130">System. void</span><span class="sxs-lookup"><span data-stu-id="7e170-130">System.Void</span></span>

## <span data-ttu-id="7e170-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e170-131">NOTES</span></span>

## <span data-ttu-id="7e170-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e170-132">RELATED LINKS</span></span>

[<span data-ttu-id="7e170-133">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="7e170-133">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="7e170-134">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7e170-134">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

