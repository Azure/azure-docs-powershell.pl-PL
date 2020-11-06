---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 133668A0-0D11-4034-A743-4C0D3CE0FAF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: 9c252649ea668e666c98719ab2045e99e729a836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549828"
---
# <span data-ttu-id="258b1-101">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="258b1-101">Set-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="258b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="258b1-102">SYNOPSIS</span></span>
<span data-ttu-id="258b1-103">Ustawia kontekst magazynu odzyskiwania witryny dla kolejnych operacji.</span><span class="sxs-lookup"><span data-stu-id="258b1-103">Sets the Site Recovery vault context for further operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="258b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="258b1-104">SYNTAX</span></span>

### <span data-ttu-id="258b1-105">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="258b1-105">AzureSiteRecoveryVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ASRVault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="258b1-106">AzureRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="258b1-106">AzureRecoveryServicesVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ARSVault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="258b1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="258b1-107">DESCRIPTION</span></span>
<span data-ttu-id="258b1-108">Polecenie cmdlet **Set-AzureRmSiteRecoveryVaultSettings** ustawia kontekst magazynu usługi Azure Site Recovery dla kolejnych operacji.</span><span class="sxs-lookup"><span data-stu-id="258b1-108">The **Set-AzureRmSiteRecoveryVaultSettings** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>
<span data-ttu-id="258b1-109">Nie dotyczy to magazynów usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="258b1-109">This does not apply to recovery services vaults.</span></span>

## <span data-ttu-id="258b1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="258b1-110">EXAMPLES</span></span>

## <span data-ttu-id="258b1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="258b1-111">PARAMETERS</span></span>

### <span data-ttu-id="258b1-112">-ARSVault</span><span class="sxs-lookup"><span data-stu-id="258b1-112">-ARSVault</span></span>
<span data-ttu-id="258b1-113">Określa obiekt **ARSVault** .</span><span class="sxs-lookup"><span data-stu-id="258b1-113">Specifies an **ARSVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="258b1-114">-ASRVault</span><span class="sxs-lookup"><span data-stu-id="258b1-114">-ASRVault</span></span>
<span data-ttu-id="258b1-115">Określa obiekt **ASRVault** .</span><span class="sxs-lookup"><span data-stu-id="258b1-115">Specifies an **ASRVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: AzureSiteRecoveryVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="258b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="258b1-116">-DefaultProfile</span></span>
<span data-ttu-id="258b1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="258b1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="258b1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="258b1-118">CommonParameters</span></span>
<span data-ttu-id="258b1-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="258b1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="258b1-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="258b1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="258b1-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="258b1-121">INPUTS</span></span>

### <span data-ttu-id="258b1-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="258b1-122">ARSVault</span></span>
<span data-ttu-id="258b1-123">Parametr "ARSVault" akceptuje wartość typu "ARSVault" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="258b1-123">Parameter 'ARSVault' accepts value of type 'ARSVault' from the pipeline</span></span>

### <span data-ttu-id="258b1-124">ASRVault</span><span class="sxs-lookup"><span data-stu-id="258b1-124">ASRVault</span></span>
<span data-ttu-id="258b1-125">Parametr "ASRVault" akceptuje wartość typu "ASRVault" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="258b1-125">Parameter 'ASRVault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="258b1-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="258b1-126">OUTPUTS</span></span>

### <span data-ttu-id="258b1-127">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="258b1-127">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="258b1-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="258b1-128">NOTES</span></span>

## <span data-ttu-id="258b1-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="258b1-129">RELATED LINKS</span></span>

[<span data-ttu-id="258b1-130">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="258b1-130">Get-AzureRmSiteRecoveryVaultSettings</span></span>](./Get-AzureRmSiteRecoveryVaultSettings.md)
