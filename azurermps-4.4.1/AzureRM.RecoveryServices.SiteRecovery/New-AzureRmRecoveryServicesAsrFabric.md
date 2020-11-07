---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 28c038a6dfd29f9daaeb942afa8fcb4c479cd0aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718996"
---
# <span data-ttu-id="3be48-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3be48-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="3be48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3be48-102">SYNOPSIS</span></span>
<span data-ttu-id="3be48-103">Tworzy sieć szkieletową odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="3be48-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3be48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3be48-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3be48-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3be48-105">DESCRIPTION</span></span>
<span data-ttu-id="3be48-106">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrFabric** umożliwia utworzenie sieci szkieletowej odzyskiwania witryny platformy Azure określonego typu.</span><span class="sxs-lookup"><span data-stu-id="3be48-106">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="3be48-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3be48-107">EXAMPLES</span></span>

### <span data-ttu-id="3be48-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3be48-108">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="3be48-109">Rozpoczyna tworzenie sieci szkieletowej z przekazaną nazwą i zwraca zadanie ASR używane do śledzenia operacji tworzenia sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="3be48-109">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="3be48-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3be48-110">PARAMETERS</span></span>

### <span data-ttu-id="3be48-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3be48-111">-Name</span></span>
<span data-ttu-id="3be48-112">Określa nazwę sieci szkieletowej odzyskiwania witryny usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="3be48-112">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3be48-113">-Type</span><span class="sxs-lookup"><span data-stu-id="3be48-113">-Type</span></span>
<span data-ttu-id="3be48-114">Określa typ sieci szkieletowej usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3be48-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3be48-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3be48-115">-Confirm</span></span>
<span data-ttu-id="3be48-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3be48-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3be48-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3be48-117">-WhatIf</span></span>
<span data-ttu-id="3be48-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3be48-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3be48-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3be48-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3be48-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be48-120">CommonParameters</span></span>
<span data-ttu-id="3be48-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3be48-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be48-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3be48-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be48-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3be48-123">INPUTS</span></span>

### <span data-ttu-id="3be48-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3be48-124">None</span></span>

## <span data-ttu-id="3be48-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3be48-125">OUTPUTS</span></span>

### <span data-ttu-id="3be48-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3be48-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3be48-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3be48-127">NOTES</span></span>

## <span data-ttu-id="3be48-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3be48-128">RELATED LINKS</span></span>

[<span data-ttu-id="3be48-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3be48-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="3be48-130">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3be48-130">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
