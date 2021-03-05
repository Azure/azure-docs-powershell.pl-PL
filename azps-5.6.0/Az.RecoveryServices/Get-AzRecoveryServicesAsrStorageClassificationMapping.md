---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c5dea86066fd2b7bc6bd3b2bd3eb7ac94f401895
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963809"
---
# <span data-ttu-id="046c1-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="046c1-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="046c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="046c1-102">SYNOPSIS</span></span>
<span data-ttu-id="046c1-103">Pobiera mapowania klasyfikacji magazynu asr.</span><span class="sxs-lookup"><span data-stu-id="046c1-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="046c1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="046c1-104">SYNTAX</span></span>

### <span data-ttu-id="046c1-105">ByObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="046c1-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="046c1-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="046c1-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="046c1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="046c1-107">DESCRIPTION</span></span>
<span data-ttu-id="046c1-108">Polecenie **cmdlet Get-AzRecoveryServicesAsrStorageClassificationMapping** pobiera szczegóły mapowania klasyfikacji magazynu asr.</span><span class="sxs-lookup"><span data-stu-id="046c1-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="046c1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="046c1-109">EXAMPLES</span></span>

### <span data-ttu-id="046c1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="046c1-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="046c1-111">Lista wszystkich mapowań klasyfikacji magazynu odpowiadających określonej klasyfikacji miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="046c1-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="046c1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="046c1-112">PARAMETERS</span></span>

### <span data-ttu-id="046c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046c1-113">-DefaultProfile</span></span>
<span data-ttu-id="046c1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="046c1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="046c1-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="046c1-115">-Name</span></span>
<span data-ttu-id="046c1-116">Określa nazwę mapowania klasyfikacji magazynu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="046c1-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="046c1-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="046c1-117">-StorageClassification</span></span>
<span data-ttu-id="046c1-118">Określa obiekt klasyfikacji magazynu asr.</span><span class="sxs-lookup"><span data-stu-id="046c1-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="046c1-119">Polecenie cmdlet pobiera mapowania klasyfikacji magazynu asr odpowiadające określonej klasyfikacji magazynu</span><span class="sxs-lookup"><span data-stu-id="046c1-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="046c1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046c1-120">CommonParameters</span></span>
<span data-ttu-id="046c1-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="046c1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046c1-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="046c1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046c1-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="046c1-123">INPUTS</span></span>

### <span data-ttu-id="046c1-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="046c1-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="046c1-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="046c1-125">OUTPUTS</span></span>

### <span data-ttu-id="046c1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="046c1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="046c1-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="046c1-127">NOTES</span></span>

## <span data-ttu-id="046c1-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="046c1-128">RELATED LINKS</span></span>

[<span data-ttu-id="046c1-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="046c1-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="046c1-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="046c1-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
