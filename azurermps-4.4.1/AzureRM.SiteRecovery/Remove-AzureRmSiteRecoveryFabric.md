---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 3d4530090bc1386a34056b315c79a826be5d771f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545992"
---
# <span data-ttu-id="28d3b-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="28d3b-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="28d3b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="28d3b-103">Usuwa sieć szkieletową odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="28d3b-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28d3b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28d3b-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28d3b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="28d3b-105">DESCRIPTION</span></span>
<span data-ttu-id="28d3b-106">Polecenie cmdlet **Remove-AzureRmSiteRecoveryFabric** usuwa sieć szkieletową odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="28d3b-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="28d3b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28d3b-107">EXAMPLES</span></span>

## <span data-ttu-id="28d3b-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28d3b-108">PARAMETERS</span></span>

### <span data-ttu-id="28d3b-109">-Fabric</span><span class="sxs-lookup"><span data-stu-id="28d3b-109">-Fabric</span></span>
<span data-ttu-id="28d3b-110">Określa obiekt sieci szkieletowej usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="28d3b-110">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28d3b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="28d3b-111">-Force</span></span>
<span data-ttu-id="28d3b-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="28d3b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="28d3b-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28d3b-113">-Confirm</span></span>
<span data-ttu-id="28d3b-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28d3b-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28d3b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28d3b-115">-WhatIf</span></span>
<span data-ttu-id="28d3b-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28d3b-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="28d3b-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="28d3b-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28d3b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28d3b-118">-DefaultProfile</span></span>
<span data-ttu-id="28d3b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28d3b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28d3b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d3b-120">CommonParameters</span></span>
<span data-ttu-id="28d3b-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28d3b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d3b-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28d3b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d3b-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28d3b-123">INPUTS</span></span>

### <span data-ttu-id="28d3b-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="28d3b-124">ASRFabric</span></span>
<span data-ttu-id="28d3b-125">Parametr "Fabric" akceptuje wartość typu "ASRFabric" z procesu</span><span class="sxs-lookup"><span data-stu-id="28d3b-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="28d3b-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28d3b-126">OUTPUTS</span></span>

### <span data-ttu-id="28d3b-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="28d3b-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="28d3b-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28d3b-128">NOTES</span></span>

## <span data-ttu-id="28d3b-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28d3b-129">RELATED LINKS</span></span>

[<span data-ttu-id="28d3b-130">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="28d3b-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="28d3b-131">Nowe — AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="28d3b-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)
