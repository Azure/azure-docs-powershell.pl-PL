---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4BF1E20A-46EA-48E2-8C7A-F121AE6815AF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 1b01fef6563fef97f78913f916a6481acd6f6ed3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718978"
---
# <span data-ttu-id="51132-101">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="51132-101">New-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="51132-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51132-102">SYNOPSIS</span></span>
<span data-ttu-id="51132-103">Tworzy mapowanie między sieciami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="51132-103">Creates a mapping between virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51132-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51132-104">SYNTAX</span></span>

### <span data-ttu-id="51132-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="51132-105">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51132-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="51132-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork> -AzureVMNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51132-107">Opis</span><span class="sxs-lookup"><span data-stu-id="51132-107">DESCRIPTION</span></span>
<span data-ttu-id="51132-108">Polecenie cmdlet **New-AzureRMSiteRecoveryNetworkMapping** tworzy mapowanie między dwiema sieciami wirtualnymi i zwraca zadanie odzyskiwania witryny Azure, aby je śledzić.</span><span class="sxs-lookup"><span data-stu-id="51132-108">The **New-AzureRMSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="51132-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51132-109">EXAMPLES</span></span>

## <span data-ttu-id="51132-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51132-110">PARAMETERS</span></span>

### <span data-ttu-id="51132-111">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="51132-111">-AzureVMNetworkId</span></span>
<span data-ttu-id="51132-112">Określa identyfikator sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="51132-112">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51132-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51132-113">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51132-114">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="51132-114">-PrimaryNetwork</span></span>
<span data-ttu-id="51132-115">Określa podstawowy obiekt sieciowy.</span><span class="sxs-lookup"><span data-stu-id="51132-115">Specifies the primary network object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51132-116">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="51132-116">-RecoveryNetwork</span></span>
<span data-ttu-id="51132-117">Określa obiekt sieciowy odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="51132-117">Specifies the recovery network object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51132-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51132-118">-DefaultProfile</span></span>
<span data-ttu-id="51132-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51132-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51132-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51132-120">CommonParameters</span></span>
<span data-ttu-id="51132-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51132-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51132-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51132-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51132-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51132-123">INPUTS</span></span>

### <span data-ttu-id="51132-124">ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="51132-124">ASRNetwork</span></span>
<span data-ttu-id="51132-125">Parametr "PrimaryNetwork" akceptuje wartość typu "ASRNetwork" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="51132-125">Parameter 'PrimaryNetwork' accepts value of type 'ASRNetwork' from the pipeline</span></span>

## <span data-ttu-id="51132-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51132-126">OUTPUTS</span></span>

### <span data-ttu-id="51132-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="51132-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="51132-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51132-128">NOTES</span></span>

## <span data-ttu-id="51132-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51132-129">RELATED LINKS</span></span>

[<span data-ttu-id="51132-130">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="51132-130">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="51132-131">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="51132-131">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
