---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 846c27dc521e13cb2814a4f9e004325da4263bf7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708574"
---
# <span data-ttu-id="5f227-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="5f227-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="5f227-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f227-102">SYNOPSIS</span></span>
<span data-ttu-id="5f227-103">Umożliwia ustawienie kontekstu magazynu usług odzyskiwania, który ma być stosowany do kolejnych operacji odzyskiwania witryny platformy Azure w bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5f227-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="5f227-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f227-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f227-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5f227-105">DESCRIPTION</span></span>
<span data-ttu-id="5f227-106">Polecenie cmdlet **Set-AzRecoveryServicesAsrVaultContext** ustawia kontekst magazynu usługi Azure Site Recovery dla kolejnych operacji.</span><span class="sxs-lookup"><span data-stu-id="5f227-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="5f227-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f227-107">EXAMPLES</span></span>

### <span data-ttu-id="5f227-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5f227-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="5f227-109">Ustawia kontekst magazynu dla określonego magazynu usług odzyskiwania dla kolejnych operacji odzyskiwania witryny platformy Azure w bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5f227-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="5f227-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f227-110">PARAMETERS</span></span>

### <span data-ttu-id="5f227-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f227-111">-DefaultProfile</span></span>
<span data-ttu-id="5f227-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f227-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f227-113">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="5f227-113">-Vault</span></span>
<span data-ttu-id="5f227-114">Obiekt magazynu usług Recovery Services odpowiadający magazynowi usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5f227-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="5f227-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f227-115">-Confirm</span></span>
<span data-ttu-id="5f227-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f227-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f227-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f227-117">-WhatIf</span></span>
<span data-ttu-id="5f227-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f227-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f227-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5f227-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f227-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f227-120">CommonParameters</span></span>
<span data-ttu-id="5f227-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f227-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f227-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f227-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f227-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f227-123">INPUTS</span></span>

### <span data-ttu-id="5f227-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="5f227-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="5f227-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f227-125">OUTPUTS</span></span>

### <span data-ttu-id="5f227-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="5f227-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="5f227-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f227-127">NOTES</span></span>

## <span data-ttu-id="5f227-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f227-128">RELATED LINKS</span></span>