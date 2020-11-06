---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 496eeed8b4ed4b41ce2c67d47fc636711cd5cb84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544231"
---
# <span data-ttu-id="7558d-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7558d-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="7558d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7558d-102">SYNOPSIS</span></span>
<span data-ttu-id="7558d-103">Usuwa określony kontener ochrony z tkaniny.</span><span class="sxs-lookup"><span data-stu-id="7558d-103">Deletes the specified Protection Container from its Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7558d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7558d-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7558d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7558d-105">DESCRIPTION</span></span>
<span data-ttu-id="7558d-106">Polecenie cmdlet Remove-AzureRmRecoveryServicesAsrProtectionContainer powoduje usunięcie określonego kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7558d-106">The Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="7558d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7558d-107">EXAMPLES</span></span>

### <span data-ttu-id="7558d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7558d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="7558d-109">Rozpoczyna usuwanie określonego kontenera ochrony i zwraca zadanie ASR użyte do śledzenia operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="7558d-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="7558d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7558d-110">PARAMETERS</span></span>

### <span data-ttu-id="7558d-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7558d-111">-Confirm</span></span>
<span data-ttu-id="7558d-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7558d-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7558d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7558d-113">-DefaultProfile</span></span>
<span data-ttu-id="7558d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7558d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7558d-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7558d-115">-InputObject</span></span>
<span data-ttu-id="7558d-116">Określa kontener ochrony, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="7558d-116">Specifies the protection container to be removed .</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7558d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7558d-117">-WhatIf</span></span>
<span data-ttu-id="7558d-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7558d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7558d-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7558d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7558d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7558d-120">CommonParameters</span></span>
<span data-ttu-id="7558d-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7558d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7558d-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7558d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7558d-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7558d-123">INPUTS</span></span>

### <span data-ttu-id="7558d-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7558d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="7558d-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7558d-125">OUTPUTS</span></span>

### <span data-ttu-id="7558d-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7558d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7558d-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7558d-127">NOTES</span></span>

## <span data-ttu-id="7558d-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7558d-128">RELATED LINKS</span></span>
