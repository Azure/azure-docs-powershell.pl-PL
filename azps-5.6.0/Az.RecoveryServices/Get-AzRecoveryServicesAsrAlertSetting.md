---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: cadde5ec773452897aa9c6915a5f3e16f00cfef5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007681"
---
# <span data-ttu-id="b12d7-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="b12d7-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="b12d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b12d7-102">SYNOPSIS</span></span>
<span data-ttu-id="b12d7-103">Pobiera skonfigurowane ustawienia powiadomień usługi Azure Site Recovery dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="b12d7-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="b12d7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b12d7-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b12d7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b12d7-105">DESCRIPTION</span></span>
<span data-ttu-id="b12d7-106">Polecenie **cmdlet Get-AzRecoveryServicesAsrAlertSetting** pobiera skonfigurowane ustawienia powiadomień usługi Azure Site Recovery dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="b12d7-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="b12d7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b12d7-107">EXAMPLES</span></span>

### <span data-ttu-id="b12d7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b12d7-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="b12d7-109">Uzyskaj alert / ustawienie powiadomień dotyczące odzyskiwania witryn platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b12d7-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="b12d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b12d7-110">PARAMETERS</span></span>

### <span data-ttu-id="b12d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b12d7-111">-DefaultProfile</span></span>
<span data-ttu-id="b12d7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b12d7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b12d7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b12d7-113">CommonParameters</span></span>
<span data-ttu-id="b12d7-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b12d7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b12d7-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b12d7-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b12d7-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b12d7-116">INPUTS</span></span>

### <span data-ttu-id="b12d7-117">Brak</span><span class="sxs-lookup"><span data-stu-id="b12d7-117">None</span></span>

## <span data-ttu-id="b12d7-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b12d7-118">OUTPUTS</span></span>

### <span data-ttu-id="b12d7-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="b12d7-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="b12d7-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b12d7-120">NOTES</span></span>

## <span data-ttu-id="b12d7-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b12d7-121">RELATED LINKS</span></span>
