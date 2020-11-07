---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 152bd9cce3622f0ef0f04049b96791dc08627308
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708629"
---
# <span data-ttu-id="78848-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="78848-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="78848-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78848-102">SYNOPSIS</span></span>
<span data-ttu-id="78848-103">Tworzy mapowanie klasyfikacji magazynu ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="78848-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="78848-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78848-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78848-105">Opis</span><span class="sxs-lookup"><span data-stu-id="78848-105">DESCRIPTION</span></span>
<span data-ttu-id="78848-106">Polecenie cmdlet **New-AzRecoveryServicesAsrStorageClassificationMapping** tworzy mapowanie klasyfikacji magazynu na magazyn usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="78848-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="78848-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78848-107">EXAMPLES</span></span>

### <span data-ttu-id="78848-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="78848-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="78848-109">Rozpoczyna operację tworzenia mapowania klasyfikacji magazynu przy użyciu określonych parametrów i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="78848-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="78848-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78848-110">PARAMETERS</span></span>

### <span data-ttu-id="78848-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78848-111">-DefaultProfile</span></span>
<span data-ttu-id="78848-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78848-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78848-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78848-113">-Name</span></span>
<span data-ttu-id="78848-114">Określa nazwę mapowania klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="78848-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="78848-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="78848-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="78848-116">Określa podstawowy obiekt klasyfikacji magazynu ASR dla mapowania.</span><span class="sxs-lookup"><span data-stu-id="78848-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="78848-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="78848-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="78848-118">Określa obiekt klasyfikacji magazynu ASR odzyskiwania w celu mapowania.</span><span class="sxs-lookup"><span data-stu-id="78848-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="78848-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78848-119">-Confirm</span></span>
<span data-ttu-id="78848-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78848-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78848-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78848-121">-WhatIf</span></span>
<span data-ttu-id="78848-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78848-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78848-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="78848-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78848-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78848-124">CommonParameters</span></span>
<span data-ttu-id="78848-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78848-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78848-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78848-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78848-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78848-127">INPUTS</span></span>

### <span data-ttu-id="78848-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="78848-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="78848-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78848-129">OUTPUTS</span></span>

### <span data-ttu-id="78848-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="78848-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="78848-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78848-131">NOTES</span></span>

## <span data-ttu-id="78848-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78848-132">RELATED LINKS</span></span>

[<span data-ttu-id="78848-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="78848-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="78848-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="78848-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)