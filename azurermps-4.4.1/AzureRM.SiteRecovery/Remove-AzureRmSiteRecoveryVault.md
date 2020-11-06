---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 63E9894A-3AC5-4397-9B21-D0A72EBA5C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: e5d85c6cdc30ff00d2a35bba6d1a79119cbaddd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549843"
---
# <span data-ttu-id="6a45c-101">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="6a45c-101">Remove-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="6a45c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a45c-102">SYNOPSIS</span></span>
<span data-ttu-id="6a45c-103">Usuwa magazyn odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="6a45c-103">Removes a Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a45c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a45c-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryVault -Vault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a45c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a45c-105">DESCRIPTION</span></span>
<span data-ttu-id="6a45c-106">Polecenie cmdlet **Remove-AzureRmSiteRecoveryVault** usuwa magazyn odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6a45c-106">The **Remove-AzureRmSiteRecoveryVault** cmdlet deletes an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="6a45c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a45c-107">EXAMPLES</span></span>

## <span data-ttu-id="6a45c-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a45c-108">PARAMETERS</span></span>

### <span data-ttu-id="6a45c-109">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="6a45c-109">-Vault</span></span>
<span data-ttu-id="6a45c-110">Określa obiekt magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="6a45c-110">Specifies the Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a45c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a45c-111">-DefaultProfile</span></span>
<span data-ttu-id="6a45c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a45c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a45c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a45c-113">CommonParameters</span></span>
<span data-ttu-id="6a45c-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a45c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a45c-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a45c-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a45c-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a45c-116">INPUTS</span></span>

### <span data-ttu-id="6a45c-117">ASRVault</span><span class="sxs-lookup"><span data-stu-id="6a45c-117">ASRVault</span></span>
<span data-ttu-id="6a45c-118">Parametr "magazyn" akceptuje wartość typu "ASRVault" z potoku.</span><span class="sxs-lookup"><span data-stu-id="6a45c-118">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="6a45c-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a45c-119">OUTPUTS</span></span>

## <span data-ttu-id="6a45c-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a45c-120">NOTES</span></span>

## <span data-ttu-id="6a45c-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a45c-121">RELATED LINKS</span></span>

[<span data-ttu-id="6a45c-122">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="6a45c-122">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="6a45c-123">Nowe — AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="6a45c-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)
