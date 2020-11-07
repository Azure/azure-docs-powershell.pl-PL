---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 3b01e089271cc131af5a4258c46836a87104ef62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717153"
---
# <span data-ttu-id="45df8-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="45df8-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="45df8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45df8-102">SYNOPSIS</span></span>
<span data-ttu-id="45df8-103">Usuwa zasady replikacji odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="45df8-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45df8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45df8-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45df8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45df8-105">DESCRIPTION</span></span>
<span data-ttu-id="45df8-106">Polecenie cmdlet **Remove-AzureRMSiteRecoveryPolicy** usuwa zasady replikacji odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="45df8-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="45df8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45df8-107">EXAMPLES</span></span>

## <span data-ttu-id="45df8-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45df8-108">PARAMETERS</span></span>

### <span data-ttu-id="45df8-109">-Policy</span><span class="sxs-lookup"><span data-stu-id="45df8-109">-Policy</span></span>
<span data-ttu-id="45df8-110">Określa obiekt zasady odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="45df8-110">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45df8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45df8-111">-DefaultProfile</span></span>
<span data-ttu-id="45df8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45df8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45df8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45df8-113">CommonParameters</span></span>
<span data-ttu-id="45df8-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45df8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45df8-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45df8-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45df8-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45df8-116">INPUTS</span></span>

### <span data-ttu-id="45df8-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="45df8-117">ASRPolicy</span></span>
<span data-ttu-id="45df8-118">Parametr "Policy" przyjmuje wartość typu "ASRPolicy" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="45df8-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="45df8-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45df8-119">OUTPUTS</span></span>

## <span data-ttu-id="45df8-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45df8-120">NOTES</span></span>

## <span data-ttu-id="45df8-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45df8-121">RELATED LINKS</span></span>

[<span data-ttu-id="45df8-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="45df8-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="45df8-123">Nowe — AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="45df8-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
