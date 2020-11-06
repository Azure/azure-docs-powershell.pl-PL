---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 2be1ca7de1728d1aed7758cd170cb608c7645f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551660"
---
# <span data-ttu-id="c5542-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="c5542-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="c5542-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5542-102">SYNOPSIS</span></span>
<span data-ttu-id="c5542-103">Pobiera informacje o ustawieniach magazynu ASR dotyczące magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c5542-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5542-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5542-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5542-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c5542-105">DESCRIPTION</span></span>
<span data-ttu-id="c5542-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrVaultContext** pobiera informacje o ustawieniach magazynu ASR związane z magazynem usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c5542-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="c5542-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5542-107">EXAMPLES</span></span>

### <span data-ttu-id="c5542-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c5542-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="c5542-109">Pobiera ustawienia magazynu ASR dla obecnie aktywnych (w ramach usługi odzyskiwania sesji programu PowerShell).</span><span class="sxs-lookup"><span data-stu-id="c5542-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="c5542-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5542-110">PARAMETERS</span></span>

### <span data-ttu-id="c5542-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5542-111">-DefaultProfile</span></span>
<span data-ttu-id="c5542-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5542-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5542-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5542-113">CommonParameters</span></span>
<span data-ttu-id="c5542-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5542-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5542-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5542-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5542-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5542-116">INPUTS</span></span>

### <span data-ttu-id="c5542-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c5542-117">None</span></span>

## <span data-ttu-id="c5542-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5542-118">OUTPUTS</span></span>

### <span data-ttu-id="c5542-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c5542-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="c5542-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5542-120">NOTES</span></span>

## <span data-ttu-id="c5542-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5542-121">RELATED LINKS</span></span>
