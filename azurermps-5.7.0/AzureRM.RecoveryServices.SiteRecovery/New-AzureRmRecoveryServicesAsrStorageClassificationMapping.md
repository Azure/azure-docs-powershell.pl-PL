---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e313b3dd9df76185c1eeaf289e918e1d47ace58d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716484"
---
# <span data-ttu-id="c1198-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c1198-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="c1198-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1198-102">SYNOPSIS</span></span>
<span data-ttu-id="c1198-103">Tworzy mapowanie klasyfikacji magazynu ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="c1198-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1198-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1198-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1198-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c1198-105">DESCRIPTION</span></span>
<span data-ttu-id="c1198-106">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** tworzy mapowanie klasyfikacji magazynu na magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="c1198-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="c1198-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1198-107">EXAMPLES</span></span>

### <span data-ttu-id="c1198-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c1198-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="c1198-109">Rozpoczyna operację tworzenia mapowania klasyfikacji magazynu przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="c1198-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c1198-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1198-110">PARAMETERS</span></span>

### <span data-ttu-id="c1198-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1198-111">-Confirm</span></span>
<span data-ttu-id="c1198-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1198-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1198-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1198-113">-DefaultProfile</span></span>
<span data-ttu-id="c1198-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1198-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="c1198-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c1198-115">-Name</span></span>
<span data-ttu-id="c1198-116">Określa nazwę mapowania klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="c1198-116">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="c1198-117">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c1198-117">-PrimaryStorageClassification</span></span>
<span data-ttu-id="c1198-118">Określa podstawowy obiekt klasyfikacji magazynu ASR dla mapowania.</span><span class="sxs-lookup"><span data-stu-id="c1198-118">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1198-119">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c1198-119">-RecoveryStorageClassification</span></span>
<span data-ttu-id="c1198-120">Określa obiekt klasyfikacji magazynu ASR odzyskiwania w celu mapowania.</span><span class="sxs-lookup"><span data-stu-id="c1198-120">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1198-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1198-121">-WhatIf</span></span>
<span data-ttu-id="c1198-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1198-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1198-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c1198-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1198-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1198-124">CommonParameters</span></span>
<span data-ttu-id="c1198-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1198-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1198-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1198-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1198-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1198-127">INPUTS</span></span>

### <span data-ttu-id="c1198-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c1198-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="c1198-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1198-129">OUTPUTS</span></span>

### <span data-ttu-id="c1198-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c1198-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c1198-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1198-131">NOTES</span></span>

## <span data-ttu-id="c1198-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1198-132">RELATED LINKS</span></span>

[<span data-ttu-id="c1198-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c1198-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="c1198-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c1198-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
