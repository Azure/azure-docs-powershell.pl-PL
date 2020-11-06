---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverypolicydissociationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: eb12462b85c4a12416f41f899ebc9b2c46cca465
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550535"
---
# <span data-ttu-id="734fd-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="734fd-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="734fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="734fd-102">SYNOPSIS</span></span>
<span data-ttu-id="734fd-103">Rozpoczyna zadanie tworzenia skojarzenia w zasadach replikacji skojarzonych z kontenerem ochrona przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="734fd-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="734fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="734fd-104">SYNTAX</span></span>

### <span data-ttu-id="734fd-105">EnterpriseToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="734fd-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="734fd-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="734fd-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="734fd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="734fd-107">DESCRIPTION</span></span>
<span data-ttu-id="734fd-108">Polecenie cmdlet **Starting-AzureRmSiteRecoveryPolicyDissociationJob** inicjuje zadanie skojarzenia zabezpieczeń w zasadach replikacji skojarzonych z kontenerem Ochrona usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="734fd-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="734fd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="734fd-109">EXAMPLES</span></span>

## <span data-ttu-id="734fd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="734fd-110">PARAMETERS</span></span>

### <span data-ttu-id="734fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="734fd-111">-DefaultProfile</span></span>
<span data-ttu-id="734fd-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="734fd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="734fd-113">-Policy</span><span class="sxs-lookup"><span data-stu-id="734fd-113">-Policy</span></span>
<span data-ttu-id="734fd-114">Określa obiekt zasad usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="734fd-114">Specifies an Azure Site Recovery policy object.</span></span>

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

### <span data-ttu-id="734fd-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="734fd-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="734fd-116">Określa podstawowy kontener ochrony.</span><span class="sxs-lookup"><span data-stu-id="734fd-116">Specifies a primary protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="734fd-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="734fd-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="734fd-118">Określa kontener ochrona przed odzyskiwaniem.</span><span class="sxs-lookup"><span data-stu-id="734fd-118">Specifies a recovery protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="734fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734fd-119">CommonParameters</span></span>
<span data-ttu-id="734fd-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="734fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="734fd-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="734fd-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734fd-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="734fd-122">INPUTS</span></span>

### <span data-ttu-id="734fd-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="734fd-123">ASRPolicy</span></span>
<span data-ttu-id="734fd-124">Parametr "Policy" przyjmuje wartość typu "ASRPolicy" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="734fd-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="734fd-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="734fd-125">OUTPUTS</span></span>

### <span data-ttu-id="734fd-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="734fd-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="734fd-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="734fd-127">NOTES</span></span>

## <span data-ttu-id="734fd-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="734fd-128">RELATED LINKS</span></span>

