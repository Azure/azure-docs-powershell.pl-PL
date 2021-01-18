---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502623"
---
# <span data-ttu-id="20562-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="20562-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="20562-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20562-102">SYNOPSIS</span></span>

<span data-ttu-id="20562-103">Ustawia kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="20562-103">Sets vault context.</span></span>

## <span data-ttu-id="20562-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20562-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20562-105">Opis</span><span class="sxs-lookup"><span data-stu-id="20562-105">DESCRIPTION</span></span>

<span data-ttu-id="20562-106">Polecenie cmdlet **Set-AzRecoveryServicesVaultContext** ustawia kontekst magazynu dla usług odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="20562-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="20562-107">Ostrzeżenie: to polecenie cmdlet jest przestarzałe w przyszłym wydaniu w ramach zmiany.</span><span class="sxs-lookup"><span data-stu-id="20562-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="20562-108">Nie będzie to zamiennik.</span><span class="sxs-lookup"><span data-stu-id="20562-108">There will be no replacement for it.</span></span> <span data-ttu-id="20562-109">Użyj parametru-VaultId we wszystkich poleceniach usług odzyskiwania przechodzących dalej.</span><span class="sxs-lookup"><span data-stu-id="20562-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="20562-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20562-110">EXAMPLES</span></span>

### <span data-ttu-id="20562-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="20562-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="20562-112">Ustawia kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="20562-112">Sets vault context.</span></span>

## <span data-ttu-id="20562-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20562-113">PARAMETERS</span></span>

### <span data-ttu-id="20562-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20562-114">-DefaultProfile</span></span>

<span data-ttu-id="20562-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20562-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20562-116">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="20562-116">-Vault</span></span>

<span data-ttu-id="20562-117">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="20562-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="20562-118">Magazyn musi być obiektem **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="20562-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="20562-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20562-119">CommonParameters</span></span>
<span data-ttu-id="20562-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20562-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20562-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20562-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20562-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20562-122">INPUTS</span></span>

### <span data-ttu-id="20562-123">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="20562-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="20562-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20562-124">OUTPUTS</span></span>

### <span data-ttu-id="20562-125">System. void</span><span class="sxs-lookup"><span data-stu-id="20562-125">System.Void</span></span>

## <span data-ttu-id="20562-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20562-126">NOTES</span></span>

## <span data-ttu-id="20562-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20562-127">RELATED LINKS</span></span>
