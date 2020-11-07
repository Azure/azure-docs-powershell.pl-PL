---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 27c90687b212c0ed41dcb080df1be5686a876725
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718432"
---
# <span data-ttu-id="3ea6d-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3ea6d-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="3ea6d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ea6d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea6d-103">Usuwa mapowanie kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3ea6d-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ea6d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ea6d-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ea6d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3ea6d-105">DESCRIPTION</span></span>
<span data-ttu-id="3ea6d-106">Polecenie cmdlet **Remove-AzureRmSiteRecoveryProtectionContainerMapping** usuwa mapowanie kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3ea6d-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="3ea6d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ea6d-107">EXAMPLES</span></span>

## <span data-ttu-id="3ea6d-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ea6d-108">PARAMETERS</span></span>

### <span data-ttu-id="3ea6d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea6d-109">-DefaultProfile</span></span>
<span data-ttu-id="3ea6d-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea6d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ea6d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3ea6d-111">-Force</span></span>
<span data-ttu-id="3ea6d-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3ea6d-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea6d-113">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3ea6d-113">-ProtectionContainerMapping</span></span>
<span data-ttu-id="3ea6d-114">Określa obiekt mapowania kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3ea6d-114">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ea6d-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3ea6d-115">-Confirm</span></span>
<span data-ttu-id="3ea6d-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ea6d-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea6d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ea6d-117">-WhatIf</span></span>
<span data-ttu-id="3ea6d-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ea6d-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3ea6d-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3ea6d-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea6d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea6d-120">CommonParameters</span></span>
<span data-ttu-id="3ea6d-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ea6d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea6d-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ea6d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea6d-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ea6d-123">INPUTS</span></span>

### <span data-ttu-id="3ea6d-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3ea6d-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="3ea6d-125">Parametr "ProtectionContainerMapping" akceptuje wartość typu "ASRProtectionContainerMapping" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="3ea6d-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="3ea6d-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ea6d-126">OUTPUTS</span></span>

### <span data-ttu-id="3ea6d-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3ea6d-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3ea6d-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ea6d-128">NOTES</span></span>

## <span data-ttu-id="3ea6d-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ea6d-129">RELATED LINKS</span></span>

[<span data-ttu-id="3ea6d-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3ea6d-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="3ea6d-131">Nowe — AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3ea6d-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
