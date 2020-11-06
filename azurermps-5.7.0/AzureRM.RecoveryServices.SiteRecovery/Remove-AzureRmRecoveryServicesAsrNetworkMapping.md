---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a51be31c510d7e428ced0c9ce5ab73a80ab28f75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526645"
---
# <span data-ttu-id="0996e-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0996e-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="0996e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0996e-102">SYNOPSIS</span></span>
<span data-ttu-id="0996e-103">Usuwa określone mapowanie sieci funkcji ASR z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0996e-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0996e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0996e-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0996e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0996e-105">DESCRIPTION</span></span>
<span data-ttu-id="0996e-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrNetworkMapping** umożliwia usunięcie określonego mapowania sieci funkcji ASR.</span><span class="sxs-lookup"><span data-stu-id="0996e-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="0996e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0996e-107">EXAMPLES</span></span>

### <span data-ttu-id="0996e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0996e-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="0996e-109">Rozpoczyna usuwanie określonego mapowania sieci funkcji ASR i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="0996e-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0996e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0996e-110">PARAMETERS</span></span>

### <span data-ttu-id="0996e-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0996e-111">-Confirm</span></span>
<span data-ttu-id="0996e-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0996e-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0996e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0996e-113">-DefaultProfile</span></span>
<span data-ttu-id="0996e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0996e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="0996e-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0996e-115">-InputObject</span></span>
<span data-ttu-id="0996e-116">Obiekt wejściowy do polecenia cmdlet: obiekt mapowania sieci ASR odpowiadający mapowaniu sieci funkcji ASR, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="0996e-116">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0996e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0996e-117">-WhatIf</span></span>
<span data-ttu-id="0996e-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0996e-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0996e-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0996e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0996e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0996e-120">CommonParameters</span></span>
<span data-ttu-id="0996e-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0996e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0996e-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0996e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0996e-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0996e-123">INPUTS</span></span>

### <span data-ttu-id="0996e-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0996e-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="0996e-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0996e-125">OUTPUTS</span></span>

### <span data-ttu-id="0996e-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0996e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0996e-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0996e-127">NOTES</span></span>

## <span data-ttu-id="0996e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0996e-128">RELATED LINKS</span></span>

[<span data-ttu-id="0996e-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0996e-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="0996e-130">Nowe — AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0996e-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
