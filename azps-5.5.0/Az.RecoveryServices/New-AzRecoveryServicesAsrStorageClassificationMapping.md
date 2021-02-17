---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 091f8892238d88554d0e0c3502ffbeb8e8d4c154
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240275"
---
# <span data-ttu-id="d2409-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d2409-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="d2409-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2409-102">SYNOPSIS</span></span>
<span data-ttu-id="d2409-103">Tworzy mapowanie klasyfikacji magazynu asr w magazynie usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d2409-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="d2409-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2409-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2409-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2409-105">DESCRIPTION</span></span>
<span data-ttu-id="d2409-106">Polecenie **cmdlet New-AzRecoveryServicesAsrStorageClassificationMapping** tworzy klasyfikację magazynu mapowania magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d2409-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="d2409-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2409-107">EXAMPLES</span></span>

### <span data-ttu-id="d2409-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d2409-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="d2409-109">Rozpoczyna operację tworzenia mapowania klasyfikacji magazynu z określonymi parametrami i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="d2409-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d2409-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2409-110">PARAMETERS</span></span>

### <span data-ttu-id="d2409-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2409-111">-DefaultProfile</span></span>
<span data-ttu-id="d2409-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2409-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d2409-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d2409-113">-Name</span></span>
<span data-ttu-id="d2409-114">Określa nazwę mapowania klasyfikacji magazynu asr.</span><span class="sxs-lookup"><span data-stu-id="d2409-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="d2409-115">- PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d2409-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="d2409-116">Określa podstawowy obiekt klasyfikacji magazynu asr dla mapowania.</span><span class="sxs-lookup"><span data-stu-id="d2409-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="d2409-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d2409-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="d2409-118">Określa obiekt klasyfikacji magazynu asr odzyskiwania dla mapowania.</span><span class="sxs-lookup"><span data-stu-id="d2409-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="d2409-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2409-119">-Confirm</span></span>
<span data-ttu-id="d2409-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d2409-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2409-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2409-121">-WhatIf</span></span>
<span data-ttu-id="d2409-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2409-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2409-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d2409-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2409-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2409-124">CommonParameters</span></span>
<span data-ttu-id="d2409-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2409-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2409-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2409-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2409-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2409-127">INPUTS</span></span>

### <span data-ttu-id="d2409-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="d2409-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="d2409-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2409-129">OUTPUTS</span></span>

### <span data-ttu-id="d2409-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d2409-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d2409-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2409-131">NOTES</span></span>

## <span data-ttu-id="d2409-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2409-132">RELATED LINKS</span></span>

[<span data-ttu-id="d2409-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d2409-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="d2409-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d2409-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
