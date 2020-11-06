---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 133668A0-0D11-4034-A743-4C0D3CE0FAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryvaultsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: b6016857054d2560602c7ea37a508317ff895d37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544095"
---
# <span data-ttu-id="85a94-101">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="85a94-101">Set-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="85a94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85a94-102">SYNOPSIS</span></span>
<span data-ttu-id="85a94-103">Ustawia kontekst magazynu odzyskiwania witryny dla kolejnych operacji.</span><span class="sxs-lookup"><span data-stu-id="85a94-103">Sets the Site Recovery vault context for further operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85a94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85a94-104">SYNTAX</span></span>

### <span data-ttu-id="85a94-105">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="85a94-105">AzureSiteRecoveryVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ASRVault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85a94-106">AzureRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="85a94-106">AzureRecoveryServicesVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ARSVault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85a94-107">Opis</span><span class="sxs-lookup"><span data-stu-id="85a94-107">DESCRIPTION</span></span>
<span data-ttu-id="85a94-108">Polecenie cmdlet **Set-AzureRmSiteRecoveryVaultSettings** ustawia kontekst magazynu usługi Azure Site Recovery dla kolejnych operacji.</span><span class="sxs-lookup"><span data-stu-id="85a94-108">The **Set-AzureRmSiteRecoveryVaultSettings** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>
<span data-ttu-id="85a94-109">Nie dotyczy to magazynów usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="85a94-109">This does not apply to recovery services vaults.</span></span>

## <span data-ttu-id="85a94-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85a94-110">EXAMPLES</span></span>

## <span data-ttu-id="85a94-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85a94-111">PARAMETERS</span></span>

### <span data-ttu-id="85a94-112">-ARSVault</span><span class="sxs-lookup"><span data-stu-id="85a94-112">-ARSVault</span></span>
<span data-ttu-id="85a94-113">Określa obiekt **ARSVault** .</span><span class="sxs-lookup"><span data-stu-id="85a94-113">Specifies an **ARSVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85a94-114">-ASRVault</span><span class="sxs-lookup"><span data-stu-id="85a94-114">-ASRVault</span></span>
<span data-ttu-id="85a94-115">Określa obiekt **ASRVault** .</span><span class="sxs-lookup"><span data-stu-id="85a94-115">Specifies an **ASRVault** object.</span></span>

```yaml
Type: ASRVault
Parameter Sets: AzureSiteRecoveryVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85a94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a94-116">-DefaultProfile</span></span>
<span data-ttu-id="85a94-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85a94-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85a94-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a94-118">CommonParameters</span></span>
<span data-ttu-id="85a94-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85a94-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a94-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85a94-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a94-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85a94-121">INPUTS</span></span>

### <span data-ttu-id="85a94-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="85a94-122">ARSVault</span></span>
<span data-ttu-id="85a94-123">Parametr "ARSVault" akceptuje wartość typu "ARSVault" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="85a94-123">Parameter 'ARSVault' accepts value of type 'ARSVault' from the pipeline</span></span>

### <span data-ttu-id="85a94-124">ASRVault</span><span class="sxs-lookup"><span data-stu-id="85a94-124">ASRVault</span></span>
<span data-ttu-id="85a94-125">Parametr "ASRVault" akceptuje wartość typu "ASRVault" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="85a94-125">Parameter 'ASRVault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="85a94-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85a94-126">OUTPUTS</span></span>

### <span data-ttu-id="85a94-127">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="85a94-127">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="85a94-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85a94-128">NOTES</span></span>

## <span data-ttu-id="85a94-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85a94-129">RELATED LINKS</span></span>

[<span data-ttu-id="85a94-130">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="85a94-130">Get-AzureRmSiteRecoveryVaultSettings</span></span>](./Get-AzureRmSiteRecoveryVaultSettings.md)
