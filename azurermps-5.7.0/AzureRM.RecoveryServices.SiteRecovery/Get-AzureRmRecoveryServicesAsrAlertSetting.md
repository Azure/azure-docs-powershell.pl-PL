---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: d1da03455fad47d889269c0d961def70df6837e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717717"
---
# <span data-ttu-id="e3172-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="e3172-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="e3172-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3172-102">SYNOPSIS</span></span>
<span data-ttu-id="e3172-103">Pobiera skonfigurowane ustawienia powiadomień usługi Azure Site Recovery dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="e3172-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3172-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3172-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3172-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3172-105">DESCRIPTION</span></span>
<span data-ttu-id="e3172-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrAlertSetting** pobiera skonfigurowane ustawienia powiadomień usługi Azure Site Recovery dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="e3172-106">The **Get-AzureRmRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="e3172-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3172-107">EXAMPLES</span></span>

### <span data-ttu-id="e3172-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e3172-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="e3172-109">Pobieranie alertu/ustawienia powiadomień dla usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e3172-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="e3172-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3172-110">PARAMETERS</span></span>

### <span data-ttu-id="e3172-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3172-111">-DefaultProfile</span></span>
<span data-ttu-id="e3172-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3172-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3172-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3172-113">CommonParameters</span></span>
<span data-ttu-id="e3172-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3172-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3172-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3172-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3172-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3172-116">INPUTS</span></span>

### <span data-ttu-id="e3172-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e3172-117">None</span></span>

## <span data-ttu-id="e3172-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3172-118">OUTPUTS</span></span>

### <span data-ttu-id="e3172-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e3172-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e3172-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3172-120">NOTES</span></span>

## <span data-ttu-id="e3172-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3172-121">RELATED LINKS</span></span>
