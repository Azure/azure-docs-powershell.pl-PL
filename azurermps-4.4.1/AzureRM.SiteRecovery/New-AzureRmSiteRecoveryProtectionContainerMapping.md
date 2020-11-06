---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 44addca6ee4f658f4cc6f8081e0f7a0c39ba4a58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549844"
---
# <span data-ttu-id="4a77e-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4a77e-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="4a77e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a77e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a77e-103">Tworzy mapowanie kontenera ochrony witryny platformy Azure, kojarząc zasady z kontenerem ochrony.</span><span class="sxs-lookup"><span data-stu-id="4a77e-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a77e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a77e-104">SYNTAX</span></span>

### <span data-ttu-id="4a77e-105">EnterpriseToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4a77e-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a77e-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="4a77e-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a77e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4a77e-107">DESCRIPTION</span></span>
<span data-ttu-id="4a77e-108">Polecenie cmdlet **New-AzureRmSiteRecoveryProtectionContainerMapping** tworzy mapowanie kontenera ochrony usługi Azure Site Recovery, kojarząc zasady z kontenerem ochrony.</span><span class="sxs-lookup"><span data-stu-id="4a77e-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="4a77e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a77e-109">EXAMPLES</span></span>

## <span data-ttu-id="4a77e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a77e-110">PARAMETERS</span></span>

### <span data-ttu-id="4a77e-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4a77e-111">-Name</span></span>
<span data-ttu-id="4a77e-112">Określa nazwę mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="4a77e-112">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a77e-113">-Policy</span><span class="sxs-lookup"><span data-stu-id="4a77e-113">-Policy</span></span>
<span data-ttu-id="4a77e-114">Określa obiekt zasad usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4a77e-114">Specifies the Azure Site Recovery Policy object.</span></span>

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

### <span data-ttu-id="4a77e-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4a77e-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="4a77e-116">Określa obiekt głównego kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="4a77e-116">Specifies the primary Protection Container object.</span></span>

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

### <span data-ttu-id="4a77e-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4a77e-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="4a77e-118">Określa obiekt kontenera ochrony przed odzyskiwaniem.</span><span class="sxs-lookup"><span data-stu-id="4a77e-118">Specifies the Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="4a77e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a77e-119">-DefaultProfile</span></span>
<span data-ttu-id="4a77e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a77e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a77e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a77e-121">CommonParameters</span></span>
<span data-ttu-id="4a77e-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a77e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a77e-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a77e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a77e-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a77e-124">INPUTS</span></span>

### <span data-ttu-id="4a77e-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="4a77e-125">ASRPolicy</span></span>
<span data-ttu-id="4a77e-126">Parametr "Policy" przyjmuje wartość typu "ASRPolicy" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="4a77e-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="4a77e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a77e-127">OUTPUTS</span></span>

### <span data-ttu-id="4a77e-128">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4a77e-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4a77e-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a77e-129">NOTES</span></span>

## <span data-ttu-id="4a77e-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a77e-130">RELATED LINKS</span></span>

[<span data-ttu-id="4a77e-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4a77e-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="4a77e-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4a77e-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
