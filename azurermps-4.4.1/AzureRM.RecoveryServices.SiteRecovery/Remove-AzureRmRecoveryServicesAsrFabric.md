---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 3f380110359668af5c1b506e1736d3ecc9f39b3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543068"
---
# <span data-ttu-id="c98d7-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="c98d7-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="c98d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c98d7-102">SYNOPSIS</span></span>
<span data-ttu-id="c98d7-103">Usuwa określoną sieć szkieletową odzyskiwania witryny platformy Azure z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c98d7-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c98d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c98d7-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c98d7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c98d7-105">DESCRIPTION</span></span>
<span data-ttu-id="c98d7-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrFabric** usuwa określoną sieć szkieletową odzyskiwania witryny platformy Azure z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c98d7-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="c98d7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c98d7-107">EXAMPLES</span></span>

### <span data-ttu-id="c98d7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c98d7-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="c98d7-109">Rozpoczyna usuwanie określonej sieci szkieletowej i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="c98d7-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c98d7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c98d7-110">PARAMETERS</span></span>

### <span data-ttu-id="c98d7-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c98d7-111">-Force</span></span>
<span data-ttu-id="c98d7-112">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="c98d7-112">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="c98d7-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c98d7-113">-InputObject</span></span>
<span data-ttu-id="c98d7-114">Obiekt wejściowy do polecenia cmdlet: obiekt sieci szkieletowej ASR odpowiadający sieci szkieletowej, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="c98d7-114">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c98d7-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c98d7-115">-Confirm</span></span>
<span data-ttu-id="c98d7-116">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="c98d7-116">Specify if confirmation is required.</span></span> <span data-ttu-id="c98d7-117">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c98d7-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="c98d7-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c98d7-118">-WhatIf</span></span>
<span data-ttu-id="c98d7-119">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c98d7-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="c98d7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98d7-120">CommonParameters</span></span>
<span data-ttu-id="c98d7-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c98d7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98d7-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c98d7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98d7-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c98d7-123">INPUTS</span></span>

### <span data-ttu-id="c98d7-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c98d7-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c98d7-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c98d7-125">OUTPUTS</span></span>

### <span data-ttu-id="c98d7-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c98d7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c98d7-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c98d7-127">NOTES</span></span>

## <span data-ttu-id="c98d7-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c98d7-128">RELATED LINKS</span></span>

[<span data-ttu-id="c98d7-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="c98d7-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="c98d7-130">Nowe — AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="c98d7-130">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
