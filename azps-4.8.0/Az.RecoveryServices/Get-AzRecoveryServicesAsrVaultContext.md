---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221157"
---
# <span data-ttu-id="a7d0f-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="a7d0f-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="a7d0f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d0f-103">Pobiera informacje o ustawieniach magazynu ASR dotyczące magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="a7d0f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7d0f-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7d0f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a7d0f-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d0f-106">Polecenie cmdlet **Get-AzRecoveryServicesAsrVaultContext** pobiera informacje o ustawieniach magazynu ASR związane z magazynem usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="a7d0f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7d0f-107">EXAMPLES</span></span>

### <span data-ttu-id="a7d0f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a7d0f-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="a7d0f-109">Pobiera ustawienia magazynu ASR dla obecnie aktywnych (w ramach usługi odzyskiwania sesji programu PowerShell).</span><span class="sxs-lookup"><span data-stu-id="a7d0f-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="a7d0f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7d0f-110">PARAMETERS</span></span>

### <span data-ttu-id="a7d0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d0f-111">-DefaultProfile</span></span>
<span data-ttu-id="a7d0f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7d0f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d0f-113">CommonParameters</span></span>
<span data-ttu-id="a7d0f-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d0f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d0f-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7d0f-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d0f-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7d0f-116">INPUTS</span></span>

### <span data-ttu-id="a7d0f-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a7d0f-117">None</span></span>

## <span data-ttu-id="a7d0f-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7d0f-118">OUTPUTS</span></span>

### <span data-ttu-id="a7d0f-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="a7d0f-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="a7d0f-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7d0f-120">NOTES</span></span>

## <span data-ttu-id="a7d0f-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7d0f-121">RELATED LINKS</span></span>
