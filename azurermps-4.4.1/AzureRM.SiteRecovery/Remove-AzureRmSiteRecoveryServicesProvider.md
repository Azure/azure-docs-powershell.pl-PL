---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: e7ee32974ef87b86d443d90b7dc628f9c9f1072f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542896"
---
# <span data-ttu-id="e5004-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e5004-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="e5004-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5004-102">SYNOPSIS</span></span>
<span data-ttu-id="e5004-103">Usuwa dostawcę usług Azure Site Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="e5004-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5004-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5004-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5004-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e5004-105">DESCRIPTION</span></span>
<span data-ttu-id="e5004-106">Polecenie cmdlet **Remove-AzureRmSiteRecoveryServicesProvider** Usuwa dostawcę usług Azure Site Recovery Services z magazynu.</span><span class="sxs-lookup"><span data-stu-id="e5004-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="e5004-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5004-107">EXAMPLES</span></span>

## <span data-ttu-id="e5004-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5004-108">PARAMETERS</span></span>

### <span data-ttu-id="e5004-109">-Force</span><span class="sxs-lookup"><span data-stu-id="e5004-109">-Force</span></span>
<span data-ttu-id="e5004-110">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e5004-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5004-111">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e5004-111">-ServicesProvider</span></span>
<span data-ttu-id="e5004-112">Określa obiekt dostawcy usług.</span><span class="sxs-lookup"><span data-stu-id="e5004-112">Specifies the Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5004-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5004-113">-Confirm</span></span>
<span data-ttu-id="e5004-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5004-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5004-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5004-115">-WhatIf</span></span>
<span data-ttu-id="e5004-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5004-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e5004-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e5004-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5004-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5004-118">-DefaultProfile</span></span>
<span data-ttu-id="e5004-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5004-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5004-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5004-120">CommonParameters</span></span>
<span data-ttu-id="e5004-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5004-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5004-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5004-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5004-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5004-123">INPUTS</span></span>

### <span data-ttu-id="e5004-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e5004-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="e5004-125">Parametr "ServicesProvider" akceptuje wartość typu "ASRRecoveryServicesProvider" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="e5004-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="e5004-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5004-126">OUTPUTS</span></span>

### <span data-ttu-id="e5004-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRJob, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e5004-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e5004-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5004-128">NOTES</span></span>

## <span data-ttu-id="e5004-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5004-129">RELATED LINKS</span></span>

[<span data-ttu-id="e5004-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e5004-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="e5004-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e5004-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
