---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: b1a68b3500f28e7a72c5d62996e0c62dc00107d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718114"
---
# <span data-ttu-id="fa4c0-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fa4c0-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="fa4c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="fa4c0-103">Odświeża (serwer odświeżania) informacje otrzymane od dostawcy usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fa4c0-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa4c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa4c0-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa4c0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fa4c0-105">DESCRIPTION</span></span>
<span data-ttu-id="fa4c0-106">Polecenie cmdlet **Update-AzureRmRecoveryServicesAsrServicesProvider** aktualizuje informacje otrzymane od dostawcy usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fa4c0-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="fa4c0-107">Za pomocą tego polecenia cmdlet można wyzwolić odświeżenie informacji otrzymanych od dostawcy usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="fa4c0-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="fa4c0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa4c0-108">EXAMPLES</span></span>

### <span data-ttu-id="fa4c0-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fa4c0-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="fa4c0-110">Rozpoczyna operację odświeżania informacji od określonego dostawcy usług ASR i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="fa4c0-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span> 

## <span data-ttu-id="fa4c0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa4c0-111">PARAMETERS</span></span>

### <span data-ttu-id="fa4c0-112">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fa4c0-112">-InputObject</span></span>
<span data-ttu-id="fa4c0-113">Obiekt wejściowy: określa obiekt dostawcy usług ASR odpowiadający dostawcy usług ASR, który identyfikuje serwer, dla którego informacje są aktualizowane (odświeżane).</span><span class="sxs-lookup"><span data-stu-id="fa4c0-113">Input Object: Specifies the ASR services provider object corresponding to the ASR services provider that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="fa4c0-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa4c0-114">-Confirm</span></span>
<span data-ttu-id="fa4c0-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa4c0-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa4c0-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa4c0-116">-WhatIf</span></span>
<span data-ttu-id="fa4c0-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa4c0-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa4c0-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fa4c0-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa4c0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa4c0-119">CommonParameters</span></span>
<span data-ttu-id="fa4c0-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa4c0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa4c0-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa4c0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa4c0-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa4c0-122">INPUTS</span></span>

### <span data-ttu-id="fa4c0-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fa4c0-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="fa4c0-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa4c0-124">OUTPUTS</span></span>

### <span data-ttu-id="fa4c0-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="fa4c0-125">System.Object</span></span>

## <span data-ttu-id="fa4c0-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa4c0-126">NOTES</span></span>

## <span data-ttu-id="fa4c0-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa4c0-127">RELATED LINKS</span></span>

[<span data-ttu-id="fa4c0-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fa4c0-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="fa4c0-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fa4c0-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
