---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 3d26a5285fbe96c0e77c56819567e21820cddf4f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717809"
---
# <span data-ttu-id="e0757-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e0757-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="e0757-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0757-102">SYNOPSIS</span></span>
<span data-ttu-id="e0757-103">Usuwa określone mapowanie kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e0757-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0757-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0757-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0757-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e0757-105">DESCRIPTION</span></span>
<span data-ttu-id="e0757-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** umożliwia usunięcie określonego mapowania kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e0757-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="e0757-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0757-107">EXAMPLES</span></span>

### <span data-ttu-id="e0757-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0757-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="e0757-109">Rozpoczyna usuwanie określonego mapowania kontenera ochrony i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="e0757-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e0757-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0757-110">PARAMETERS</span></span>

### <span data-ttu-id="e0757-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e0757-111">-Force</span></span>
<span data-ttu-id="e0757-112">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="e0757-112">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="e0757-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e0757-113">-InputObject</span></span>
<span data-ttu-id="e0757-114">Obiekt wejściowy do polecenia cmdlet: obiekt mapowania kontenera ochrony ASR odpowiadający kontenerowi ochrony, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e0757-114">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0757-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0757-115">-Confirm</span></span>
<span data-ttu-id="e0757-116">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="e0757-116">Specify if confirmation is required.</span></span> <span data-ttu-id="e0757-117">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0757-117">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="e0757-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0757-118">-WhatIf</span></span>
<span data-ttu-id="e0757-119">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0757-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="e0757-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0757-120">CommonParameters</span></span>
<span data-ttu-id="e0757-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0757-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0757-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0757-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0757-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0757-123">INPUTS</span></span>

### <span data-ttu-id="e0757-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e0757-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="e0757-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0757-125">OUTPUTS</span></span>

### <span data-ttu-id="e0757-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e0757-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e0757-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0757-127">NOTES</span></span>

## <span data-ttu-id="e0757-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0757-128">RELATED LINKS</span></span>

[<span data-ttu-id="e0757-129">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e0757-129">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="e0757-130">Nowe — AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e0757-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
