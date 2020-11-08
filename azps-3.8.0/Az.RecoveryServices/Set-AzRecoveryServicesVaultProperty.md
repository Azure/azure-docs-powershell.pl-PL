---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a9bd1eead98a7afb06e1f5b480f8a65fc5079bd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052487"
---
# <span data-ttu-id="a94ea-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="a94ea-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="a94ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a94ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a94ea-103">Aktualizuje właściwości magazynu.</span><span class="sxs-lookup"><span data-stu-id="a94ea-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="a94ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a94ea-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a94ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a94ea-105">DESCRIPTION</span></span>
<span data-ttu-id="a94ea-106">Polecenie cmdlet **Set-AzRecoveryServicesVaultProperty** aktualizuje właściwości magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a94ea-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="a94ea-107">Aby uzyskać bieżące właściwości magazynu, można użyć polecenia cmdlet **Set-AzRecoveryServicesVaultProperty** .</span><span class="sxs-lookup"><span data-stu-id="a94ea-107">You can use **Set-AzRecoveryServicesVaultProperty** cmdlet to get the current properties of a vault.</span></span>
<span data-ttu-id="a94ea-108">Za pomocą tego polecenia cmdlet **SoftDeleteFeatureState** w magazynie można włączyć w dowolnym momencie.</span><span class="sxs-lookup"><span data-stu-id="a94ea-108">Using this cmdlet **SoftDeleteFeatureState** property of a vault can be enabled at any point of time.</span></span>
<span data-ttu-id="a94ea-109">Właściwość **SoftDeleteFeatureState** magazynu może być wyłączona tylko wtedy, gdy w magazynie nie ma zarejestrowanych kontenerów.</span><span class="sxs-lookup"><span data-stu-id="a94ea-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>
<span data-ttu-id="a94ea-110">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="a94ea-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a94ea-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a94ea-111">EXAMPLES</span></span>

### <span data-ttu-id="a94ea-112">Przykład 1: aktualizowanie SoftDeleteFeatureState magazynu</span><span class="sxs-lookup"><span data-stu-id="a94ea-112">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="a94ea-113">Pierwsze polecenie pobiera obiekt magazynu, a następnie zapisuje go w zmiennej $vault.</span><span class="sxs-lookup"><span data-stu-id="a94ea-113">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="a94ea-114">Drugie polecenie aktualizuje stan "włączony" dla właściwości SoftDeleteFeatureState magazynu.</span><span class="sxs-lookup"><span data-stu-id="a94ea-114">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="a94ea-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a94ea-115">PARAMETERS</span></span>

### <span data-ttu-id="a94ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a94ea-116">-DefaultProfile</span></span>
<span data-ttu-id="a94ea-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a94ea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a94ea-118">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="a94ea-118">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="a94ea-119">SoftDeleteFeatureState usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="a94ea-119">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a94ea-120">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a94ea-120">-VaultId</span></span>
<span data-ttu-id="a94ea-121">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="a94ea-121">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a94ea-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a94ea-122">-Confirm</span></span>
<span data-ttu-id="a94ea-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a94ea-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a94ea-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a94ea-124">-WhatIf</span></span>
<span data-ttu-id="a94ea-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a94ea-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a94ea-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a94ea-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a94ea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a94ea-127">CommonParameters</span></span>
<span data-ttu-id="a94ea-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a94ea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a94ea-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a94ea-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a94ea-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a94ea-130">INPUTS</span></span>

### <span data-ttu-id="a94ea-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a94ea-131">System.String</span></span>

### <span data-ttu-id="a94ea-132">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="a94ea-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="a94ea-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a94ea-133">OUTPUTS</span></span>

### <span data-ttu-id="a94ea-134">Microsoft. Azure. Management. RecoveryServices. Backup. models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="a94ea-134">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="a94ea-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a94ea-135">NOTES</span></span>

## <span data-ttu-id="a94ea-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a94ea-136">RELATED LINKS</span></span>

[<span data-ttu-id="a94ea-137">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a94ea-137">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="a94ea-138">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="a94ea-138">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


