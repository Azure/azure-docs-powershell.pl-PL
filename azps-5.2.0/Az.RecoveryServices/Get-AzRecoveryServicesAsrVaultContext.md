---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352558"
---
# <span data-ttu-id="84914-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="84914-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="84914-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84914-102">SYNOPSIS</span></span>
<span data-ttu-id="84914-103">Pobiera informacje o ustawieniach magazynu ASR dotyczące magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="84914-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="84914-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84914-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84914-105">Opis</span><span class="sxs-lookup"><span data-stu-id="84914-105">DESCRIPTION</span></span>
<span data-ttu-id="84914-106">Polecenie cmdlet **Get-AzRecoveryServicesAsrVaultContext** pobiera informacje o ustawieniach magazynu ASR związane z magazynem usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="84914-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="84914-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84914-107">EXAMPLES</span></span>

### <span data-ttu-id="84914-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84914-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="84914-109">Pobiera ustawienia magazynu ASR dla obecnie aktywnych (w ramach usługi odzyskiwania sesji programu PowerShell).</span><span class="sxs-lookup"><span data-stu-id="84914-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="84914-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84914-110">PARAMETERS</span></span>

### <span data-ttu-id="84914-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84914-111">-DefaultProfile</span></span>
<span data-ttu-id="84914-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84914-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84914-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84914-113">CommonParameters</span></span>
<span data-ttu-id="84914-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84914-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84914-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84914-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84914-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84914-116">INPUTS</span></span>

### <span data-ttu-id="84914-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="84914-117">None</span></span>

## <span data-ttu-id="84914-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84914-118">OUTPUTS</span></span>

### <span data-ttu-id="84914-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="84914-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="84914-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84914-120">NOTES</span></span>

## <span data-ttu-id="84914-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84914-121">RELATED LINKS</span></span>
