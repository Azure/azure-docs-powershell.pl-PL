---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 04fa3c9a7024b8a9e1f525a4ef131ae151f25804
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997396"
---
# <span data-ttu-id="db913-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="db913-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="db913-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db913-102">SYNOPSIS</span></span>

<span data-ttu-id="db913-103">Ustawia kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="db913-103">Sets vault context.</span></span>

## <span data-ttu-id="db913-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="db913-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db913-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="db913-105">DESCRIPTION</span></span>

<span data-ttu-id="db913-106">Polecenie **cmdlet Set-AzRecoveryServicesVaultContext** ustawia kontekst magazynu dla usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="db913-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="db913-107">Ostrzeżenie: To polecenie cmdlet jest przestarzałe w przyszłej wersji zmieniania podziału.</span><span class="sxs-lookup"><span data-stu-id="db913-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="db913-108">Nie będzie go można zastąpić.</span><span class="sxs-lookup"><span data-stu-id="db913-108">There will be no replacement for it.</span></span> <span data-ttu-id="db913-109">Użyj parametru -VaultId we wszystkich poleceniach usługi odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="db913-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="db913-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="db913-110">EXAMPLES</span></span>

### <span data-ttu-id="db913-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="db913-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="db913-112">Ustawia kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="db913-112">Sets vault context.</span></span>

## <span data-ttu-id="db913-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db913-113">PARAMETERS</span></span>

### <span data-ttu-id="db913-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db913-114">-DefaultProfile</span></span>

<span data-ttu-id="db913-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="db913-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db913-116">— magazyn</span><span class="sxs-lookup"><span data-stu-id="db913-116">-Vault</span></span>

<span data-ttu-id="db913-117">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="db913-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="db913-118">Magazyn musi być obiektem **AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="db913-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="db913-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db913-119">CommonParameters</span></span>
<span data-ttu-id="db913-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db913-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db913-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db913-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db913-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db913-122">INPUTS</span></span>

### <span data-ttu-id="db913-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="db913-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="db913-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db913-124">OUTPUTS</span></span>

### <span data-ttu-id="db913-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="db913-125">System.Void</span></span>

## <span data-ttu-id="db913-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="db913-126">NOTES</span></span>

## <span data-ttu-id="db913-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db913-127">RELATED LINKS</span></span>
