---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: f09ca4bb6c033b954542d6c734b27bf5f2236d87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524922"
---
# <span data-ttu-id="86064-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="86064-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="86064-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86064-102">SYNOPSIS</span></span>
<span data-ttu-id="86064-103">Usuwa zasady replikacji odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="86064-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86064-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86064-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86064-105">Opis</span><span class="sxs-lookup"><span data-stu-id="86064-105">DESCRIPTION</span></span>
<span data-ttu-id="86064-106">Polecenie cmdlet **Remove-AzureRMSiteRecoveryPolicy** usuwa zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="86064-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="86064-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86064-107">EXAMPLES</span></span>

## <span data-ttu-id="86064-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86064-108">PARAMETERS</span></span>

### <span data-ttu-id="86064-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86064-109">-DefaultProfile</span></span>
<span data-ttu-id="86064-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86064-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86064-111">-Policy</span><span class="sxs-lookup"><span data-stu-id="86064-111">-Policy</span></span>
<span data-ttu-id="86064-112">Określa obiekt zasady odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="86064-112">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86064-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86064-113">CommonParameters</span></span>
<span data-ttu-id="86064-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86064-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86064-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86064-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86064-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86064-116">INPUTS</span></span>

### <span data-ttu-id="86064-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="86064-117">ASRPolicy</span></span>
<span data-ttu-id="86064-118">Parametr "Policy" przyjmuje wartość typu "ASRPolicy" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="86064-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="86064-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86064-119">OUTPUTS</span></span>

## <span data-ttu-id="86064-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86064-120">NOTES</span></span>

## <span data-ttu-id="86064-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86064-121">RELATED LINKS</span></span>

[<span data-ttu-id="86064-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="86064-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="86064-123">Nowe — AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="86064-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
