---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: 7dc64ea2bdbfb5dcbc648143dd094313eb765782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542875"
---
# <span data-ttu-id="ff2b7-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="ff2b7-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="ff2b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff2b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ff2b7-103">Rozpoczyna zadanie tworzenia skojarzenia w zasadach replikacji skojarzonych z kontenerem ochrona przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="ff2b7-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff2b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff2b7-104">SYNTAX</span></span>

### <span data-ttu-id="ff2b7-105">EnterpriseToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ff2b7-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff2b7-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ff2b7-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff2b7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ff2b7-107">DESCRIPTION</span></span>
<span data-ttu-id="ff2b7-108">Polecenie cmdlet **Starting-AzureRmSiteRecoveryPolicyDissociationJob** inicjuje zadanie skojarzenia zabezpieczeń w zasadach replikacji skojarzonych z kontenerem Ochrona usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ff2b7-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="ff2b7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff2b7-109">EXAMPLES</span></span>

## <span data-ttu-id="ff2b7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff2b7-110">PARAMETERS</span></span>

### <span data-ttu-id="ff2b7-111">-Policy</span><span class="sxs-lookup"><span data-stu-id="ff2b7-111">-Policy</span></span>
<span data-ttu-id="ff2b7-112">Określa obiekt zasad usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ff2b7-112">Specifies an Azure Site Recovery policy object.</span></span>

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

### <span data-ttu-id="ff2b7-113">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ff2b7-113">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="ff2b7-114">Określa podstawowy kontener ochrony.</span><span class="sxs-lookup"><span data-stu-id="ff2b7-114">Specifies a primary protection container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff2b7-115">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ff2b7-115">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="ff2b7-116">Określa kontener ochrona przed odzyskiwaniem.</span><span class="sxs-lookup"><span data-stu-id="ff2b7-116">Specifies a recovery protection container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff2b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff2b7-117">-DefaultProfile</span></span>
<span data-ttu-id="ff2b7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff2b7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff2b7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff2b7-119">CommonParameters</span></span>
<span data-ttu-id="ff2b7-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff2b7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff2b7-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff2b7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff2b7-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff2b7-122">INPUTS</span></span>

### <span data-ttu-id="ff2b7-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="ff2b7-123">ASRPolicy</span></span>
<span data-ttu-id="ff2b7-124">Parametr "Policy" przyjmuje wartość typu "ASRPolicy" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ff2b7-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="ff2b7-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff2b7-125">OUTPUTS</span></span>

### <span data-ttu-id="ff2b7-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ff2b7-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ff2b7-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff2b7-127">NOTES</span></span>

## <span data-ttu-id="ff2b7-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff2b7-128">RELATED LINKS</span></span>

