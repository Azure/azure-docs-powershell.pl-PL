---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 6a611017b2effa4733b75f56e6799f6857dcdfa8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886617"
---
# <span data-ttu-id="38cb7-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="38cb7-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="38cb7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38cb7-102">SYNOPSIS</span></span>

<span data-ttu-id="38cb7-103">Ustawia kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="38cb7-103">Sets vault context.</span></span>

## <span data-ttu-id="38cb7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38cb7-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38cb7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="38cb7-105">DESCRIPTION</span></span>

<span data-ttu-id="38cb7-106">Polecenie cmdlet **Set-AzRecoveryServicesVaultContext** ustawia kontekst magazynu dla usług odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38cb7-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="38cb7-107">Ostrzeżenie: to polecenie cmdlet jest przestarzałe w przyszłym wydaniu w ramach zmiany.</span><span class="sxs-lookup"><span data-stu-id="38cb7-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="38cb7-108">Nie będzie to zamiennik.</span><span class="sxs-lookup"><span data-stu-id="38cb7-108">There will be no replacement for it.</span></span> <span data-ttu-id="38cb7-109">Użyj parametru-VaultId we wszystkich poleceniach usług odzyskiwania przechodzących dalej.</span><span class="sxs-lookup"><span data-stu-id="38cb7-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="38cb7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38cb7-110">EXAMPLES</span></span>

### <span data-ttu-id="38cb7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="38cb7-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="38cb7-112">Ustawia kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="38cb7-112">Sets vault context.</span></span>

## <span data-ttu-id="38cb7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38cb7-113">PARAMETERS</span></span>

### <span data-ttu-id="38cb7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38cb7-114">-DefaultProfile</span></span>

<span data-ttu-id="38cb7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38cb7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38cb7-116">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="38cb7-116">-Vault</span></span>

<span data-ttu-id="38cb7-117">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="38cb7-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="38cb7-118">Magazyn musi być obiektem **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="38cb7-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="38cb7-119">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38cb7-119">-CommonParameters</span></span>

<span data-ttu-id="38cb7-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38cb7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38cb7-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38cb7-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38cb7-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38cb7-122">INPUTS</span></span>

### <span data-ttu-id="38cb7-123">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="38cb7-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="38cb7-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38cb7-124">OUTPUTS</span></span>

### <span data-ttu-id="38cb7-125">System. void</span><span class="sxs-lookup"><span data-stu-id="38cb7-125">System.Void</span></span>

## <span data-ttu-id="38cb7-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38cb7-126">NOTES</span></span>

## <span data-ttu-id="38cb7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38cb7-127">RELATED LINKS</span></span>
