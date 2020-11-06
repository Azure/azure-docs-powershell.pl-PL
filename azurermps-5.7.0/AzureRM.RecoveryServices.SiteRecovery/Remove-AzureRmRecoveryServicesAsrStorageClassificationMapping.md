---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c944bb084ccbcba740dc05a4ff1782500ff60930
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544227"
---
# <span data-ttu-id="bab66-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bab66-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="bab66-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bab66-102">SYNOPSIS</span></span>
<span data-ttu-id="bab66-103">Usuwa określone mapowanie klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="bab66-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bab66-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bab66-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bab66-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bab66-105">DESCRIPTION</span></span>
<span data-ttu-id="bab66-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** usuwa określone mapowanie klasyfikacji magazynu odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bab66-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="bab66-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bab66-107">EXAMPLES</span></span>

### <span data-ttu-id="bab66-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bab66-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="bab66-109">Rozpoczyna usuwanie określonego mapowania klasyfikacji magazynu i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="bab66-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="bab66-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bab66-110">PARAMETERS</span></span>

### <span data-ttu-id="bab66-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bab66-111">-Confirm</span></span>
<span data-ttu-id="bab66-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bab66-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bab66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab66-113">-DefaultProfile</span></span>
<span data-ttu-id="bab66-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bab66-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="bab66-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bab66-115">-InputObject</span></span>
<span data-ttu-id="bab66-116">Obiekt wejściowy do polecenia cmdlet: obiekt mapowania klasyfikacji magazynu ASR odpowiadający mapowaniu klasyfikacji magazynu ASR, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="bab66-116">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bab66-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bab66-117">-WhatIf</span></span>
<span data-ttu-id="bab66-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bab66-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bab66-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bab66-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bab66-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab66-120">CommonParameters</span></span>
<span data-ttu-id="bab66-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bab66-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab66-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bab66-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab66-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bab66-123">INPUTS</span></span>

### <span data-ttu-id="bab66-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bab66-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="bab66-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bab66-125">OUTPUTS</span></span>

### <span data-ttu-id="bab66-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bab66-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bab66-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bab66-127">NOTES</span></span>

## <span data-ttu-id="bab66-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bab66-128">RELATED LINKS</span></span>

[<span data-ttu-id="bab66-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bab66-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="bab66-130">Nowe — AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bab66-130">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
