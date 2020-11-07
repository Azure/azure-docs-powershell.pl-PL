---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3DDC8DD8-889C-4C76-B32E-3D2C2AD0AC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverypolicyassociationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
ms.openlocfilehash: 140bec7738d107574db5d0d157cc3f8cfac46583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718423"
---
# <span data-ttu-id="8db5a-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span><span class="sxs-lookup"><span data-stu-id="8db5a-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span></span>

## <span data-ttu-id="8db5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8db5a-102">SYNOPSIS</span></span>
<span data-ttu-id="8db5a-103">Uruchamianie zadania skojarzenia zasad replikacji witryny.</span><span class="sxs-lookup"><span data-stu-id="8db5a-103">Starts a Site Recovery replication policy association job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8db5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8db5a-104">SYNTAX</span></span>

### <span data-ttu-id="8db5a-105">EnterpriseToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8db5a-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8db5a-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="8db5a-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8db5a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8db5a-107">DESCRIPTION</span></span>
<span data-ttu-id="8db5a-108">Polecenie cmdlet **Start-AzureRmSiteRecoveryPolicyAssociationJob** inicjuje zadanie skojarzenia w celu skojarzenia zasad replikacji z kontenerem ochrony za pomocą usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8db5a-108">The **Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="8db5a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8db5a-109">EXAMPLES</span></span>

## <span data-ttu-id="8db5a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8db5a-110">PARAMETERS</span></span>

### <span data-ttu-id="8db5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db5a-111">-DefaultProfile</span></span>
<span data-ttu-id="8db5a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8db5a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8db5a-113">-Policy</span><span class="sxs-lookup"><span data-stu-id="8db5a-113">-Policy</span></span>
<span data-ttu-id="8db5a-114">Określa obiekt zasady odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="8db5a-114">Specifies the Site Recovery policy object.</span></span>

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

### <span data-ttu-id="8db5a-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8db5a-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="8db5a-116">Określa podstawowy kontener ochrony, na którym należy zastosować ustawienia profilu ochrony.</span><span class="sxs-lookup"><span data-stu-id="8db5a-116">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="8db5a-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8db5a-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="8db5a-118">Określa kontener ochrony przed odzyskiwaniem, na którym należy zastosować ustawienia profilu ochrony.</span><span class="sxs-lookup"><span data-stu-id="8db5a-118">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="8db5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db5a-119">CommonParameters</span></span>
<span data-ttu-id="8db5a-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8db5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db5a-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8db5a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db5a-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8db5a-122">INPUTS</span></span>

### <span data-ttu-id="8db5a-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="8db5a-123">ASRPolicy</span></span>
<span data-ttu-id="8db5a-124">Parametr "Policy" przyjmuje wartość typu "ASRPolicy" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="8db5a-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="8db5a-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8db5a-125">OUTPUTS</span></span>

### <span data-ttu-id="8db5a-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8db5a-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8db5a-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8db5a-127">NOTES</span></span>

## <span data-ttu-id="8db5a-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8db5a-128">RELATED LINKS</span></span>

