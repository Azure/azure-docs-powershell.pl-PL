---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4BF1E20A-46EA-48E2-8C7A-F121AE6815AF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 36f5c6e535cc67029fac7c951cbc6dbbe3c73091
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718439"
---
# <span data-ttu-id="ecb56-101">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ecb56-101">New-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="ecb56-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ecb56-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb56-103">Tworzy mapowanie między sieciami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="ecb56-103">Creates a mapping between virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecb56-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ecb56-104">SYNTAX</span></span>

### <span data-ttu-id="ecb56-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ecb56-105">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb56-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="ecb56-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork> -AzureVMNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecb56-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ecb56-107">DESCRIPTION</span></span>
<span data-ttu-id="ecb56-108">Polecenie cmdlet **New-AzureRMSiteRecoveryNetworkMapping** tworzy mapowanie między dwiema sieciami wirtualnymi i zwraca zadanie odzyskiwania witryny Azure, aby je śledzić.</span><span class="sxs-lookup"><span data-stu-id="ecb56-108">The **New-AzureRMSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="ecb56-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ecb56-109">EXAMPLES</span></span>

## <span data-ttu-id="ecb56-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ecb56-110">PARAMETERS</span></span>

### <span data-ttu-id="ecb56-111">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="ecb56-111">-AzureVMNetworkId</span></span>
<span data-ttu-id="ecb56-112">Określa identyfikator sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ecb56-112">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb56-113">-DefaultProfile</span></span>
<span data-ttu-id="ecb56-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ecb56-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecb56-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ecb56-115">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb56-116">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="ecb56-116">-PrimaryNetwork</span></span>
<span data-ttu-id="ecb56-117">Określa podstawowy obiekt sieciowy.</span><span class="sxs-lookup"><span data-stu-id="ecb56-117">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb56-118">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="ecb56-118">-RecoveryNetwork</span></span>
<span data-ttu-id="ecb56-119">Określa obiekt sieciowy odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="ecb56-119">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb56-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb56-120">CommonParameters</span></span>
<span data-ttu-id="ecb56-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecb56-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb56-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecb56-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb56-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecb56-123">INPUTS</span></span>

### <span data-ttu-id="ecb56-124">ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="ecb56-124">ASRNetwork</span></span>
<span data-ttu-id="ecb56-125">Parametr "PrimaryNetwork" akceptuje wartość typu "ASRNetwork" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ecb56-125">Parameter 'PrimaryNetwork' accepts value of type 'ASRNetwork' from the pipeline</span></span>

## <span data-ttu-id="ecb56-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ecb56-126">OUTPUTS</span></span>

### <span data-ttu-id="ecb56-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ecb56-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ecb56-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ecb56-128">NOTES</span></span>

## <span data-ttu-id="ecb56-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ecb56-129">RELATED LINKS</span></span>

[<span data-ttu-id="ecb56-130">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ecb56-130">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="ecb56-131">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ecb56-131">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
