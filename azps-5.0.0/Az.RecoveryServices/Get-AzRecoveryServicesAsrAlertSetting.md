---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309001"
---
# <span data-ttu-id="e7065-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="e7065-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="e7065-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7065-102">SYNOPSIS</span></span>
<span data-ttu-id="e7065-103">Pobiera skonfigurowane ustawienia powiadomień usługi Azure Site Recovery dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="e7065-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="e7065-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7065-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7065-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e7065-105">DESCRIPTION</span></span>
<span data-ttu-id="e7065-106">Polecenie cmdlet **Get-AzRecoveryServicesAsrAlertSetting** pobiera skonfigurowane ustawienia powiadomień usługi Azure Site Recovery dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="e7065-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="e7065-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7065-107">EXAMPLES</span></span>

### <span data-ttu-id="e7065-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7065-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="e7065-109">Pobieranie alertu/ustawienia powiadomień dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e7065-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="e7065-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7065-110">PARAMETERS</span></span>

### <span data-ttu-id="e7065-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7065-111">-DefaultProfile</span></span>
<span data-ttu-id="e7065-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7065-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7065-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7065-113">CommonParameters</span></span>
<span data-ttu-id="e7065-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7065-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7065-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7065-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7065-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7065-116">INPUTS</span></span>

### <span data-ttu-id="e7065-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e7065-117">None</span></span>

## <span data-ttu-id="e7065-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7065-118">OUTPUTS</span></span>

### <span data-ttu-id="e7065-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="e7065-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="e7065-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7065-120">NOTES</span></span>

## <span data-ttu-id="e7065-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7065-121">RELATED LINKS</span></span>
