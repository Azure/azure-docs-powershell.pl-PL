---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 5220271538903206876dd8d5c476824e1ac10874
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553781"
---
# <span data-ttu-id="699b2-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="699b2-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="699b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="699b2-102">SYNOPSIS</span></span>
<span data-ttu-id="699b2-103">Usuwa/wyrejestrowuje określonego dostawcę usług odzyskiwania usługi Azure Site Recovery z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="699b2-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="699b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="699b2-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="699b2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="699b2-105">DESCRIPTION</span></span>
<span data-ttu-id="699b2-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrServicesProvider** usuwa określonego dostawcę usług odzyskiwania usługi Azure Site Recovery z magazynu.</span><span class="sxs-lookup"><span data-stu-id="699b2-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="699b2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="699b2-107">EXAMPLES</span></span>

### <span data-ttu-id="699b2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="699b2-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="699b2-109">Rozpoczyna usuwanie/Wyrejestrowanie określonego dostawcy usług Azure Site Recovery Services i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="699b2-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="699b2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="699b2-110">PARAMETERS</span></span>

### <span data-ttu-id="699b2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="699b2-111">-Force</span></span>
<span data-ttu-id="699b2-112">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="699b2-112">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="699b2-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="699b2-113">-InputObject</span></span>
<span data-ttu-id="699b2-114">Obiekt wejściowy do polecenia cmdlet: obiekt dostawcy usług odzyskiwania ASR odpowiadający dostawcy usług odzyskiwania ASR, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="699b2-114">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="699b2-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="699b2-115">-Confirm</span></span>
<span data-ttu-id="699b2-116">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="699b2-116">Specify if confirmation is required.</span></span> <span data-ttu-id="699b2-117">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="699b2-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="699b2-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="699b2-118">-WhatIf</span></span>
<span data-ttu-id="699b2-119">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="699b2-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="699b2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699b2-120">CommonParameters</span></span>
<span data-ttu-id="699b2-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="699b2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699b2-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="699b2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699b2-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="699b2-123">INPUTS</span></span>

### <span data-ttu-id="699b2-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="699b2-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="699b2-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="699b2-125">OUTPUTS</span></span>

### <span data-ttu-id="699b2-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="699b2-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="699b2-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="699b2-127">NOTES</span></span>

## <span data-ttu-id="699b2-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="699b2-128">RELATED LINKS</span></span>

[<span data-ttu-id="699b2-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="699b2-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="699b2-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="699b2-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
