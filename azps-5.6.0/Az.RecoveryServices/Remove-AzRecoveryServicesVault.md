---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: b3d0b292d7e680ca1d16e935c34a268cea836aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953114"
---
# <span data-ttu-id="6205f-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6205f-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="6205f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6205f-102">SYNOPSIS</span></span>
<span data-ttu-id="6205f-103">Usuwa magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6205f-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="6205f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6205f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6205f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6205f-105">DESCRIPTION</span></span>
<span data-ttu-id="6205f-106">Polecenie **cmdlet Remove-AzRecoveryServicesVault** usuwa magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6205f-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="6205f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6205f-107">EXAMPLES</span></span>

### <span data-ttu-id="6205f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6205f-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="6205f-109">Usuwa magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="6205f-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="6205f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6205f-110">PARAMETERS</span></span>

### <span data-ttu-id="6205f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6205f-111">-DefaultProfile</span></span>
<span data-ttu-id="6205f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6205f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6205f-113">— magazyn</span><span class="sxs-lookup"><span data-stu-id="6205f-113">-Vault</span></span>
<span data-ttu-id="6205f-114">Określa obiekt magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6205f-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="6205f-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6205f-115">-Confirm</span></span>
<span data-ttu-id="6205f-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6205f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6205f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6205f-117">-WhatIf</span></span>
<span data-ttu-id="6205f-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6205f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6205f-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6205f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6205f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6205f-120">CommonParameters</span></span>
<span data-ttu-id="6205f-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6205f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6205f-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6205f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6205f-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6205f-123">INPUTS</span></span>

### <span data-ttu-id="6205f-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="6205f-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="6205f-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6205f-125">OUTPUTS</span></span>

### <span data-ttu-id="6205f-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="6205f-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="6205f-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6205f-127">NOTES</span></span>

## <span data-ttu-id="6205f-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6205f-128">RELATED LINKS</span></span>

[<span data-ttu-id="6205f-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6205f-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="6205f-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="6205f-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="6205f-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6205f-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


