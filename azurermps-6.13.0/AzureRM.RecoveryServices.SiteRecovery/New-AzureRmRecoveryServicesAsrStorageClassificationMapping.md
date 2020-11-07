---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 6ab8102de0deb27c18c6e50f8d78db2f23a5155a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716929"
---
# <span data-ttu-id="2f607-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2f607-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="2f607-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f607-102">SYNOPSIS</span></span>
<span data-ttu-id="2f607-103">Tworzy mapowanie klasyfikacji magazynu ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2f607-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f607-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f607-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f607-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2f607-105">DESCRIPTION</span></span>
<span data-ttu-id="2f607-106">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** tworzy mapowanie klasyfikacji magazynu na magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2f607-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="2f607-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f607-107">EXAMPLES</span></span>

### <span data-ttu-id="2f607-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2f607-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="2f607-109">Rozpoczyna operację tworzenia mapowania klasyfikacji magazynu przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="2f607-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2f607-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f607-110">PARAMETERS</span></span>

### <span data-ttu-id="2f607-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f607-111">-DefaultProfile</span></span>
<span data-ttu-id="2f607-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f607-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2f607-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2f607-113">-Name</span></span>
<span data-ttu-id="2f607-114">Określa nazwę mapowania klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="2f607-114">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f607-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2f607-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="2f607-116">Określa podstawowy obiekt klasyfikacji magazynu ASR dla mapowania.</span><span class="sxs-lookup"><span data-stu-id="2f607-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f607-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2f607-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="2f607-118">Określa obiekt klasyfikacji magazynu ASR odzyskiwania w celu mapowania.</span><span class="sxs-lookup"><span data-stu-id="2f607-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f607-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f607-119">-Confirm</span></span>
<span data-ttu-id="2f607-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f607-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f607-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f607-121">-WhatIf</span></span>
<span data-ttu-id="2f607-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f607-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f607-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f607-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f607-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f607-124">CommonParameters</span></span>
<span data-ttu-id="2f607-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f607-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f607-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f607-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f607-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f607-127">INPUTS</span></span>

### <span data-ttu-id="2f607-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2f607-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="2f607-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f607-129">OUTPUTS</span></span>

### <span data-ttu-id="2f607-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2f607-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2f607-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f607-131">NOTES</span></span>

## <span data-ttu-id="2f607-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f607-132">RELATED LINKS</span></span>

[<span data-ttu-id="2f607-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2f607-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="2f607-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2f607-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
