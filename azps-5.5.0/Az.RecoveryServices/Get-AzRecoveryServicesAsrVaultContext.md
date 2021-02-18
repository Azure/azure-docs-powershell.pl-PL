---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202027"
---
# <span data-ttu-id="99c03-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="99c03-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="99c03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99c03-102">SYNOPSIS</span></span>
<span data-ttu-id="99c03-103">Pobiera informacje o ustawieniach magazynu usługi odzyskiwania dla magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="99c03-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="99c03-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99c03-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99c03-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="99c03-105">DESCRIPTION</span></span>
<span data-ttu-id="99c03-106">Polecenie **cmdlet Get-AzRecoveryServicesAsrVaultContext** pobiera informacje o ustawieniach magazynu asr związane z magazynem usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="99c03-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="99c03-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99c03-107">EXAMPLES</span></span>

### <span data-ttu-id="99c03-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99c03-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="99c03-109">Pobiera ustawienia magazynu asr dla obecnie aktywnego (w sesji programu PowerShell) magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="99c03-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="99c03-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99c03-110">PARAMETERS</span></span>

### <span data-ttu-id="99c03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c03-111">-DefaultProfile</span></span>
<span data-ttu-id="99c03-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="99c03-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99c03-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c03-113">CommonParameters</span></span>
<span data-ttu-id="99c03-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99c03-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c03-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99c03-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c03-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99c03-116">INPUTS</span></span>

### <span data-ttu-id="99c03-117">Brak</span><span class="sxs-lookup"><span data-stu-id="99c03-117">None</span></span>

## <span data-ttu-id="99c03-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99c03-118">OUTPUTS</span></span>

### <span data-ttu-id="99c03-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="99c03-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="99c03-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99c03-120">NOTES</span></span>

## <span data-ttu-id="99c03-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99c03-121">RELATED LINKS</span></span>
