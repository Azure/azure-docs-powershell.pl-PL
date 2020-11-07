---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: e7ce712102ffbb74fd8f19eed544642af5a6ebce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708711"
---
# <span data-ttu-id="83ff3-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="83ff3-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="83ff3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="83ff3-103">Pobiera skonfigurowane ustawienia powiadomień usługi Azure Site Recovery dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="83ff3-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="83ff3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83ff3-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83ff3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="83ff3-105">DESCRIPTION</span></span>
<span data-ttu-id="83ff3-106">Polecenie cmdlet **Get-AzRecoveryServicesAsrAlertSetting** pobiera skonfigurowane ustawienia powiadomień usługi Azure Site Recovery dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="83ff3-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="83ff3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83ff3-107">EXAMPLES</span></span>

### <span data-ttu-id="83ff3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="83ff3-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="83ff3-109">Pobieranie alertu/ustawienia powiadomień dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="83ff3-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="83ff3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83ff3-110">PARAMETERS</span></span>

### <span data-ttu-id="83ff3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ff3-111">-DefaultProfile</span></span>
<span data-ttu-id="83ff3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="83ff3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83ff3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ff3-113">CommonParameters</span></span>
<span data-ttu-id="83ff3-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ff3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ff3-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83ff3-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ff3-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83ff3-116">INPUTS</span></span>

### <span data-ttu-id="83ff3-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="83ff3-117">None</span></span>

## <span data-ttu-id="83ff3-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83ff3-118">OUTPUTS</span></span>

### <span data-ttu-id="83ff3-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="83ff3-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="83ff3-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83ff3-120">NOTES</span></span>

## <span data-ttu-id="83ff3-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83ff3-121">RELATED LINKS</span></span>
