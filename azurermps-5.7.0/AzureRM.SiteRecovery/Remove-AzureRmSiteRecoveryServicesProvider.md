---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 88b6b83f24edb06871fd87f61fec1732893b0f41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524917"
---
# <span data-ttu-id="3dc11-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3dc11-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="3dc11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3dc11-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc11-103">Usuwa dostawcę usług Azure Site Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="3dc11-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dc11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3dc11-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dc11-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3dc11-105">DESCRIPTION</span></span>
<span data-ttu-id="3dc11-106">Polecenie cmdlet **Remove-AzureRmSiteRecoveryServicesProvider** Usuwa dostawcę usług Azure Site Recovery Services z magazynu.</span><span class="sxs-lookup"><span data-stu-id="3dc11-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="3dc11-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3dc11-107">EXAMPLES</span></span>

## <span data-ttu-id="3dc11-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3dc11-108">PARAMETERS</span></span>

### <span data-ttu-id="3dc11-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc11-109">-DefaultProfile</span></span>
<span data-ttu-id="3dc11-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc11-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dc11-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3dc11-111">-Force</span></span>
<span data-ttu-id="3dc11-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3dc11-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3dc11-113">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3dc11-113">-ServicesProvider</span></span>
<span data-ttu-id="3dc11-114">Określa obiekt dostawcy usług.</span><span class="sxs-lookup"><span data-stu-id="3dc11-114">Specifies the Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dc11-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3dc11-115">-Confirm</span></span>
<span data-ttu-id="3dc11-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dc11-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dc11-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc11-117">-WhatIf</span></span>
<span data-ttu-id="3dc11-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dc11-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3dc11-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3dc11-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dc11-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc11-120">CommonParameters</span></span>
<span data-ttu-id="3dc11-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dc11-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc11-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dc11-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc11-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dc11-123">INPUTS</span></span>

### <span data-ttu-id="3dc11-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3dc11-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="3dc11-125">Parametr "ServicesProvider" akceptuje wartość typu "ASRRecoveryServicesProvider" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="3dc11-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="3dc11-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3dc11-126">OUTPUTS</span></span>

### <span data-ttu-id="3dc11-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRJob, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3dc11-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3dc11-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3dc11-128">NOTES</span></span>

## <span data-ttu-id="3dc11-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3dc11-129">RELATED LINKS</span></span>

[<span data-ttu-id="3dc11-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3dc11-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="3dc11-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3dc11-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
