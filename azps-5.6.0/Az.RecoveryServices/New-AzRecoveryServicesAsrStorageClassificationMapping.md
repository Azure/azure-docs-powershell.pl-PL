---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8ad9ca87687acfdeb526dc33cdcb5a6ec70c65bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953418"
---
# <span data-ttu-id="101a1-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="101a1-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="101a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="101a1-102">SYNOPSIS</span></span>
<span data-ttu-id="101a1-103">Tworzy mapowanie klasyfikacji magazynu asr w magazynie usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="101a1-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="101a1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="101a1-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="101a1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="101a1-105">DESCRIPTION</span></span>
<span data-ttu-id="101a1-106">Polecenie **cmdlet New-AzRecoveryServicesAsrStorageClassificationMapping** tworzy klasyfikację magazynu mapowania magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="101a1-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="101a1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="101a1-107">EXAMPLES</span></span>

### <span data-ttu-id="101a1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="101a1-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="101a1-109">Rozpoczyna operację tworzenia mapowania klasyfikacji magazynu z określonymi parametrami i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="101a1-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="101a1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="101a1-110">PARAMETERS</span></span>

### <span data-ttu-id="101a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="101a1-111">-DefaultProfile</span></span>
<span data-ttu-id="101a1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="101a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="101a1-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="101a1-113">-Name</span></span>
<span data-ttu-id="101a1-114">Określa nazwę mapowania klasyfikacji magazynu asr.</span><span class="sxs-lookup"><span data-stu-id="101a1-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="101a1-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="101a1-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="101a1-116">Określa podstawowy obiekt klasyfikacji magazynu asr dla mapowania.</span><span class="sxs-lookup"><span data-stu-id="101a1-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="101a1-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="101a1-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="101a1-118">Określa obiekt klasyfikacji magazynu asr odzyskiwania dla mapowania.</span><span class="sxs-lookup"><span data-stu-id="101a1-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="101a1-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="101a1-119">-Confirm</span></span>
<span data-ttu-id="101a1-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="101a1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="101a1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="101a1-121">-WhatIf</span></span>
<span data-ttu-id="101a1-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="101a1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="101a1-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="101a1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="101a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="101a1-124">CommonParameters</span></span>
<span data-ttu-id="101a1-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="101a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="101a1-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="101a1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="101a1-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="101a1-127">INPUTS</span></span>

### <span data-ttu-id="101a1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="101a1-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="101a1-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="101a1-129">OUTPUTS</span></span>

### <span data-ttu-id="101a1-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="101a1-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="101a1-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="101a1-131">NOTES</span></span>

## <span data-ttu-id="101a1-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="101a1-132">RELATED LINKS</span></span>

[<span data-ttu-id="101a1-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="101a1-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="101a1-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="101a1-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
