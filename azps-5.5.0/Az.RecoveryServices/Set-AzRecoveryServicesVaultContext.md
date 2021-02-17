---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191291"
---
# <span data-ttu-id="af971-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="af971-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="af971-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af971-102">SYNOPSIS</span></span>

<span data-ttu-id="af971-103">Ustawia kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="af971-103">Sets vault context.</span></span>

## <span data-ttu-id="af971-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="af971-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af971-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="af971-105">DESCRIPTION</span></span>

<span data-ttu-id="af971-106">Polecenie **cmdlet Set-AzRecoveryServicesVaultContext** ustawia kontekst magazynu dla usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="af971-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="af971-107">Ostrzeżenie: To polecenie cmdlet jest przestarzałe w przyszłej wersji zmieniania podziału.</span><span class="sxs-lookup"><span data-stu-id="af971-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="af971-108">Nie będzie go można zastąpić.</span><span class="sxs-lookup"><span data-stu-id="af971-108">There will be no replacement for it.</span></span> <span data-ttu-id="af971-109">Użyj parametru -VaultId we wszystkich poleceniach usługi odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="af971-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="af971-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="af971-110">EXAMPLES</span></span>

### <span data-ttu-id="af971-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="af971-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="af971-112">Ustawia kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="af971-112">Sets vault context.</span></span>

## <span data-ttu-id="af971-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af971-113">PARAMETERS</span></span>

### <span data-ttu-id="af971-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af971-114">-DefaultProfile</span></span>

<span data-ttu-id="af971-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="af971-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af971-116">— magazyn</span><span class="sxs-lookup"><span data-stu-id="af971-116">-Vault</span></span>

<span data-ttu-id="af971-117">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="af971-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="af971-118">Magazyn musi być obiektem **AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="af971-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="af971-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af971-119">CommonParameters</span></span>
<span data-ttu-id="af971-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af971-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af971-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af971-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af971-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af971-122">INPUTS</span></span>

### <span data-ttu-id="af971-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="af971-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="af971-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="af971-124">OUTPUTS</span></span>

### <span data-ttu-id="af971-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="af971-125">System.Void</span></span>

## <span data-ttu-id="af971-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="af971-126">NOTES</span></span>

## <span data-ttu-id="af971-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af971-127">RELATED LINKS</span></span>
