---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371282"
---
# <span data-ttu-id="2f275-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="2f275-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="2f275-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f275-102">SYNOPSIS</span></span>
<span data-ttu-id="2f275-103">Aktualizuje właściwości magazynu.</span><span class="sxs-lookup"><span data-stu-id="2f275-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="2f275-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f275-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f275-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2f275-105">DESCRIPTION</span></span>
<span data-ttu-id="2f275-106">Polecenie cmdlet **Set-AzRecoveryServicesVaultProperty** aktualizuje właściwości magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="2f275-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="2f275-107">To polecenie cmdlet zwraca zaktualizowane właściwości magazynu po bieżącej operacji set.</span><span class="sxs-lookup"><span data-stu-id="2f275-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="2f275-108">Za pomocą tych właściwości polecenia cmdlet magazynu, takich jak Soft-Delete, można włączyć w dowolnym momencie.</span><span class="sxs-lookup"><span data-stu-id="2f275-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="2f275-109">Właściwość **SoftDeleteFeatureState** magazynu może być wyłączona tylko wtedy, gdy w magazynie nie ma zarejestrowanych kontenerów.</span><span class="sxs-lookup"><span data-stu-id="2f275-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="2f275-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f275-110">EXAMPLES</span></span>

### <span data-ttu-id="2f275-111">Przykład 1: aktualizowanie SoftDeleteFeatureState magazynu</span><span class="sxs-lookup"><span data-stu-id="2f275-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="2f275-112">Pierwsze polecenie pobiera obiekt magazynu, a następnie zapisuje go w zmiennej $vault.</span><span class="sxs-lookup"><span data-stu-id="2f275-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="2f275-113">Drugie polecenie aktualizuje stan "włączony" dla właściwości SoftDeleteFeatureState magazynu.</span><span class="sxs-lookup"><span data-stu-id="2f275-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="2f275-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f275-114">PARAMETERS</span></span>

### <span data-ttu-id="2f275-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f275-115">-DefaultProfile</span></span>
<span data-ttu-id="2f275-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f275-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f275-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="2f275-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="2f275-118">SoftDeleteFeatureState usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2f275-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2f275-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2f275-119">-VaultId</span></span>
<span data-ttu-id="2f275-120">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2f275-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2f275-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f275-121">-Confirm</span></span>
<span data-ttu-id="2f275-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f275-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f275-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f275-123">-WhatIf</span></span>
<span data-ttu-id="2f275-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f275-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="2f275-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f275-125">CommonParameters</span></span>
<span data-ttu-id="2f275-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f275-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f275-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f275-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f275-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f275-128">INPUTS</span></span>

### <span data-ttu-id="2f275-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2f275-129">System.String</span></span>

### <span data-ttu-id="2f275-130">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="2f275-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="2f275-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f275-131">OUTPUTS</span></span>

### <span data-ttu-id="2f275-132">Microsoft. Azure. Management. RecoveryServices. Backup. models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="2f275-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="2f275-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f275-133">NOTES</span></span>

## <span data-ttu-id="2f275-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f275-134">RELATED LINKS</span></span>

[<span data-ttu-id="2f275-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="2f275-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="2f275-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="2f275-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


